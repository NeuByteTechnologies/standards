# Excel — Tool Rationale & Usage Standards

## Overview
Excel is included in the NeuByte toolchain as a **core Systems Analyst and Analytics tool**.  
It is the standard for:

- Requirements Traceability Matrices (RTM)
- Prioritization frameworks
- KPI calculations
- Data dictionaries
- Structured tabular documentation
- Lightweight data analysis

Excel remains a dominant tool in enterprise environments due to its flexibility, familiarity, and ability to handle structured data without requiring a database or BI platform.

---

## Why Excel Is Included
Excel fills several critical roles in the documentation and analysis workflow:

### ✔ Industry Standard for RTM
Most organizations expect RTMs in Excel format because it supports:

- filtering  
- sorting  
- conditional formatting  
- cross‑referencing  
- stakeholder review  

Excel is the **de facto** format for traceability.

### ✔ Ideal for Tabular Documentation
Excel is the best tool for:

- data dictionaries  
- field mappings  
- CRUD matrices  
- prioritization grids  
- gap analysis  

These artifacts are difficult to maintain in Word or Markdown.

### ✔ Lightweight Data Analysis
Excel supports:

- pivot tables  
- quick aggregations  
- KPI calculations  
- exploratory analysis  

This makes it a bridge between raw data and Power BI.

### ✔ Universal Stakeholder Accessibility
Everyone can open an Excel file — business users, engineers, PMs, executives.

This makes it the safest choice for cross‑functional documentation.

---

## Why Excel Is *Not* Used for Everything
Excel is powerful, but it is not the right tool for:

### ❌ UI Specifications  
These belong in **Word**, where layout, narrative, and screenshots are easier to manage.

### ❌ Standards Documentation  
Markdown is better for version control, readability, and GitHub integration.

### ❌ Database Modeling  
MySQL Workbench is the correct tool for schema design.

### ❌ Complex Analytics  
Power BI is the correct tool for dashboards and visual storytelling.

Excel is used where it excels: **structured, tabular, traceable information**.

---

## When to Use Excel
Use Excel when you need:

- a Requirements Traceability Matrix  
- a Data Dictionary  
- a CRUD Matrix  
- a Prioritization Matrix  
- a KPI calculation sheet  
- a quick pivot table  
- a structured table for stakeholder review  

Excel is the right tool when the information is:

- tabular  
- sortable  
- filterable  
- cross‑referenced  
- reviewed by multiple stakeholders  

---

## When *Not* to Use Excel
Do **not** use Excel for:

- UI Specs (use Word)  
- Standards documentation (use Markdown)  
- Architecture diagrams (use Inkscape)  
- API specifications (use Markdown or JSON)  
- Database schemas (use MySQL Workbench)  
- Dashboards (use Power BI)  

Excel is not a replacement for:

- a database  
- a BI tool  
- a diagramming tool  
- a documentation system  

---

## File Formats
Recommended formats:

- `.xlsx` — primary format  
- `.csv` — for data exchange  
- `.xlsm` — only if macros are required (rare)  

Avoid:

- `.xls` — legacy format  
- exporting Excel screenshots into documentation  

---

## Workflow Integration
Excel fits into the NeuByte workflow like this:

1. **Define requirements** → Word / Markdown  
2. **Map requirements** → Excel RTM  
3. **Model data** → MySQL Workbench  
4. **Analyze data** → Excel pivots  
5. **Visualize insights** → Power BI  
6. **Document standards** → Markdown  

Excel is the **traceability and analysis layer** of the workflow.

---

## Summary
Excel is a **core Systems Analyst and Analytics tool** used for structured, tabular documentation and lightweight analysis.

Use it for:
- RTM  
- Data dictionaries  
- CRUD matrices  
- KPI calculations  
- Prioritization frameworks  

Do not use it for:
- UI specs  
- diagrams  
- standards documentation  
- dashboards  
- database modeling  

Excel is the **structure and traceability engine** of the NeuByte toolchain.
