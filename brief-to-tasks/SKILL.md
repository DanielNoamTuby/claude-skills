---
name: brief-to-tasks
description: Use when a design brief needs an ordered build plan made of independently verifiable vertical slices.
---

# Brief to Tasks

Turn a design brief into a flat, ordered checklist. Each item should include
structure, styling, interaction, and verification rather than splitting those
concerns into separate phases.

## Process

1. Read `DESIGN_BRIEF.md`, `INFORMATION_ARCHITECTURE.md`, and any feature
   token file from `.design/<feature-slug>/`.
2. Explore existing components, views, styles, conventions, tests, and
   dependencies. Mark each relevant component as reuse, modify, or new.
3. Create independently buildable slices that fit one work session.
4. Order them by dependencies, visual priority, and risk.
5. Save `TASKS.md` beside the brief.

## Template

```markdown
# Build Tasks: [Feature/Page Name]

Generated from: .design/<feature-slug>/DESIGN_BRIEF.md
Date: [date]

## Foundation
- [ ] **[Task]** — [what done means]. Reuses: [components/tokens].

## Core UI
- [ ] **[Task]** — [description]. Depends on: [task].

## Interactions & States
- [ ] **[Task]** — [description]. Covers: [hover, loading, error, empty].

## Responsive & Polish
- [ ] **[Task]** — [layout and accessibility checks].

## Review
- [ ] **Design review** — run `design-review` against the brief.
```

Every task must state whether it reuses, modifies, or creates components. The
first build task should establish the chosen aesthetic direction. Keep the
list flat: group by concern, but do not nest more than one level.

Adapted from `designer-skills` by Julian Oczkowski under the Apache License,
Version 2.0. Modified for general use; see `../NOTICE.md`.
