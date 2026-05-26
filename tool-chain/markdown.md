# Markdown — Tool Rationale & Usage Standards

## Overview
Markdown is a **core documentation tool** in the NeuByte toolchain.  
It is the primary format for:

- standards documentation  
- toolchain documentation  
- design system documentation  
- templates and examples  
- project READMEs  
- folder‑level overviews  
- lightweight specifications  
- diagrams explanations  
- developer‑facing documentation  

Markdown is chosen because it is lightweight, version‑control friendly, GitHub‑native, and readable in both raw and rendered form.

---

## Why Markdown Is Included
Markdown supports the core principles of the NeuByte documentation philosophy:

### ✔ GitHub‑Native
GitHub renders Markdown automatically, making it ideal for:

- standards  
- templates  
- diagrams  
- documentation sites (via GitHub Pages)  

No conversion required.

### ✔ Version‑Control Friendly
Markdown is plain text, which means:

- clean diffs  
- easy merges  
- minimal conflicts  
- long‑term maintainability  

This is essential for standards documentation.

### ✔ Lightweight and Readable
Markdown is readable even without rendering:

## Section Title
- Bullet point
- Another bullet

This makes it ideal for technical documentation.

### ✔ Flexible but Structured
Markdown supports:

- headings  
- lists  
- tables  
- code blocks  
- callouts  
- embedded images  
- links  
- diagrams (via SVG or Mermaid if needed)  

It provides structure without the overhead of Word or HTML.

---

## Why Markdown Is *Not* Used for Everything
Markdown is powerful, but it is not the right tool for:

### ❌ UI Specifications  
These require screenshots, annotations, and layout control → **Word**.

### ❌ RTMs and Data Dictionaries  
These require sorting, filtering, and tabular manipulation → **Excel**.

### ❌ High‑fidelity diagrams  
These require vector precision → **Inkscape**.

Markdown is used where text‑based documentation is needed — not where layout or data manipulation is required.

---

## When to Use Markdown
Use Markdown for:

- standards documentation  
- toolchain documentation  
- design system documentation  
- API documentation  
- developer guides  
- folder READMEs  
- templates  
- code samples  
- diagrams explanations  
- project documentation  

Markdown is the **default documentation format** for NeuByte.

---

## When *Not* to Use Markdown
Do **not** use Markdown for:

- UI Specs (use Word)  
- RTMs (use Excel)  
- Data Dictionaries (Excel or MySQL Workbench)  
- final diagrams (use Inkscape)  
- dashboards (use Power BI)  
- formal client‑facing documents (use Word/PDF)  

Markdown is for **technical documentation**, not polished deliverables.

---

## Markdown Standards for NeuByte
All Markdown files must follow the NeuByte formatting rules:

### **1. Heading Hierarchy**

# H1 — Document Title
## H2 — Major Section
### H3 — Subsection
#### H4 — Optional Subsection


### 2. Code Blocks
Use fenced code blocks:


```json
{
  "example": true
}
```

### 3. Tables
Use GitHub‑flavored Markdown tables:

```markdown
| Field | Type | Description |
|-------|------|-------------|
| id    | int  | Primary key |
```

### 4. Images
Embed SVG or PNG:

```markdown
![System Diagram](../diagrams/system-overview.svg)
```

### 5. Links
Relative links only:

```markdown
[Toolchain](../toolchain/README.md)
```

### 6. File Naming
Use `PascalCase.md` for standards and documentation.

---

## File Types
Markdown files use:

- `.md` — primary format  
- `.markdown` — allowed but not preferred  

Avoid:

- `.txt` — lacks structure  
- `.docx` — not version‑friendly  
- `.html` — unnecessary complexity  

---

## Workflow Integration
Markdown fits into the NeuByte workflow like this:

1. **Author** — Write documentation in VS Code  
2. **Version** — Commit to GitHub  
3. **Render** — GitHub displays Markdown automatically  
4. **Publish** — Optional GitHub Pages site  
5. **Integrate** — Link Markdown to diagrams, templates, and standards  

Markdown is the **documentation backbone** of the NeuByte ecosystem.

---

## Summary
Markdown is the **primary documentation format** for NeuByte because it is:

- lightweight  
- readable  
- GitHub‑native  
- version‑control friendly  
- flexible  
- ideal for standards and technical documentation  

Use Markdown for all **text‑based standards and documentation**.  
Use Word, Excel, and Inkscape where their strengths apply.

Markdown is the **foundation** of the NeuByte documentation system.
```

---

If you want to continue alphabetically, the next file is:

### **`mysql.md`**

Just say **“next mysql”** and I’ll generate it.
