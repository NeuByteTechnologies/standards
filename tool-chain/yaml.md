# YAML — Tool Rationale & Usage Standards

## Overview
YAML is a **core configuration and data‑serialization format** in the NeuByte toolchain.  
It is used for:

- Jekyll front‑matter  
- GitHub Pages configuration  
- Python configuration files  
- data structures for the resume system  
- structured metadata for standards  
- environment settings  
- toolchain configuration  

YAML is chosen because it is human‑readable, Git‑friendly, and widely supported across modern tooling.

---

## Why YAML Is Included
YAML provides several advantages that align with NeuByte’s documentation and development strategy:

### ✔ Human‑Readable Structure
YAML is designed to be:

- clean  
- indentation‑based  
- easy to scan  
- easy to edit  

This makes it ideal for configuration files and structured metadata.

### ✔ Git‑Friendly
YAML is plain text, which means:

- clean diffs  
- easy merges  
- minimal conflicts  
- long‑term maintainability  

Perfect for GitHub‑based workflows.

### ✔ Native to Jekyll & GitHub Pages
YAML is required for:

- front‑matter metadata  
- `_config.yml`  
- collections  
- navigation  
- layouts  

Your entire GitHub Pages system depends on YAML.

### ✔ Ideal for Structured Data
YAML is used for:

- resume data (`_data/work.yml`, `_data/skills.yml`)  
- toolchain metadata  
- standards metadata  
- configuration files  

It provides structure without the verbosity of JSON.

---

## Why YAML Is *Not* Used for Everything
YAML is powerful, but it is not the right tool for:

- large datasets (use CSV or SQL)  
- complex schemas (use JSON or SQL)  
- diagrams (use Inkscape)  
- UI specs (use Word)  
- analytics (use Power BI)  

YAML is for **configuration and structured metadata**, not data modeling or documentation.

---

## When to Use YAML
Use YAML for:

- Jekyll front‑matter  
- GitHub Pages configuration  
- resume data files  
- structured metadata  
- Python configuration  
- environment settings  
- toolchain definitions  

YAML is the **configuration backbone** of the NeuByte ecosystem.

---

## When *Not* to Use YAML
Do **not** use YAML for:

- large tables (use Excel)  
- relational data (use MySQL)  
- diagrams (use Inkscape)  
- UI specs (use Word)  
- analytics (use Power BI)  

YAML is not a replacement for databases or