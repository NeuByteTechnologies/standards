# Draw.io (diagrams.net) — Tool Rationale & Usage Standards

## Overview
Draw.io (also known as diagrams.net) is included in the NeuByte toolchain as a **secondary diagramming tool** used for:
- rapid ideation  
- low‑fidelity sketches  
- collaborative drafts  
- quick architecture explorations  
- early‑stage process flows  

It is *not* the primary tool for final, polished diagrams.  
That role belongs to **Inkscape**, which enforces the NeuByte visual grammar.

Draw.io is chosen because it is:
- free and browser‑based  
- fast for rough work  
- easy to share  
- easy to embed in GitHub  
- ideal for early thinking before committing to SVG standards  

---

## Why Draw.io Is Included
Draw.io fills a specific need in the design workflow:

### ✔ Speed  
It allows quick diagramming without setting up a full Inkscape environment.

### ✔ Collaboration  
It supports real‑time editing and link sharing.

### ✔ Low‑Friction Drafting  
Perfect for:
- brainstorming  
- whiteboard‑style flows  
- early architecture sketches  
- rough system layouts  

### ✔ GitHub Integration  
Draw.io files (`.drawio` or `.drawio.svg`) can be stored directly in the repo.

---

## Why Draw.io Is *Not* the Primary Diagramming Tool
NeuByte diagrams follow a strict **visual grammar**:

- 2 pt strokes  
- Manrope typography  
- NeuByte color palette  
- consistent spacing  
- consistent arrowheads  
- semantic color rules  
- SVG‑first workflow  

Draw.io cannot enforce these rules reliably.

Therefore:

### ❌ Not used for final diagrams  
### ❌ Not used for portfolio visuals  
### ❌ Not used for standards documentation  
### ❌ Not used for PowerPoint exports  
### ❌ Not used for the design system examples  

All final diagrams must be created in **Inkscape**.

---

## When to Use Draw.io
Use Draw.io when you need:

- a fast sketch  
- a collaborative draft  
- a disposable diagram  
- a rough layout to think through a problem  
- a temporary visual for internal notes  
- a diagram that will later be rebuilt in Inkscape  

Examples:
- early system architecture  
- rough ERD before MySQL modeling  
- brainstorming flows  
- whiteboard‑style ideation  

---

## When *Not* to Use Draw.io
Do **not** use Draw.io for:

- final architecture diagrams  
- diagrams included in the portfolio  
- diagrams included in standards  
- diagrams included in PowerPoint  
- anything requiring NeuByte visual grammar  
- anything exported as SVG for reuse  

These must be created in **Inkscape**.

---

## File Formats
Recommended formats:

- `.drawio` — editable source  
- `.drawio.svg` — hybrid format viewable in GitHub  
- `.png` — only for temporary sharing  

Final diagrams should **never** remain in Draw.io format.

---

## Workflow Integration
Draw.io fits into the NeuByte workflow like this:

1. **Ideate** — rough sketch in Draw.io  
2. **Refine** — rebuild in Inkscape using NeuByte visual grammar  
3. **Export** — SVG → PowerPoint → LinkedIn or repo  
4. **Document** — include final SVG in standards or design system  

This keeps the workflow fast *and* consistent.

---

## Summary
Draw.io is a **supporting tool**, not a primary one.  
It accelerates early thinking but does not replace Inkscape.

Use it for:
- speed  
- collaboration  
- drafts  

Do not use it for:
- final diagrams  
- portfolio visuals  
- standards documentation  

Draw.io is the **whiteboard**.  
Inkscape is the **craftsmanship**.