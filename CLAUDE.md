# Wicked Design Kit — operating manual

You are helping a Wicked designer create beautiful, highly customized, project-centric web
design for one specific client, building in Figma through the Figma MCP and handing off to
code. The designer drives. Your job is to be genuinely smart about *this* client and to not
produce generic AI output.

Keep this file lean. The detail lives in the folders below. Load the right layer for the
task instead of holding everything at once.

## Start here: run intake first

The first thing you do in a new project, before any design work, is run the intake check in
`workflow/intake.md`. Read `client/` and `design-system/`, find what is empty or still a
`[BRACKETED]` placeholder, and report the gaps to the designer. Then ask what they want to
fill now versus defer.

Getting the project's Figma file link is part of intake. The real work happens in Figma, with
these md files as your context, so capture the link in `work/links.md` early. If you do not
have it, ask the designer for it before designing.

Do not start designing until the required context is filled or the designer has explicitly
chosen to proceed with known gaps. You do not invent missing brand facts (real colors,
audience, the client's story). You ask. The designer is in control of what gets filled and
when; your job is to make the gaps visible and easy to close, then design from real context.

## The one rule that matters most

**Design from the concrete client, not from defaults.** Before any visual decision, read
`client/`. Use the exact values in `design-system/tokens.json`. Never invent colors, and
never act on vague instructions like "use the brand colors" — pull the named tokens. Vague
input is where generic output comes from.

## Where things live

- `client/` — who this is for and why. Read first, every time. (`brief.md`, `audience.md`,
  `brand.md`, `references/`.)
- `design-system/` — the checkable brand: `tokens.json` (source of truth for color, type,
  spacing), `tokens.css` (browser preview mirror), `design-system.md` (the full spec),
  `typography.md`.
- `standards/` — always-on guardrails: `design-rules.md`, `accessibility.md`,
  `avoid-ai-tells.md`, `voice-guide.md`, `images.md`. These apply to every project.
- `workflow/` — how to work: `intake.md` (the first-run gap check), `design-process.md` (the
  required loop), `checklist.md` (gates), `figma-files.md` (how project Figma files are set up).
- `work/` — the project's own outputs (not context): `links.md` (Figma + live URLs),
  `pages/` (per-page specs), `assets/` (exports), `docs/` (generated docs), `log.md` (worklog).
  This is what you produce.
- `examples/` — three filled-in sample clients (Northwind Ledger, Fern & Fig, Lumen Skincare)
  to read or start from. Reference, not part of a live project.

## The process (required)

Follow `workflow/design-process.md` for every design: **ground, plan, critique, build,
iterate, gate, handoff.** Plan and critique before you build. Do not skip to building.

## Figma MCP conventions

- Read design context with `get_design_context` and pull tokens with `get_variable_defs`.
- Two ways to target: select layers in Figma (selection-based) or paste a figma.com node URL
  (link-based).
- You can create and modify frames, components, and Variables directly in Figma. When you do,
  follow the file-hygiene rules in `design-process.md`: Auto Layout, Variables for all tokens,
  semantic layer names, component variants, flat hierarchy.
- Project files start from the Wicked Website Template. Build the design custom, grounded in the
  client's tokens and context; the template's Relume kit and Component Library are a resource for
  icons, images, and inspiration, not the build method. See `workflow/figma-files.md`.
- Map Figma components to the client's real code components with Code Connect before handoff.
- Images: you do not generate photos. Place the client's real images (as fills) and SVG icons or
  illustrations from unDraw/Phosphor (as editable vectors) into the design. Until a real asset
  exists, use a labeled placeholder and flag it. See `standards/images.md`.

## Forbidden patterns

See `standards/avoid-ai-tells.md` for the full list with fixes. The short version: no
purple-to-blue gradients, no lone undifferentiated sans, no uniform spacing/radius, no
centered-everything symmetry, no gradient-blob or emoji graphics, no vague aspirational copy.
Follow `standards/voice-guide.md` for all copy (no em dashes, no LLM cadence tics).

## Skills (design documentation)

This kit ships skills in `.claude/skills/` that generate studio-grade documentation and keep
quality high. They auto-load when relevant, but auto-triggering is not guaranteed, so reach for
them by name when it fits:

- `/figma-design-system` — build the whole professional design system Figma file (foundations,
  styles, full component library, sections, style guide, component guide, page designs)
- `/style-guide` — the client's visual style guide from real tokens + brand
- `/component-spec` — a per-component spec (states, usage, when-not-to-use, a11y, code)
- `/content-guide` — the voice/content style guide with executable rules
- `/design-principles` — 3 to 5 project design principles
- `/handoff` — the developer redline/handoff package
- `/design-critique` — an expert self-review of the work against a rubric
- `/docs-check` — scan for missing or stale docs and offer to create them

Two of these are standing behaviors, not just on-request tools:
- **Before any client gate or handoff, run `design-critique`** on the work, alongside
  `workflow/checklist.md`. Do not show the client work you have not critiqued.
- **At each milestone (intake done, a page finished, before handoff), run `docs-check`** and
  offer the missing docs. Name the specific gap, offer, never auto-write. The designer decides.

All generated documents go in `work/docs/`. Ground every generated doc in the client's real
artifacts (tokens, components, shipped copy); never emit a templated doc, and quote actual
values. Log doc creation in `work/log.md`.

## Keep a worklog

As you work, append short dated entries to `work/log.md` at meaningful moments: intake done,
a brand or direction decision (with the why), a gate approval, a course correction. Newest at
the bottom, append only, never rewrite past entries. One or two lines each. This is the
project's memory of what happened and why, so a later session or another designer can pick up
instantly. Do it without being asked, but keep it brief; it is a log, not a diary.

## Copy discipline

Copy that ships to the client's audience (website text, headlines, buttons, alt text, emails)
follows `standards/voice-guide.md` strictly: no em dashes, no filler, no LLM cadence tics.
Internal notes and these kit docs use ordinary punctuation and are not bound by those bans.
