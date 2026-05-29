# Mermaid — Tool Rationale & Usage Standards

## Overview
Mermaid is included in the NeuByte toolchain as an **optional, text‑based diagramming tool**.  
It is primarily used for lightweight, inline diagrams inside Markdown files — especially in GitHub, GitLab, and documentation systems that support Mermaid rendering.

Mermaid is *not* used for final, polished diagrams.  
It is a convenience tool for quick, text‑driven visuals that support documentation, not design.

---

## Why Mermaid Is Included
Mermaid provides several advantages for documentation workflows:

### ✔ Text‑Based Diagrams
Diagrams are written as code:

````markdown
```mermaid
flowchart TD
    A[Start] --> B[Process]
    B --> C[End]
    ```