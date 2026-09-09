# Token Architecture (Wicked, proven)

The exact Phase 1 foundation, verified working. Adapt the values to the client; keep the
structure, names, scopes, and code syntax. Build in this order, one `use_figma` call per step,
validating after. Full API patterns live in `figma-generate-library`'s `token-creation.md`;
this file is the Wicked-specific plan. The numbers below are Wicked defaults; the client's real
token values live in `design-system/tokens.json` and are what you build into these variables
(see `design-system/README.md` for the mapping).

## Collections and modes

| Collection | Modes | Holds |
|---|---|---|
| Primitives | `Value` | raw color ramps |
| Color | `Light`, `Dark` | semantic colors, aliased to primitives |
| Spacing | `Value` | spacing floats |
| Radius | `Value` | radius floats |
| Typography Primitives | `Value` | families, weights, sizes |

Dark mode needs a Professional plan or higher (the Wicked account qualifies).

## Primitives (scopes = [], hidden from pickers)

- **Neutral ramp** `neutral/0 … neutral/1000` — warm-neutral, from the paper tone to the ink
  tone to pure black. About 12 steps.
- **Brand/accent ramp** — the client's signature color, roughly 5 steps (for example a warm `clay/100…500` ramp).
- **Functional** — `green/{100,500}`, `red/{100,500}`, `amber/{100,500}`, `blue/{100,500}`.

Code syntax: `var(--color-neutral-500)` etc.

## Color (semantic, aliased Light/Dark, scoped)

| Token | Light → primitive | Dark → primitive | Scopes |
|---|---|---|---|
| `color/bg/default` | neutral/50 | neutral/900 | FRAME_FILL, SHAPE_FILL |
| `color/bg/surface` | neutral/0 | neutral/800 | FRAME_FILL, SHAPE_FILL |
| `color/bg/subtle` | neutral/100 | neutral/700 | FRAME_FILL, SHAPE_FILL |
| `color/bg/inverse` | neutral/900 | neutral/50 | FRAME_FILL, SHAPE_FILL |
| `color/bg/accent` | accent/300 | accent/400 | FRAME_FILL, SHAPE_FILL |
| `color/text/default` | neutral/900 | neutral/50 | TEXT_FILL |
| `color/text/muted` | neutral/500 | neutral/400 | TEXT_FILL |
| `color/text/inverse` | neutral/0 | neutral/900 | TEXT_FILL |
| `color/text/on-accent` | neutral/900 | neutral/900 | TEXT_FILL |
| `color/border/default` | neutral/200 | neutral/700 | STROKE_COLOR |
| `color/border/strong` | neutral/300 | neutral/600 | STROKE_COLOR |
| `color/action/primary` | neutral/900 | neutral/0 | FRAME_FILL, SHAPE_FILL |
| `color/action/primary-hover` | neutral/1000 | neutral/100 | FRAME_FILL, SHAPE_FILL |
| `color/action/on-primary` | neutral/0 | neutral/900 | TEXT_FILL |
| `color/feedback/{success,danger,warning,info}` | the 500 | the 500 | SHAPE_FILL, STROKE_COLOR |
| `color/feedback/{...}-subtle` | the 100 | neutral/800 | FRAME_FILL, SHAPE_FILL |

Alias, never duplicate raw values. Code syntax `var(--color-bg-default)` etc.

## Spacing (scope GAP, WIDTH_HEIGHT) and Radius (scope CORNER_RADIUS)

- Spacing: `0=0, xs=4, sm=8, md=16, lg=24, xl=32, 2xl=48, 3xl=64, 4xl=96`.
- Radius: `none=0, sm=4, md=6, lg=12, full=9999` (Wicked defaults; use the client's `tokens.json` values).

## Typography Primitives

- `family/display` (FONT_FAMILY) = the display face (or its available substitute).
- `family/body` (FONT_FAMILY) = the body face (or substitute).
- `weight/{regular,medium,semibold}` (FONT_STYLE) = the exact Figma style strings.
- `size/{xs=12, sm=14, md=16, lg=18, xl=24, 2xl=36, 3xl=54, 4xl=80}` (FONT_SIZE).

## Text styles (type ramp)

Display/XL (display 80), Display/L (display 54), Heading/H1 (display 36),
Heading/H2 (body semibold 28), Heading/H3 (body semibold 22), Body/Large (body 18),
Body/Medium (body 16), Body/Small (body 14), Label/Tag (body semibold 13, +letter-spacing),
Caption (body 13). Load fonts before creating.

## Effect styles

Shadow/Subtle (0 1px 2px 5%), Shadow/Medium (dual, ~8% + 5%), Shadow/Strong (dual, ~10% + 5%).
Keep light for editorial brands.

## Color styles

Also create semantic color paint styles bound to the semantic variables, for designers who work
from the styles panel. Name by role in folders: `Background/*`, `Text/*`, `Border/*`,
`Action/*`, `Feedback/*`. Each style's paint is bound to the matching `color/*` variable, so the
variables stay the single source of truth (the styles resolve through them, including Light/Dark).

## Validate before Phase 2

- Every planned collection exists with the right modes.
- Primitives: `scopes = []`, code syntax set.
- Semantic: targeted scopes, code syntax, aliases resolve (0 broken).
- All text and effect styles present.
- No `ALL_SCOPES` anywhere.
