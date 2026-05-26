# MySQL — Tool Rationale & Usage Standards

## Overview
MySQL is the **primary relational database platform** used in the NeuByte ecosystem for application development, data modeling, and backend persistence.  
It is the database engine behind the Fitness App OLTP system and is used for:

- schema design  
- relational modeling  
- transactional workloads  
- stored logic (where appropriate)  
- data integrity enforcement  
- local development and testing  

MySQL is chosen because it is lightweight, widely supported, cloud‑deployable, and integrates cleanly with modern application stacks.

---

## Why MySQL Is Included
MySQL provides several advantages that align with NeuByte’s engineering and data architecture goals:

### ✔ Industry‑Standard Relational Database
MySQL is one of the most widely used relational databases in the world.  
It supports:

- ACID transactions  
- relational integrity  
- indexing strategies  
- foreign keys  
- normalization patterns  

This makes it ideal for OLTP workloads.

### ✔ Strong Local Development Workflow
MySQL is easy to install and run locally, enabling:

- rapid schema iteration  
- local testing  
- isolated development environments  
- reproducible builds  

This supports fast prototyping and iterative design.

### ✔ Cloud‑Ready
MySQL is supported across major cloud platforms:

- Azure Database for MySQL  
- AWS RDS for MySQL  
- Google Cloud SQL  

This makes deployment flexible and scalable.

### ✔ SQL‑Based, Not Proprietary
MySQL uses ANSI SQL with minimal vendor‑specific extensions.  
This makes it:

- portable  
- easy to learn  
- compatible with SQL Server concepts  
- ideal for cross‑platform developers  

Your SQL Server background transfers cleanly.

---

## Why MySQL Is the Primary Database for NeuByte Projects
MySQL was selected for NeuByte projects because it provides:

- predictable performance  
- strong community support  
- easy integration with Python APIs  
- simple deployment to Azure  
- low operational overhead  
- strong tooling (Workbench, VS Code extensions)  

It is the right balance of power, simplicity, and portability.

---

## When to Use MySQL
Use MySQL for:

- OLTP systems  
- application backends  
- normalized relational models  
- transactional workloads  
- user management  
- logging and events  
- reference tables  
- module‑level data dictionaries  
- schema versioning  

MySQL is the **default database engine** for NeuByte application projects.

---

## When *Not* to Use MySQL
Do **not** use MySQL for:

- OLAP workloads (use Fabric or Power BI)  
- large‑scale analytics (use columnar storage)  
- unstructured data (use blob/object storage)  
- document‑centric workloads (use NoSQL)  
- real‑time streaming (use event hubs or Kafka)  

MySQL is optimized for **transactional** workloads, not analytics.

---

## Required MySQL Tools
The NeuByte toolchain includes:

### **1. MySQL Workbench**
Used for:
- schema design  
- ER modeling  
- visual relationships  
- forward engineering  
- reverse engineering  
- SQL script execution  

### **2. VS Code MySQL Extensions**
Used for:
- inline SQL editing  
- schema browsing  
- query execution  
- integration with API development  

### **3. MySQL Shell (mysqlsh)**
Used for:
- scripting  
- admin tasks  
- JSON/SQL hybrid workflows  

---

## File Formats
MySQL uses the following file types in the NeuByte ecosystem:

- `.sql` — schema scripts  
- `.md` — data dictionary documentation  
- `.png` / `.svg` — ER diagrams (exported from Workbench or Inkscape)  
- `.json` — sample payloads  
- `.csv` — import/export data  

Avoid:

- proprietary Workbench model formats for long‑term storage  
- exporting diagrams as JPG  

---

## MySQL Standards for NeuByte
All MySQL schemas must follow NeuByte database standards:

### 1. Naming Conventions
- `PascalCase` for tables  
- `camelCase` for columns  
- `_id` suffix for foreign keys  
- singular table names  
- consistent prefixing for reference tables  

### 2. Data Types
Use:
- `INT` for identifiers  
- `VARCHAR` for text  
- `DATETIME` for timestamps  
- `BOOLEAN` for flags  
- `DECIMAL` for numeric precision  

Avoid:
- `TEXT` unless required  
- `FLOAT` for financial values  

### 3. Indexing
- primary keys on all tables  
- foreign key indexes  
- composite indexes where appropriate  
- avoid over‑indexing  

### 4. Relationships
- enforce foreign keys  
- use cascading rules intentionally  
- maintain referential integrity  

---

## Workflow Integration
MySQL fits into the NeuByte workflow like this:

1. **Model** — design schema in MySQL Workbench  
2. **Document** — create module‑level Data Dictionary in Markdown  
3. **Implement** — generate SQL scripts  
4. **Test** — run locally using MySQL Server  
5. **Integrate** — connect to Python API  
6. **Deploy** — publish to Azure Database for MySQL  
7. **Version** — commit schema scripts to GitHub  

MySQL is the **data backbone** of NeuByte application development.

---

## Summary
MySQL is the **primary relational database** for NeuByte projects because it is:

- reliable  
- scalable  
- SQL‑based  
- cloud‑ready  
- easy to develop locally  
- well‑supported  
- ideal for OLTP workloads  

Use MySQL for all **application‑level relational data modeling**.  
Use Fabric, Power BI, or analytical stores for OLAP workloads.

MySQL is the **transactional data engine** of the NeuByte toolchain.
