# Figma File Management

How Wicked projects are set up and organized in Figma. The md files in this kit are the
context; the Figma file is where the work happens. This is how the two connect.

## Every project starts from the Wicked Website Template

Do not start from a blank Figma file. Duplicate the **Wicked Website Template**:
https://www.figma.com/design/SpSd3GSE3SxRiJLUe1RmrF/Wicked-Website-Template

It comes with two libraries attached, the **Relume Figma Kit** and a **Component Library**.
These are a **resource, not the build method**: reach into them for icons, images, and ideas or
inspiration when you need them. They are not where the design comes from.

**Build custom.** Wicked designs are built from scratch, grounded in the client's tokens and
context. That is what keeps them bespoke and off the generic path (see
`../standards/avoid-ai-tells.md`). The template gives you a clean starting file and a place to
grab assets; the design itself is yours to build for this client.

## Setup, per client

1. Duplicate the Wicked Website Template into the client's Figma project.
2. Record the new file link in `work/links.md` (intake requires this).
3. Apply the client's design system: create the client's variables from
   `design-system/tokens.json` (color, type, spacing, radius) in the file, and theme the
   components to them, so the whole file re-skins to the client.

## Building the work

- Build custom sections and components, grounded in `client/` and `design-system/`, following
  `design-process.md` (ground, plan, critique, build).
- Create the client's tokens as Figma variables and bind everything to them, so a token change
  re-themes the whole file.
- Use Relume, the Component Library, unDraw, and Phosphor only to pull in icons, images, or
  inspiration when you need them, not as a substitute for designing.

## Building the full design system

A one-off page is one thing; a professional file is a system. To build the complete design
system (foundations, styles, a full component library with variants and states, sections, a
style guide, a component guide, and page designs), use the `/figma-design-system` skill. It
runs Figma's phased design-system workflow (Discovery, Foundations, File Structure, Components,
QA), grounded in this client's tokens and context. It is a large, staged build, not a one-shot.

## File and page organization

Keep one Figma file per client project, organized into pages:
- **Cover** — project name, client, status.
- **Style guide** — the visual style guide (color, type, spacing, components). Mirrors
  `work/docs/style-guide.md`.
- **Components** — the client's themed components and any custom ones.
- **Pages** — one frame per page or screen (Home, Product, Contact), named semantically.
- **Archive** — superseded explorations, kept out of the way.

## Hygiene (carries into handoff)

Auto Layout on containers, variables for every token, semantic layer names (never "Frame 74"),
component variants for states, flat hierarchy. See `design-process.md` for the full build
rules and `checklist.md` for the pre-handoff gate.

## Fonts and images (realities)

- **Fonts:** the client's licensed faces may not be installed in Figma. Check the available
  fonts, substitute the closest match, and flag the substitution; swap to the licensed faces
  when they are available.
- **Images:** never generate photos. Place the client's real images (raster as fills, SVG icons
  and illustrations as editable vectors) via the Figma asset upload. Until a real asset exists,
  use a labeled placeholder and flag it. See `../standards/images.md`.
- **Nothing hardcoded:** bind every fill, stroke, spacing, and radius to a variable, and use a
  text style for every text. That is what lets the file re-theme and hand off cleanly.
