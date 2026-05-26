# Project Management Standard
## NeuByte Technologies — GitHub Organization Standard

## 1. Purpose
The NeuByte Project Management Standard defines how all work is organized, tracked, and executed across the NeuByte GitHub Organization.  
It ensures:  

- Consistency across all repositories
- Predictable sprint execution
- Clear documentation and traceability
- A unified workflow for Issues, Sprints, and Views
- A professional, portfolio‑grade project system

This standard applies to all projects created from the NeuByte Project Template.

## 2. Project Template Overview
All new projects must be created from the NeuByte Project Template.  
The template provides:  

- Custom fields
- Standardized views
- Sprint structure
- Automation rules
- Naming conventions
- Area and Category taxonomy

Only the owner (Gordon) may create new projects from the template.  

## 3. Custom Fields
All Issues must use the following fields:

### 3.1 Required Fields
| Field | Type | Purpose |
| --- | --- | --- |
| **Status** | Single-select | Workflow state (Backlog → Ready → In Progress → In Review → Done) |
| **Priority** | Single-select | P1, P2, P3 — determines execution order |
| **Area** | Single-select | Maps to repository or major work domain |
| **Category** | Single-select | Type of work (Documentation, Diagrams, Feature, etc.) |
| **Sprint** | Iteration | Weekly sprint assignment |
| **Effort** | Number | Story Points (1, 2, 3, 5, 8) |
| **Repo** | Text | Repository name where work lives |


### 3.2 Optional Fields
| Field | Type | Purpose |
| --- | --- | --- |
| **Milestone** | Single-select | Historical Work, LinkedIn Strategy, etc. |
| **Target Date** | Date | Optional deadline |

## 4. Areas (Where Work Lives)
Areas represent **repositories or major work domains.**

Standard Areas:

- **Portfolio**
- **Resume System**
- **Design System**
- **API**
- **Architecture**

Every Issue must belong to exactly one Area.  

## 5. Categories (What Type of Work It Is)
Categories describe the nature of the work, not where it lives.  

Standard Categories:  

-Feature
- Bug
- Documentation
- Diagram
- Enhancement
- Standard
- Sprint Notes

Every Issue must have exactly one Category.

## 6. Status Workflow
All Issues follow the same lifecycle:  

- Backlog — Not ready for work
- Ready — Prioritized and ready to start
- In Progress — Actively being worked
- In Review — Needs validation or review
- Done — Completed

Issues may not skip states unless explicitly justified.  

## 7. Sprint Structure
NeuByte uses weekly sprints, Monday → Sunday.  

### 7.1 Sprint Naming
```
Sprint 1
Sprint 2
Sprint 3
```
### 7.2 Sprint Cadence
- New sprint begins Sunday morning
- Sprint Board automatically updates to the current sprint
- Issues must be assigned to a sprint before work begins

### 7.3 Sprint Notes
Sprint Notes are stored as Discussions, not Issues.
Each Sprint Note has a placeholder Issue linking to the Discussion so it appears in the project.

## 8. Views
The NeuByte Project Template includes the following standardized views:

### 8.1 Backlog (Table)
- Shows all Issues
- Sorted by Priority
- Used for planning and grooming

### 8.2 Sprint Board (Board)
The only Board view  
- Filters: Sprint = Current
- Grouped by Status
- Used for weekly execution

### 8.3 Area Views (Tables)
Each Area has its own Table view:
- Portfolio Work
- Resume System
- Design System
- API Work
- Architecture
- Web Work

Filters:
`Area = <Area Name>`

### 8.4 Category Views (Tables)
- Documentation
- Diagrams

Filters:
`Category = <Category Name>`

### 8.5 Sprint Notes Archive (Table)
Shows placeholder Issues linking to Sprint Note Discussions.

Filters:

`Category = Documentation`
`Milestone = Historical Work`
`Title contains “Sprint”`

## 9. Automation Rules
The template includes the following automation:

### 9.1 Status Automation
When Issue is moved to In Progress, set `Status = In Progress`
When Issue is moved to Done, set `Status = Done`

### 9.2 Sprint Automation
Sprint Board automatically updates to the current sprint  
Issues added to the Sprint Board automatically receive the current Sprint  

### 9.3 New Issue Automation
New Issues added to the project automatically go to Backlog

## 10. Issue Creation Rules
All Issues must follow these rules:  

### 10.1 Required Elements
- Clear title
- Description with acceptance criteria
- Area
- Category
- Priority
- Sprint (if active work)
- Effort (Story Points)

### 10.2 Placeholder Issues
Used for:

- Sprint Notes
 - LinkedIn Feedback Hub
 - Documentation Discussions
- Placeholder Issues must:
 - Link to the Discussion
 - Have Category = Documentation
 - Have Story Points = 0
 - Have Status = Done

## 11. Governance
### 11.1 Template Ownership
Only Gordon may:

- Modify the Project Template
- Create new projects from the template
- Change fields, views, or automation

### 11.2 Change Control
Changes to the template must be documented in:

```
/standards/project-management-standard.md
```

### 11.3 Versioning
Template versions follow:


```
v1.0 — Initial Release
v1.1 — Field updates
v1.2 — View updates
```

## 12. Repository Structure
Standards documents live in:

```
/standards
   project-management-standard.md
   issue-standards.md
   sprint-standards.md
   documentation-standard.md
   visual-grammar.md
   ```