# Inkscape Standards (NeuByte Visual Grammar v2.0)
## 1. Purpose
This document defines the official NeuByte diagramming standards for all Inkscape‑produced diagrams.  
It ensures consistency across:  

- Architecture diagrams
- UI flows
- Swimlane diagrams
- Sequence diagrams
- System context diagrams
- Component diagrams

This standard aligns with the NeuByte Visual Grammar v2.0 and the CSS design tokens used in the NeuByte web theme.  

## 2. Included Files
### 2.1 Default Template
`default.svg`  
Contains:  

- Default stroke
- Default fill
- Default font
- Default text color
- Default page settings
- Default grid/snapping (if enabled)
- Default arrow markers

### 2.2 NeuByte Palette
`NeuByte-Extended.gpl ` 
Contains:

- Semantic colors
- Neutral colors
- Stroke colors
- Emphasis fills
- Metadata colors
- UI element colors

### 2.3 Inkscape Application Defaults
These are the settings configured inside Inkscape itself:  

- Default stroke = #333333, 2px
- Default fill = none
- Default font = Manrope 14px
- Default text color = #333333
- Default palette = NeuByte Extended
- Export presets (PNG @ 2×, SVG clean, etc.)

## 3. Layering Standard
This is the part you were asking about — and yes, this is separate from visual grammar.  
Visual grammar defines how things look.  
Layering defines how things are organized.  

They complement each other but are not the same system.

### NeuByte Layering Model (Final Standard)

---

01 - Background  
02 - Containers  
03 - Shapes & Nodes  
04 - Connectors  
05 - Labels & Text  
06 - Annotations / Callouts  
07 - Metadata (title block, legend)  

-- 

**Why this order?**   
Because it matches:  

- Human editing workflow  
- Z‑index logic in CSS
- How Inkscape handles selection
- How diagrams are typically constructed  

**Why Swimlanes are Layer 02 (not 04 or 05)**  
You were absolutely right earlier — **swimlanes are background containers**, not primary elements.  

They belong under nodes, connectors, and labels.  

This is the correct hierarchy:  

- Swimlanes = containers
- Buttons, nodes, UI elements = shapes
- Connectors = above shapes
- Text = above connectors

This makes editing dramatically easier.  

## 4. Naming Conventions
**Layers**

---

01-background
02-containers
03-nodes
04-connectors
05-text
06-annotations
07-metadata

---

**Groups**

---

node-login-button
node-api-gateway
container-swimlane-user
connector-auth-flow
label-title

**Components**

---

btn-primary
ui-field
ui-card
diagram-node
diagram-container

---

##  5. Visual Grammar Alignment
This section explains how Inkscape diagrams map to the NeuByte CSS system:

| Visual Grammar Token | Inkscape Equivalent |
| --- | --- |
| ``--stroke-default`` | Default stroke in default.svg |
| ``--color-neutral-700`` | Palette swatch |
| ``--font-body`` | Manrope 14px default |
| ``--radius-md`` | Rounded rectangle corner radius |
| ``--spacing-md`` | Grid spacing / padding |


This ensures diagrams match:  

- Web UI
- Documentation
- Slide decks
- Architecture diagrams  
- Everything stays visually unified.

## 6. Export Standards
**PNG**

- 2× scale
- Transparent background
- Clean edges

**SVG**
- Remove metadata
- Remove editor namespace
- Keep IDs
- Keep groups
- Keep layers

## 7. File Locations

---

/docs/diagrams/Inkscape-standards.md  
/docs/diagrams/default.svg  
/docs/diagrams/NeuByte-Extended.gpl  
/docs/diagrams/examples/  

---