---
name: frontend-design
description: Use when building a frontend interface that needs a deliberate, distinctive visual direction instead of generic styling.
---

# Frontend Design

Build working frontend code with careful attention to hierarchy, composition,
states, accessibility, and visual detail.

## Before coding

1. Explore existing components, tokens, themes, fonts, layouts, dependencies,
   and responsive conventions. Extend matching patterns instead of duplicating
   them.
2. Understand the problem, audience, tone, constraints, and content.
3. Choose and state an aesthetic direction before implementation.

## Aesthetic directions

### Dieter Rams / Functionalist
Less but better: clean sans-serif type, restrained color with one functional
accent, strict grid, mathematical spacing, minimal purposeful motion, and
precise borders.

### Swiss / International Typographic
Objective structure: strong sans-serif type, high contrast, rigid columns,
clear rules, dramatic hierarchy, and no decorative gradients or shadows.

### Japanese Minimalism
Negative space as content: muted naturals, quiet typography, balanced
asymmetry, generous margins, hairline borders, and slow opacity transitions.

### Brutalist / Raw
Visible structure: system or monospace type, stark or clashing flat color,
exposed borders, compressed or uneven spacing, and hard-cut interactions.

### Scandinavian
Warm functional restraint: approachable type, natural palette, open layout,
consistent rounded corners, generous spacing, and gentle motion.

### Art Deco / Geometric
Formal symmetry: geometric display type, deep rich color, centered structure,
architectural spacing, and precise decorative geometry.

### Neo-Memphis
Playful disruption: mixed type, bold clashing color, broken grids, overlapping
shapes, thick borders, and intentionally bouncy motion.

### Editorial / Magazine
Content-led composition: expressive display type, clean body text, strong
columns, full-bleed imagery, thin rules, captions, and generous margins.

## Implementation

- Use semantic CSS variables for repeated visual decisions.
- Match implementation complexity to the chosen direction.
- Build every meaningful state: default, hover, focus, active, disabled,
  loading, empty, error, and success where applicable.
- Keep touch targets at least 44×44px and body text readable.
- Use the existing theme mechanism, with intentional light and dark palettes.
- Respect reduced-motion preferences.
- Avoid generic AI styling: purple gradients on white, arbitrary card grids,
  and unconsidered default typography.

Adapted from `designer-skills` by Julian Oczkowski under the Apache License,
Version 2.0. Modified for general use; see `../NOTICE.md`.
