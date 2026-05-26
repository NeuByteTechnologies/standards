# Inkscape — Tool Rationale & Usage Standards

## Overview
Inkscape is the **primary diagramming tool** in the NeuByte toolchain.  
It is used to create all final, production‑quality diagrams that follow the NeuByte Visual Grammar, including:

- architecture diagrams  
- process flows  
- UI flow diagrams  
- data flow diagrams  
- system context diagrams  
- component diagrams  
- design system visuals  

Inkscape provides the precision, control, and SVG‑native workflow required to maintain a consistent, professional visual identity across all NeuByte documentation.

---

## Why Inkscape Is Included
Inkscape is chosen as the primary diagramming tool because it supports the core principles of the NeuByte design system:

### ✔ Vector‑Native (SVG)
All diagrams are created as scalable vector graphics, ensuring:

- pixel‑perfect clarity  
- infinite scalability  
- clean exports to PowerPoint  
- consistent rendering across GitHub and browsers  

### ✔ Full Control Over Visual Grammar
Inkscape allows strict enforcement of NeuByte diagram rules:

- 2 pt stroke width  
- Manrope typography  
- NeuByte color palette  
- consistent spacing  
- consistent arrowheads  
- rounded corners  
- semantic color usage  

No other tool provides this level of control.

### ✔ Customizable Defaults
Inkscape supports:

- default stroke settings  
- default text styles  
- default fill/stroke colors  
- reusable templates (`default.svg`)  
- custom palettes (`NeuByte-Extended.gpl`)  

This ensures every diagram starts with the correct visual foundation.

### ✔ Open Source & Cross‑Platform
Inkscape is:

- free  
- open source  
- cross‑platform  
- widely supported  

This makes it ideal for long‑term standards documentation.

---

## Why Inkscape Is the *Primary* Diagramming Tool
Other tools (Draw.io, Mermaid) are useful for drafts, but they cannot enforce:

- consistent stroke widths  
- consistent typography  
- consistent spacing  
- consistent color semantics  
- consistent arrowheads  
- consistent corner radii  

Inkscape is the only tool capable of producing **final, polished, standards‑compliant diagrams**.

---

## When to Use Inkscape
Use Inkscape for:

- final architecture diagrams  
- final process flows  
- final UI flows  
- final data flows  
- diagrams included in standards  
- diagrams included in the design system  
- diagrams included in PowerPoint  
- diagrams included in your portfolio  
- diagrams exported to GitHub  

If it is a **final deliverable**, it must be created in Inkscape.

---

## When *Not* to Use Inkscape
Do **not** use Inkscape for:

- quick sketches (use Draw.io)  
- whiteboard‑style brainstorming  
- temporary diagrams  
- rough drafts  
- collaborative ideation  

Inkscape is for **precision and polish**, not speed.

---

## Required Inkscape Assets
The NeuByte design system includes the following Inkscape assets:

### **1. `default.svg`**
The base template containing:
- page size  
- grid settings  
- snapping rules  
- default stroke width  
- default text style  
- default color palette  

### **2. `NeuByte-Extended.gpl`**
The official NeuByte color palette:
- grayscale neutrals  
- primary blues  
- semantic colors  
- accent colors  

### **3. Tool Defaults**
Documented in `tool-defaults.md`, including:
- stroke settings  
- fill settings  
- text defaults  
- arrowhead defaults  
- shape defaults  

### **4. Export Presets**
Documented in `export-presets.md`, including:
- PNG export settings  
- DPI  
- transparency rules  
- naming conventions  

---

## File Formats
Recommended formats:

- `.svg` — primary editable format  
- `.png` — export for PowerPoint or GitHub  
- `.pdf` — optional for print  

Avoid:

- `.jpg` — lossy  
- `.gif` — low fidelity  
- `.bmp` — unnecessary  

---

## Workflow Integration
Inkscape fits into the NeuByte workflow like this:

1. **Draft** — rough sketch in Draw.io (optional)  
2. **Design** — rebuild in Inkscape using NeuByte visual grammar  
3. **Export** — SVG → PNG → PowerPoint or GitHub  
4. **Document** — embed in standards or design system  
5. **Version** — commit SVG + PNG to GitHub  

Inkscape is the **craftsmanship layer** of the NeuByte ecosystem.

---

## Summary
Inkscape is the **primary diagramming tool** for NeuByte because it provides:

- vector precision  
- strict visual grammar enforcement  
- customizable defaults  
- reusable templates  
- consistent exports  
- professional, polished diagrams  

Use Inkscape for all **final, standards‑compliant diagrams**.  
Use Draw.io only for drafts.

Inkscape is the **visual identity engine** of the NeuByte toolchain.
