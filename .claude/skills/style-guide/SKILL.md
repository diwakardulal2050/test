---
name: style-guide
description: Generate the client's visual style guide (logo usage, color roles, typography, spacing, key components, imagery, do's and don'ts) grounded in the project's real design tokens and brand. Use when the designer asks for a style guide, brand style sheet, or visual guidelines.
when_to_use: style guide, visual guidelines, brand style sheet, color and type reference, design standards doc
paths:
  - "design-system/**"
  - "client/**"
---

# Style Guide Generator

Produce a reference style guide anyone can use to make on-brand material for this client. It
must be bespoke, not templated. A style guide that quotes this brand's actual hex values, real
type, and real component names reads as authoritative; a generic one is worthless.

## Ground first (required)

Read the real inputs before writing a word:
- `design-system/tokens.json` and `design-system/tokens.css` (the actual values)
- `design-system/design-system.md` and `design-system/typography.md`
- `client/brand.md` (logo, imagery, voice)
- `standards/` (accessibility numbers, the anti-tells, voice)

If tokens are still the example defaults or `[BRACKETED]` placeholders, stop and say the style
guide would be generic. Fill the design system first (run intake), then come back.

## Output structure

Write to `work/docs/style-guide.md`. Every section explains *when and why*, and includes a
"when not to" where it applies, not just what it looks like.

1. **Overview** — who this brand is in two lines, and how to use this guide.
2. **Logo** — usage, clear space, minimum size, misuse (paired do/don't).
3. **Color** — each role with its token name, exact hex, what it is for, and its measured WCAG
   ratio. Call out that decorative gradients are not used.
4. **Typography** — the two-font system, the scale and ratio, line-heights, the 16px body floor.
5. **Spacing and layout** — the 8pt scale, the 1280px desktop floor, the rule to vary spacing.
6. **Key components** — the site's real components with their states.
7. **Imagery and iconography** — the photography/illustration style and icon source.
8. **Do's and don'ts** — the client-specific ones plus the relevant global anti-tells, paired.

## Also render it in Figma (when a project file exists)

The markdown is the reference; a visual style guide page is the companion. When the project has
a Figma file (see `work/links.md`), offer to build a **Style guide page** in it, themed to the
client's variables:
- Color swatches, each labeled with the token name, hex, and role.
- The type scale, each tier shown at size with its name and specs.
- The spacing scale, shown as blocks.
- The live components (button and its states, and any others), as instances.

Build it on the file's "Style guide" page (see `workflow/figma-files.md`), using Auto Layout
and bound variables so it re-themes if a token changes.

## Rules

- Quote real values from `tokens.json`. Never invent a color or restate a placeholder.
- Obey `standards/voice-guide.md` in the prose (no em dashes, no filler).
- Offer to also emit an HTML version (`work/docs/style-guide.html`) if the designer wants a
  shareable page.
- Append a short `[progress]` line to `work/log.md` when done.
