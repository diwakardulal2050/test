# Images and Assets

How images work in this kit. Images are where AI design most often gives itself away, so the
rules here are strict.

## The core rule

**The AI does not generate photographs or fake illustration.** It builds layout, type, color,
and components. Generic AI imagery (stock-style photos, plastic AI illustration, gradient
blobs) is one of the clearest AI-tells (see `avoid-ai-tells.md`). Real images carry the brand;
the design holds space for them.

## Where images come from (in order of preference)

1. **The client's real assets** — product photos, team photos, real brand imagery. This is the
   best material and the main source of distinctiveness. Source files go in
   `client/references/`; exports headed for the build go in `work/assets/`.
2. **Custom graphics the designer makes** in Figma or Canva.
3. **unDraw** (https://undraw.co) for friendly illustration and **Phosphor**
   (https://phosphoricons.com) for icons, as SVG, when custom art is not available.

## Placeholders

Until a real asset exists, use a clearly labeled placeholder in the design (as with the Lumen
product block). A placeholder is honest and temporary. Never ship one to a client without
flagging it, and never fake an image with a gradient shape or an emoji.

## Getting images into Figma

The pipeline exists and the AI can drive it:
- **Real photos (PNG, JPG, WebP)** are placed as fills on the target node.
- **SVGs (unDraw, Phosphor)** import as editable vector layers.

The AI places assets the designer provides or points to; it does not invent them. When you drop
real photography into `work/assets/` or `client/references/`, ask it to place them and it will
swap the placeholders for the real thing.

## Accessibility

Every meaningful image needs alt text. Decorative images are marked as decorative. Capture the
alt text in the page spec and the handoff so the build inherits it (see `accessibility.md`).
