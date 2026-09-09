---
name: component-spec
description: Generate a per-component specification (anatomy, variants, states, usage and when-not-to-use, props and API, accessibility, responsive behavior, code) grounded in the real component in Figma or the codebase. Use when documenting a component or building the component library.
when_to_use: component spec, component documentation, document this component, component library, button spec, input spec, card spec
paths:
  - "design-system/**"
  - "src/components/**"
  - "work/**"
---

# Component Spec Generator

Document one real component to a standard a developer can build from without guessing. Ground
it in the actual component, not a hypothetical one.

## Ground first (required)

- Read the real component: from Figma via the MCP (`get_design_context`, `get_variable_defs`)
  or from the codebase if it exists.
- Use its real name, real variants, and the real tokens it consumes (`design-system/tokens.json`).
- Derive the do's and don'ts from misuse you actually observe in the file, not invented cases.

If the component does not exist yet, say so; this skill documents built components, it does not
design new ones.

## Output structure

Write to `work/docs/components/<component-name>.md`. Per-component fields:

1. **Name and description** — what it is, in one line.
2. **Anatomy** — the labeled sub-parts.
3. **Variants** — the real variants.
4. **States** — default, hover, focus, active, disabled, loading, error, empty (those that apply).
5. **Usage** — when to use, and explicitly **when NOT to use** (reach for X instead).
6. **Do's and don'ts** — paired examples.
7. **Props / API** — name, type, required or optional, default.
8. **Behavior** — interaction and events.
9. **Accessibility** — keyboard nav, screen-reader behavior, contrast, focus order, ARIA.
10. **Responsive** — how it reflows.
11. **Code** — a real snippet.
12. **Related components** and a short **changelog**.

## Rules

- The "when NOT to use" and accessibility sections are not optional. They are what separate a
  real spec from a screenshot.
- Obey `standards/accessibility.md` and `standards/voice-guide.md`.
- Append a `[progress]` line to `work/log.md` when done.
