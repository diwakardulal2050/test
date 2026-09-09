---
name: handoff
description: Generate a developer handoff and redline package (final states, spacing and type and color redlines, token references, production assets list, copy deck, accessibility notes) for a page or component at the design-to-dev transition. Use for handoff, redlines, or a developer spec.
when_to_use: handoff, dev handoff, redlines, developer spec, ready for development, handoff package, build spec
paths:
  - "work/**"
  - "design-system/**"
---

# Handoff Generator

Produce the package a developer needs to build the design pixel-accurate, without asking
questions. Modern Figma Dev Mode auto-generates a lot of this, so do not re-type what the tool
already shows; capture the information the build needs and the decisions the tool cannot see.

## Ground first (required)

- Read the final Figma frames via the MCP (`get_design_context`, `get_variable_defs`).
- Read `design-system/tokens.json`, the relevant `work/pages/<page>.md`, and
  `standards/accessibility.md`.
- Note any Code Connect mappings so the build uses the client's real components.

## Output structure

Write to `work/docs/handoff-<page-or-component>.md`. Spec unique elements and their variations
only. Do not repeat identical components; point at their component spec instead.

1. **Scope** — what this covers and the source Figma link.
2. **All states** — the final mockups for every state (empty, loading, error, success).
3. **Redlines** — spacing, sizing, and type (family, size, weight, line-height), as token
   references where possible, raw values where not.
4. **Color** — values used, by token.
5. **Production assets** — the SVGs and images to export, with names and any @2x/@3x needs.
6. **Behavior** — a prototype link, and any interaction logic the visuals do not show.
7. **Copy deck** — the real copy, per element.
8. **Component and token references** — links to the relevant specs.
9. **Accessibility notes** — keyboard order, focus, contrast, target sizes, ARIA.

## Rules

- Everything references tokens, not stray values, wherever a token exists.
- Record the handoff link in `work/links.md` and append a `[progress]` line to `work/log.md`.
