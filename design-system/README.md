# Design System

Two things live here, and they are not competing sources of truth.

- **`tokens.json`** is the client's design tokens in DTCG format: the portable source you
  author per client (color, spacing, type, radius, elevation). `tokens.css` mirrors it for
  browser preview. `design-system.md` is the human-readable spec, and `typography.md` details
  the type system.
- **The Figma variable architecture** is how those tokens become Figma variables when you build
  the design system with `/figma-design-system`. The structure (Primitives, then semantic Color
  with Light and Dark, then Spacing, Radius, Typography, plus text and effect styles) is
  documented in `.claude/skills/figma-design-system/references/token-architecture.md`.

## Which is canonical

`tokens.json` holds the client's real values. `token-architecture.md` documents the Wicked
default structure and naming for expressing them in Figma. Keep the two in sync: if a value
changes, change it in `tokens.json` and rebuild the affected variables. The example values in
both files are illustrative. Replace them with the client's real tokens.

## Naming map (DTCG to Figma)

The names map directly:

| DTCG (`tokens.json`) | Figma variable |
|---|---|
| `action-primary` | `color/action/primary` |
| `text-default` | `color/text/default` |
| `bg-default` | `color/bg/default` |
| `space.3` / `space-md` | `spacing/md` |
| `radius.md` | `radius/md` |
| `font.size.lg` | `size/lg` |

The scales (type ratio, spacing steps, radius set) are Wicked defaults; hold one scale
consistently across both files for a given client.
