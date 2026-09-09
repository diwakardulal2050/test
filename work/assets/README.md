# Assets

Exported and produced assets for this project: images, icons, illustrations, and any source
files. This is output, not reference. (Reference material the client gave you, like their
logo or competitor screenshots, lives in `client/references/`.)

## Naming

Descriptive, lowercase, hyphenated: `[what]-[variant].[ext]`. For example
`hero-roasting.jpg`, `icon-wholesale.svg`, `logo-export-white.png`. The AI reads these names,
so make them mean something.

## What belongs here

- Final exports headed for the build (optimized images, SVG icons).
- Custom illustration or graphics you produced.
- Source files for produced assets, if you want them with the project.

Prefer real assets over generated graphics (see `../../standards/avoid-ai-tells.md`). For
stock-free sources: unDraw for illustration, Phosphor for icons (linked in
`../../client/references/README.md`).

## Missing assets checklist (verified against Figma frame 10479-1744, 2026-09-09)

Export these from the Figma file (select the layer, Export → PNG) and add them to the repo;
this environment cannot download Figma exports directly (egress policy). Node links use
https://www.figma.com/design/jdzMJkmpGq91Lw07mU6pmH/ICC-IMS--Copy-?node-id=NODE

- [ ] ICC-IMS logo (layer "image 2", 1000x260, node 10479-1764) — used in nav and footer;
      the prototype currently uses an SVG recreation
- [ ] Hero card photo — State DOTs (inside node 10479-1797)
- [ ] Hero card photo — Cities & Counties (inside node 10479-1806)
- [ ] Hero card photo — AEC Firms (inside node 10479-1814)
- [ ] Case study photo — Arizona DOT highway (layer "Rectangle 4755" inside node 10479-2116)
- [ ] Case study photo — Long Beach street (layer "Rectangle 4756" inside node 10479-2127)
- [ ] Case study photo — DFW night collection (layer "Rectangle 4757" inside node 10479-2138)
- [ ] Re-export 7 blank logos (came through as empty 219-byte PNGs): PennDOT, FDOT, WYDOT,
      Moore OK, Lancaster TX, Harvard IL, Camden SC (nodes 10479-1825/1826/1827/1838/1839/1840/1841)

Already placed: What We Do van (Vector 6), Who We Are crew (Rectangle 47581), the three
pillar photos (Rectangle 4755, -1, -2), and 10 agency logos.
