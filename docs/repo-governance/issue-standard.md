# issue-standard.md
NeuByte Issue Governance Standard  
Version 1.0

## Purpose
This document defines the **rules and expectations** for creating, structuring, and managing issues across all NeuByte repositories.
It ensures:

- consistent issue quality
- correct use of templates
- clean repo boundaries
- predictable workflows
- traceable decisions

This standard applies to all **NeuByte repos.**

## 1. Issue Templates & When to Use Them
**Administrative Task**
Use for operational, organizational, or governance work:

- repo setup
- cleanup
- migration
- standards updates
- Pages platform tasks (router repo)

**Bug Report**
Use for defects in:

- HTML
- Jekyll
- documentation
- diagrams
- site rendering
- code (API, Web, Data)

**Diagram Task**
Use for creating or updating diagrams using the NeuByte Visual Grammar:

- architecture diagrams
- flow diagrams
- sequence diagrams
- data lineage diagrams

**Documentation Task**
Use for creating or updating written artifacts:

- requirements
- use cases
- functional specs
- architecture docs
- standards docs
- help articles

**Enhancement Request**
Use for improving existing:

- documentation
- diagrams
- specifications
- shared components
- site capabilities

**Feature Request**
Use for requesting new:

- documentation artifacts
- diagram types
- specification sections
- site capabilities
- architectural components

**Blank Issue**
Use only when no template fits.  
Must still follow the structure in Section 2.  

## 2. Required Issue Structure
Every issue must include:

### 1. Summary
One sentence describing the task.

### 2. Problem / Context
Why this issue exists.
What triggered it.

### 3. Scope
What is included.
What is explicitly excluded.

### 4. Acceptance Criteria
Binary, testable, measurable.

### 5. Repo Classification
Choose one:

- Product Architecture → architecture
- Documentation Architecture → standards
- Product Documentation → portfolio
- Pages Platform Architecture → router
- Product Code → fitness-api / fitness-web / data-engineering
- Help System → help-product

### 6. Dependencies
List related issues or documents.

### 7. Deliverables
Document, code, diagram, or update.

## 3. Repo Boundary Rules
Before creating an issue, validate:

✔ Does this belong in this repo?
If not, create it in the correct repo.

✔ Does this issue cross repo boundaries?
If yes, split it into multiple issues.

✔ Does this violate REPO-BOUNDARIES.md?
If yes, rewrite or reject it.

❌ Never mix:
- architecture + documentation
- documentation + standards
- standards + code
- pages platform + product architecture

🏷️ 4. Labels
Every issue must include:

**Required**
- type:xxx
- priority:low|medium|high
- status:ready|in-progress|blocked|review

**Optional**
- architecture
- documentation
- standards
- pages
- api
- web
- data
- help

## 5. Issue Lifecycle
All issues follow:

**- Ready**
**- In Progress**
**- Review**
**- Done**
**- Closed** (invalid, duplicate, or rejected)

## 6. Invalid Issue Criteria
An issue must be closed as invalid if:

- it violates repo boundaries
- it mixes multiple domains
- it attempts to move content to the wrong repo
- it lacks scope or acceptance criteria
- it duplicates an existing issue
- it is based on outdated assumptions

## 7. Cross‑Repo Issue Rules
✔ Never create a single issue that spans multiple repos
Split it.

✔ Cross‑repo dependencies must be explicit
Use GitHub linking.

✔ Architecture issues must never appear in Portfolio
And vice‑versa.

✔ Standards issues must never appear in Architecture
Standards govern documentation, not product architecture.

## 8. Governance
This standard is maintained in the Standards repo.
Changes require a standards-task issue and approval.

## Final Notes
This document is the authoritative reference for issue creation and management across all NeuByte repos.