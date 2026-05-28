# REPO-BOUNDARIES.md
**NeuByte Repository Boundary & Governance Standard  
Version 1.0**

##  Purpose
This document defines the **authoritative boundaries** for every repository in the NeuByte organization.  
It ensures:  

- clear ownership
- clean separation of concerns
- predictable documentation placement
- consistent architecture governance
- scalable multi‑repo Pages ecosystem

This is the source of truth for deciding where any file, document, or issue belongs.  

##  1. Architecture Repo
**Repository**: architecture  
**Category**: Product Architecture  
**Purpose**: Document the technical architecture of the FitnessApp system.  

### Contains
- System architecture overview
- Component relationships (MySQL ↔ API ↔ Web)
- Architecture diagrams
- Architecture Decision Records (ADRs)
- Shared technical assets
 - cross‑language shared assets
 - Python shared assets
 - C# shared assets
 - MySQL shared assets
 - Power BI shared assets
- Integration patterns
- Authentication flows
- Domain models (architecture‑level)
- Architecture philosophy

### Does NOT contain
- Functional requirements
- UI specifications
- Documentation standards
- Pages platform architecture
- Jekyll layouts, includes, or data files
- Product help content

## 2. Portfolio Repo
**Repository**: portfolio  
**Category**: Product Documentation  
**Purpose**: Store functional, behavioral, and UI documentation for the FitnessApp product.  

### Contains
- Use cases
- Requirements
- Functional specifications
- UI specifications
- Module documentation
- Data dictionary (unless moved to data repo)
- Resume system (Jekyll-based)
- Portfolio Pages site content

##  Does NOT contain
- Architecture documentation
- Documentation standards
- Pages platform architecture
- Shared technical assets
- Code

## 3. Standards Repo
**Repository**: standards  
**Category**: Documentation Architecture  
**Purpose**: Define how NeuByte documents, designs, and communicates across all repos.  

### Contains
- DESIGN-SYSTEM.md
- Typography, color, spacing rules
- Diagram grammar
- Naming conventions
- Writing standards
- Documentation templates
- Visual grammar
- Repo governance (this document)
- Cross‑repo documentation rules

###  Does NOT contain
- Product architecture
- Functional documentation
- Pages platform architecture
- Code

## 4. Router Repo
**Repository**: router  
**Category**: Pages Platform Architecture  
**Purpose**: Define the GitHub Pages ecosystem across all NeuByte repos.  

###  Contains
- Pages routing architecture
- Cross‑repo navigation
- Shared CSS
- Shared includes
- Shared layouts
- URL structure
- Ecosystem map
- Pages platform governance

### Does NOT contain
- Product architecture
- Functional documentation
- Documentation standards
- Code

## 5. fitness-api Repo
**Repository**: fitness-api  
**Category**: Product Code  
**Purpose**: Python API backend.  

### Contains
- API code
- DTOs
- Service layer
- Repository layer
- Tests
- OpenAPI spec (if generated here)

### Does NOT contain
- Architecture documentation
- Functional documentation
- Pages platform architecture
- Documentation standards

## 6. fitness-web Repo
**Repository**: fitness-web  
**Category**: Product Code  
**Purpose**: C# web frontend.  

### Contains
- Web application code
- Razor/MVC/Blazor components
- Shared UI components
- Tests

### Does NOT contain
- Architecture documentation
- Functional documentation
- Documentation standards
- Pages platform architecture

## 7. data-engineering Repo
**Repository**: data-engineering  
**Category**: Product Code  
**Purpose**: Data pipelines and ETL.  

### Contains
- ETL pipelines
- Data transformations
- Orchestration
- Data quality rules
- Pipeline diagrams

### Does NOT contain
- Product architecture
- Functional documentation
- Documentation standards
- Pages platform architecture

## 8. help-product Repo
**Repository**: help-product  
**Category**: Product Help System  
**Purpose**: Jekyll-based help article system.  

### Contains
- Help articles
- Help site layouts
- Help site includes
- Help site data files
- Help site navigation

### Does NOT contain
- Product architecture
- Functional documentation
- Documentation standards
- Pages platform architecture

## 9. Cross‑Repo Rules
✔ Rule 1 — Architecture ≠ Documentation ≠ Pages
These three domains must never mix.

✔ Rule 2 — Each Pages site has its own Jekyll framework
No cross‑repo _layouts, _includes, or _data.

✔ Rule 3 — Standards repo defines how all repos communicate
But does not contain product or architecture content.

✔ Rule 4 — Portfolio remains the home of functional documentation
Until explicitly migrated.

✔ Rule 5 — Architecture repo contains only system architecture
No functional or visual documentation.

## 10. Decision Tree (Where Does This Go?)
**Is it code?**
→ API, Web, or Data repo.

**Is it functional documentation?**
→ Portfolio repo.

**Is it product architecture?**
→ Architecture repo.

**Is it documentation standards or design system?**
→ Standards repo.

**Is it Pages platform architecture?**
→ Router repo.

**Is it help content?**
→ help-product repo.

## Final Notes
This document is the authoritative reference for all future documentation and issue placement decisions.  
Any ambiguity should be resolved by updating this document, not by bending repo boundaries.  