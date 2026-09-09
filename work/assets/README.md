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

## Asset status (verified against Figma frame 10479-1744, 2026-09-09)

All design images are now placed. The remaining exports were fetched from Figma via the
one-shot GitHub Actions workflow (.github/workflows/fetch-figma-assets.yml); raw fetches
live in `figma/`, curated copies in `photos/` and `logos/`.

- [x] ICC-IMS logo (1000x260 source) -> logos/logo-icc-ims.png (nav + footer)
- [x] Hero card photos -> photos/hero-state-dots.png, hero-cities-counties.png, hero-aec-firms.png
- [x] Case study photos -> photos/case-arizona-dot.png, case-long-beach.png, case-dfw-airport.png
- [x] 8 remaining agency logos -> logos/logo-*.png (PennDOT, FDOT, WYDOT, ADOT, Moore OK,
      Lancaster TX, Harvard IL, Camden SC). Note: these logo layers export blank from the
      Figma frame itself (empty crop frames); the raw fill sources were fetched instead.
