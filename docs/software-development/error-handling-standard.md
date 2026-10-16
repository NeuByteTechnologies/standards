## 1. Purpose
This standard defines a unified, cross‑system error model for all NeuByte components, including:

C# applications (fitness-app, services, APIs)

Python ETL/ELT pipelines

SQL stored procedures and database utilities

Azure Data Factory / Synapse / Functions

DevOps scripts

Jekyll/YAML tooling

Any future components

The goal is continuity across concerns: consistent error categories, codes, envelopes, logging, severity, and alerting.

## 2. Error Envelope (Canonical Format)

All components MUST return or log errors using the following envelope:

Code
---
{
  "success": false,
  "error": {
    "code": "STRING",
    "category": "STRING",
    "message": "STRING",
    "statusCode": NUMBER,
    "severity": "INFO | WARNING | ERROR | CRITICAL",
    "isOperational": true | false,
    "traceId": "UUIDv4",
    "timestamp": "ISO-8601",
    "details": {},
    "meta": {}
  }
}
---

### Required Fields
code — unique error code from the registry

category — one of the categories defined below

message — human-readable description

statusCode — HTTP-style numeric code (even outside HTTP contexts)

severity — determines logging and alerting behavior

isOperational — indicates whether the system is stable

traceId — required for cross-system correlation

timestamp — ISO-8601 UTC

details — structured data about the failure

meta — optional metadata

## 3. Error Categories
### 3.1 VALIDATION
User input, schema validation, field-level issues.

**Examples:**

- VALIDATION_REQUIRED_FIELD
- VALIDATION_INVALID_FORMAT
- VALIDATION_SCHEMA_MISMATCH

### 3.2 AUTHENTICATION
Identity verification failures.

**Examples:**

- AUTH_TOKEN_EXPIRED
- AUTH_INVALID_CREDENTIALS

### 3.3 AUTHORIZATION
Permission or role-based failures.

**Examples:**

- AUTH_FORBIDDEN
- AUTH_INSUFFICIENT_PERMISSIONS

### 3.4 DOMAIN
Business logic failures.

**Examples:**

- WORKOUT_NOT_FOUND
- USER_DUPLICATE_EMAIL
- NUTRITION_INVALID_MACRO

### 3.5 DATABASE
Database connectivity, query, or constraint issues.

**Examples:**

- DB_CONNECTION_FAILED
- DB_TIMEOUT
- DB_DUPLICATE_KEY
- DB_DEADLOCK

### 3.6 EXTERNAL_SERVICE
Failures from external APIs or third-party systems.

**Examples:**

- EXT_TIMEOUT
- EXT_RATE_LIMIT
- EXT_BAD_RESPONSE

### 3.7 INTERNAL
Unexpected or unhandled exceptions.

**Examples:**

- SYSTEM_INTERNAL_ERROR
- SYSTEM_NULL_REFERENCE
- SYSTEM_UNEXPECTED_STATE

### 3.8 CONFIGURATION
Missing or invalid configuration.

**Examples:**

- CONFIG_MISSING_ENV_VAR
- CONFIG_INVALID_VALUE

### 3.9 NETWORK
Connectivity issues.

**Examples:**

- NET_DNS_FAILURE
- NET_SOCKET_ERROR
- NET_UNREACHABLE

### 3.10 FILESYSTEM
File or directory issues.

**Examples:**

- FS_FILE_NOT_FOUND
- FS_PERMISSION_DENIED
- FS_PATH_TOO_LONG

### 3.11 ETL / ELT
Errors related to data ingestion, transformation, loading, orchestration, or runtime.

- ETL_INGESTION
- ETL_INGESTION_FILE_NOT_FOUND
- ETL_INGESTION_SOURCE_UNAVAILABLE
- ETL_INGESTION_MALFORMED_INPUT
- ETL_TRANSFORMATION
- ETL_TRANSFORMATION_SCHEMA_DRIFT
- ETL_TRANSFORMATION_TYPE_MISMATCH
- ETL_TRANSFORMATION_DATA_QUALITY_FAILURE
- ETL_TRANSFORMATION_PYTHON_EXCEPTION
- ETL_TRANSFORMATION_SQL_EXCEPTION
- ETL_LOAD
- ETL_LOAD_WRITE_FAILED
- ETL_LOAD_BULK_INSERT_FAILURE
- ETL_LOAD_DUPLICATE_KEY
- ETL_ORCHESTRATION
- ETL_ORCH_ADF_PIPELINE_FAILURE
- ETL_ORCH_FUNCTION_TIMEOUT
- ETL_ORCH_ACTIVITY_DEPENDENCY_FAILURE
- ETL_RUNTIME
- ETL_RUNTIME_OOM
- ETL_RUNTIME_RESOURCE_THROTTLING
- ETL_RUNTIME_LONG_RUNNING_TIMEOUT

## 4. Severity Levels
### INFO
Non-impactful informational events.

### WARNING
Recoverable issues, degraded performance.

### ERROR
Operational failures requiring attention.

### CRITICAL
System instability, data loss, or pipeline failure.

## 5. Operational Flag
- isOperational = true
 - The system is stable; error is expected or recoverable.
- isOperational = false
 - The system is unstable; error indicates a bug, corruption, or critical failure.

## 6. Status Codes
Even outside HTTP contexts, all systems MUST use HTTP-style numeric codes:

- 400 — Validation
- 401 — Authentication
- 403 — Authorization
- 404 — Not Found
- 409 — Conflict
- 422 — Domain
- 429 — Rate Limit
- 500 — Internal
- 503 — External Service / ETL Orchestration

ETL-specific:

- 560 — ETL Ingestion
- 561 — ETL Transformation
- 562 — ETL Load
- 563 — ETL Orchestration
- 564 — ETL Runtime

## 7. Trace ID Standard
- MUST be UUID v4
- MUST be included in all logs and envelopes
- MUST propagate across systems (C#, Python, SQL, Azure)

## 8. Redaction Rules
The following MUST be removed from all logs and envelopes:

- passwords
- tokens
- Authorization header
- credit card numbers
- PII fields
- request bodies > 10 KB

## 9. Alerting Rules
### CRITICAL
- PagerDuty
- Slack
- Full diagnostic logging

### ERROR (non-operational)
- Slack
- Error log

### WARNING
- Warning log

### INFO
- No alert

## 10. Error Code Registry
All error codes MUST be defined in:

### Code
standards/software-development/error-codes.md
Codes MUST be:

- UPPER_SNAKE_CASE
- prefixed by category
- globally unique

## 11. Cross-System Implementation Requirements
### C#
- AppException class
- ErrorType registry
- ErrorEnvelope model
- ErrorHandlerMiddleware

### Python
- AppError class
- same envelope
- same error codes

### SQL
- stored procedures return envelope JSON
- error codes match registry

### Azure
- ADF/Synapse/Functions MUST emit envelope logs

### DevOps
- scripts MUST emit envelope logs

### Jekyll/YAML
- tooling MUST emit envelope logs

## 12. Versioning
This standard is versioned using semantic versioning:

Code
---
error-handling-standard v1.0.0
Updates MUST be documented in:
---

Code
---
standards/software-development/versioning-standard.md
---
