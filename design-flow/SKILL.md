---
name: design-flow
description: Use when a new feature or product needs a guided design-to-build process, or when the user asks for a complete design workflow.
---

# Design Flow

Guide the designer through these phases in order:

1. **Grill Me** → clarify the idea
2. **Design Brief** → capture intent
3. **Information Architecture** → define structure
4. **Design Tokens** → establish the visual system
5. **Brief to Tasks** → plan buildable slices
6. **Frontend Design** → build the interface
7. **Design Review** → review the result separately

## Rules

1. At the start, show the sequence and ask which phases to skip. A clear idea
   may skip grilling; a single component may skip information architecture; an
   established token system may skip token generation.
2. Before each phase, state what it produces.
3. Invoke the corresponding skill and follow its full instructions.
4. After each phase, summarize its output, decisions, and open questions.
   Confirm before continuing.
5. Check whether each phase changes the next one. Tokens should follow the
   brief's chosen direction; tasks should follow the resulting structure.
6. The designer may stop at any phase. State what is complete and what comes
   next.

The review phase is separate and requires built work. Do not run it
automatically when nothing exists to inspect.

## Returning to an unfinished flow

Look for the feature's existing design documents, identify the next incomplete
phase, and ask which feature to resume if more than one exists. Keep all
artifacts in the same `.design/<feature-slug>/` folder:

```
.design/<feature-slug>/
├── DESIGN_BRIEF.md
├── INFORMATION_ARCHITECTURE.md
├── TASKS.md
├── DESIGN_REVIEW.md
└── screenshots/
```

Adapted from `designer-skills` by Julian Oczkowski under the Apache License,
Version 2.0. Modified for general use; see `../NOTICE.md`.
