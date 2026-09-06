---
name: information-architecture
description: Use when a product or feature needs its navigation, content hierarchy, page structure, naming, or user flows defined before visual design or implementation.
---

# Information Architecture

Define the structural skeleton between the design brief and the build. Extend
the project's existing routes, navigation, layouts, content models, and naming
conventions rather than inventing a parallel structure.

## Process

1. Read the feature's `DESIGN_BRIEF.md` from `.design/<feature-slug>/`.
2. Explore existing routing, navigation, layouts, page directories, URL
   patterns, content models, and data boundaries.
3. Resolve:
   - the primary things users need to find or do, ranked by frequency;
   - acceptable navigation depth;
   - content that grows over time;
   - distinct user types and entry points;
   - the view where users spend most of their time.
4. Save `INFORMATION_ARCHITECTURE.md` beside the brief.

## Template

```markdown
# Information Architecture: [Product/Site Name]

## Site Map
- Home `/`
  - Feature `/feature`
    - Detail `/feature/detail`
- Settings `/settings`

## Navigation Model
- **Primary navigation**: [items and maximum count]
- **Secondary navigation**: [sidebars, tabs, and contextual links]
- **Utility navigation**: [account, settings, help]
- **Mobile navigation**: [drawer, bottom tabs, or other adaptation]

## Content Hierarchy
### [Page Name]
1. [Highest-priority content] — [rationale]
2. [Second priority] — [rationale]
3. [Below the fold / secondary content]

## User Flows
### [Flow Name]
1. User lands on [page].
2. User sees [content or prompt].
3. User takes [action].
   - If [condition] → [outcome].
4. User arrives at [destination].

## Naming Conventions
| Concept | Label in UI | Notes |
| --- | --- | --- |
| [thing] | [term] | [reason] |

## Component Reuse Map
| Component | Used on | Behavior differences |
| --- | --- | --- |
| [component] | [pages] | [variations] |

## Content Growth Plan
[Pagination, filtering, search, archive, or other growth strategy.]

## URL or State Strategy
- Pattern: [URL or view-state pattern]
- Dynamic segments: [parameterized values]
- Query/state: [filters, sorting, pagination, or local state]
```

If the product has no URLs, replace the site map with a destination or screen
map and describe the state boundaries explicitly.

Adapted from `designer-skills` by Julian Oczkowski under the Apache License,
Version 2.0. Modified for general use; see `../NOTICE.md`.
