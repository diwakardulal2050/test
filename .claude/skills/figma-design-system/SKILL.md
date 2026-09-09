---
name: figma-design-system
description: Build a complete, professional design system Figma file for a client — foundations (variables, styles), a full component library with variants and states, sections/patterns, a style guide, a component/usage guide, and page designs. Use when the goal is a real Figma design system, branding + web design system, or "make the professional Figma file", not a single screen.
when_to_use: design system, figma design system, component library, professional figma file, style guide and components, branding system, build the whole design system, foundations and components
---

# Figma Design System Builder (Wicked)

Build the whole thing: a professional design system Figma file a top-tier team could ship
from. Foundations, styles, a full component library, sections, a style guide, a component
guide, and page designs, built to production quality, grounded in this client's context and
tokens. Not one screen. Not a few frames.

## Load these first

This skill defines WHAT a Wicked professional file contains, the Wicked standard, and the
realities of building it. It runs on top of Figma's own build skills, which you MUST load:
- `figma-use` (skill://figma/figma-use/SKILL.md) — Plugin API rules (HOW to call).
- `figma-generate-library` (skill://figma/figma-generate-library/SKILL.md) — the phased
  design-system workflow, the state ledger, variant/scope/code-syntax rules, validation.
  Follow its phase contract, checklists, and the Phase 0 scope-lock exactly.

## Ground it in the client

Read `client/` (brand, audience, brief), `design-system/tokens.json` and
`design-system/design-system.md`, and `standards/`. The client's tokens become the file's
variables. Everything is built **custom** for this client (see `standards/avoid-ai-tells.md`).

## Run it as a phased, resumable build

This is never a one-shot. It is many `use_figma` calls, strictly sequential, across phases and
likely across sessions. Keep a **state ledger on disk** (in the scratchpad:
`design-system-state-{RUN_ID}.json`) with every collection, variable, style, page, and
component ID, and re-read it at the start of each turn. Log milestones to `work/log.md`.

- **Phase 0 — Discovery + scope lock.** Read the context. `get_libraries` + inspect the file.
  Lock the exact v1 component and section list with the designer (a brochure site needs less
  than a store). Print the locked scope. No writes yet.
- **Phase 1 — Foundations.** Build the token architecture below. Validate: 0 broken aliases,
  every semantic variable scoped, every variable code-syntaxed, all planned styles present.
- **Phase 2 — File structure + foundations docs.** Build the page skeleton, then the
  foundations pages (color swatches, type specimens, spacing bars, elevation). Screenshot.
- **Phase 3 — Components, one at a time.** For each: own page, base component with auto-layout
  bound to variables (nothing hardcoded), all variants (`combineAsVariants` + grid layout),
  component properties (TEXT/BOOLEAN/INSTANCE_SWAP), states, usage docs on the page. Validate
  each with `get_metadata` + `get_screenshot`. Atoms before molecules before organisms.
- **Phase 4 — Patterns, guides, QA.** Build the sections/patterns and the guides. Audit
  contrast, target sizes, naming, and unresolved bindings. Migrate any hardcoded earlier work
  onto the tokens.

## The Wicked token architecture (Phase 1)

Proven, concrete. Adapt the values per client; keep the structure. Full scope table and script
patterns in `references/token-architecture.md`.

- **Primitives** (1 mode "Value", `scopes = []` so they stay hidden): a neutral ramp
  (0 to 1000), the brand/accent ramp (the client's signature), and functional colors
  (green/red/amber/blue at 100 + 500). Code syntax `var(--color-...)`.
- **Color** (modes Light + Dark, every value aliased to a primitive): `bg/*`, `text/*`,
  `border/*`, `action/*`, `feedback/*` (+ subtle). Scope per role (backgrounds
  FRAME_FILL+SHAPE_FILL, text TEXT_FILL, borders STROKE_COLOR). Code syntax on all.
- **Spacing** (Value): `0, xs, sm, md, lg, xl, 2xl, 3xl, 4xl` on a 4/8 base. Scope GAP + WIDTH_HEIGHT.
- **Radius** (Value): `none, sm, md, lg, full`. Scope CORNER_RADIUS.
- **Typography Primitives** (Value): `family/{display,body}` (FONT_FAMILY),
  `weight/{regular,medium,semibold}` (FONT_STYLE), `size/{xs..4xl}` (FONT_SIZE).
- **Text styles**: Display/XL, Display/L, Heading/H1-H3, Body/Large-Small, Label/Tag, Caption.
- **Effect styles**: Shadow/Subtle, Shadow/Medium, Shadow/Strong.
- **Color styles**: semantic paint styles bound to the color variables (Background, Text,
  Border, Action, Feedback), for designers who work from the styles panel.

## Page structure (Phase 2)

Group the pages with separator pages so the sidebar stays legible:

```
Cover, Getting Started,
——— System ———,    Foundations, Components, Patterns,
——— Reference ———, Style Guide, Component Guide,
——— Delivery ———,  Screens, Archive
```

Put all components on a single `Components` page (each as a labeled section) for small or demo
systems; use a page per component only for a large library where one page gets unwieldy. Order
the pages with `figma.root.insertChild(index, page)`.

## The component set (Phase 3)

Right-sized in Phase 0. The full menu for a web project:
- Atoms: Button, Link, Icon, Input, Textarea, Select, Checkbox, Radio, Toggle, Badge, Avatar,
  Divider
- Molecules: Form field, Card, Alert, Tooltip, Breadcrumb, Pagination, Tabs, Accordion
- Organisms: Navbar, Footer, Modal

Sections/patterns: Hero, Feature row, Testimonial, Pricing, CTA band, FAQ, Logo cloud, Stats,
Contact/Newsletter, plus anything the client's site needs.

## The two guides are deliverables

- **Style Guide page** — foundations + key components at a glance, bound to variables
  (`/style-guide` covers its content).
- **Component Guide** — per component: anatomy, variants, states, usage, when-NOT-to-use,
  do/don't, accessibility. Mirror to `work/docs/components/` via `/component-spec`.

## Realities (learned, non-negotiable)

- **Build custom.** Relume, the Component Library, unDraw, and Phosphor are a resource for
  icons, images, and inspiration only, not the build method.
- **Fonts.** The client's licensed faces may not be installed (for example Ogg, Neue Haas
  Grotesk). Check with `listAvailableFontsAsync`, substitute the closest available (for example
  DM Serif Display, Inter), and **flag the substitution**; swap to the licensed faces later.
- **Images.** Never generate photos. Place the client's real images with `upload_assets`
  (raster as fills, SVG as editable vectors). Until a real asset exists, use a labeled
  placeholder and flag it. See `standards/images.md`.
- **Nothing hardcoded.** Every fill, stroke, spacing, and radius binds to a variable; every
  text uses a text style. That is what makes the file re-theme and hand off cleanly.
- **Accessibility.** Verify contrast, 24px targets, and focus per `standards/accessibility.md`.
