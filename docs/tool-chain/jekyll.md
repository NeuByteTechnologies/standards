# Jekyll — Tool Rationale & Usage Standards

## Overview
Jekyll is the static site generator that powers **GitHub Pages**.  
It converts Markdown files, YAML metadata, layouts, and assets into a fully rendered documentation website.

Jekyll is included in the NeuByte toolchain because it enables the Standards Repository to function as a **professional, browsable documentation portal** without requiring servers, databases, or deployment pipelines.

Jekyll is optional — but when GitHub Pages is enabled, it becomes the underlying engine.


## Why Jekyll Is Included
Jekyll provides several capabilities that align perfectly with a standards‑driven ecosystem:

### ✔ Converts Markdown Into a Website
Your standards repo is Markdown‑based.  
Jekyll transforms that Markdown into:

- HTML pages  
- navigation structures  
- layouts  
- styled documentation  

This makes your repo feel like a real documentation site.

### ✔ Uses YAML Front‑Matter for Metadata
Every page can define:

- title  
- layout  
- navigation order  
- categories  
- tags  
- custom variables  

Example:

---
title: Inkscape Standards
layout: default
---

This metadata controls how the page is rendered.

✔ Supports Layouts and Includes
Jekyll allows you to define:
- reusable page layouts
- shared headers and footers
- navigation menus
- reusable components

This keeps your documentation consistent and maintainable.  

✔ Zero Infrastructure
Jekyll runs automatically on GitHub Pages.  
No servers.  
No deployments.  
No build pipelines.  

GitHub handles everything.  

### Why Jekyll Is Optional
Jekyll is only required if you enable GitHub Pages.  

If you choose not to publish the repo as a website, you can ignore Jekyll entirely and rely on raw Markdown rendering in GitHub.  

The Standards Repo works perfectly without Jekyll.  

### When to Use Jekyll
Use Jekyll when you want:  

- a polished documentation website
- a structured navigation system
- a public‑facing standards portal
- a browsable design system
- a clean, professional presentation layer

Jekyll is ideal when your repo grows large and you want readers to navigate it easily.  

### When *Not* to Use Jekyll
Do not use Jekyll when:

- you want minimal overhead
- you prefer raw Markdown browsing
- you don’t want to maintain layouts or navigation
- you want advanced documentation features (Docusaurus, MkDocs, etc.)

Jekyll is simple and powerful — but not infinitely flexible.  

### Core Jekyll Concepts
**1. YAML Front‑Matter**
Every Jekyll page begins with a YAML block:

title: Example Page
layout: default

This metadata tells Jekyll how to render the page.

**2. Layouts**
Layouts define the structure of your pages.

Example:

_layouts/
  default.html
  page.html
  standard.html


Layouts allow you to maintain a consistent look across the entire site.

**3. Includes**
Reusable components stored in:

_includes/


Examples:

- navigation menus
- headers
- footers
- callout blocks

Includes reduce duplication and improve maintainability.

**4. Collections**
Collections group related content.

Example:

collections:
  standards:
    output: true
  toolchain:
    output: true

This allows you to create structured sections of your documentation site.

**5. Configuration (_config.yml)**
The central configuration file controls:

- site metadata
- theme
- navigation
- collections
- plugins
- Markdown engine

Example:

yaml
title: NeuByte Standards
markdown: kramdown
theme: minimal

### Folder Structure for Jekyll

If GitHub Pages is enabled, your repo may include:

Code
standards/  
│  
├── _config.yml  
├── _layouts/  
├── _includes/  
├── _sass/          (optional)  
├── assets/         (CSS, images)  
└── docs/           (optional build root)  
  
This structure is optional and only needed if you want a custom site.  

### Workflow Integration*
Jekyll fits into the NeuByte workflow like this:

- **Write standards** → Markdown
- **Add metadata** → YAML front‑matter
- **Apply layouts** → Jekyll templates
- **Build site** → GitHub Pages
 - **Publish** → automatic hosting
 - **Update** → commit → auto‑rebuild

Jekyll is the rendering engine of the NeuByte documentation ecosystem.  

### Summary
Jekyll is the static site generator that powers GitHub Pages.  
It transforms your Markdown‑based Standards Repository into a professional documentation website.  

Use Jekyll for:  

- public‑facing standards
- design system documentation
- toolchain explanations
- role‑based standards
- templates and diagrams

Avoid Jekyll when:  

- you want minimal overhead
- you prefer raw Markdown
- you don’t want to maintain layouts or navigation
- Jekyll is the engine behind the NeuByte documentation site.
