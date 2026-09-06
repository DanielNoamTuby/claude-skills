---
name: design-brief
description: Use when a feature, page, or product idea needs its user problem, experience direction, constraints, and scope captured before implementation.
---

# Design Brief

Create a shared design intent document for a feature or page. This is a design
brief, not an implementation work order.

## Process

1. Ask what is being built, who it is for, and what constraints or ideas
   already exist.
2. Explore the project: tokens, themes, components, layouts, routes, fonts,
   dependencies, and existing pages. Extend its vocabulary rather than
   replacing it.
3. Interview until these decisions are clear:
   - primary user and job to be done;
   - success criteria;
   - emotional tone and anti-references;
   - device, accessibility, performance, and brand constraints;
   - real versus placeholder content;
   - important interaction and failure states.
4. Save the result as `DESIGN_BRIEF.md` in a short, lowercase,
   hyphenated feature folder such as `.design/settings-page/`.

## Template

```markdown
# Design Brief: [Feature/Page Name]

## Problem
[The user's friction, not the technical or business problem.]

## Solution
[The experience that resolves it.]

## Experience Principles
1. [Principle] — [what it means in practice]
2. [Principle] — [what it means in practice]
3. [Principle] — [what it means in practice]

## Aesthetic Direction
- **Philosophy**: [named philosophy or described vibe]
- **Tone**: [emotional register]
- **Reference points**: [what it should feel like]
- **Anti-references**: [what it must not feel like]

## Existing Patterns
- Typography: [current conventions]
- Colors: [current tokens]
- Spacing: [current scale]
- Components: [reused or extended components]

## Component Inventory
| Component | Status | Notes |
| --- | --- | --- |
| [name] | Exists / Modify / New | [detail] |

## Key Interactions
[Actions, state changes, transitions, and feedback.]

## Responsive Behavior
[How layout and behavior adapt across supported sizes.]

## Accessibility Requirements
[Contrast, keyboard access, labels, focus, semantics, and motion.]

## Out of Scope
[Specific exclusions that prevent scope creep.]
```

Do not put project-specific implementation rules into a reusable brief skill.
Record those rules in the project's own contributing or agent guidance.

Adapted from `designer-skills` by Julian Oczkowski under the Apache License,
Version 2.0. Modified for general use; see `../NOTICE.md`.
