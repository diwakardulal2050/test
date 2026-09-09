# Design System — [CLIENT NAME]

The full design spec for this client. It must be **implementable without the codebase**:
anyone should be able to build a faithful page from this file plus `tokens.json` alone. Keep
the token, the rule, and the reason together so the AI can extrapolate to cases this file
never spelled out.

Replace every [BRACKETED] placeholder. Delete the example rows once real values are in. The
nine sections below are fixed; fill all nine.

---

## 1. Visual theme and atmosphere

One paragraph: the feeling this design should create, grounded in the client and audience
(see `../client/`). Name the concrete subject. Avoid adjectives you cannot check ("premium,"
"clean"); tie the feeling to specific moves.

> Example: [Client] sells [thing] to [audience] who [pain]. The site should feel [specific
> feeling] through [specific moves: a confident wide layout, one warm accent, generous
> whitespace around a single hero statement]. It should not feel [what to avoid].

## 2. Color palette and roles

Semantic roles, not raw hex in the wild. Every color has a job. Values live in `tokens.json`;
this table is the human-readable map. Record the measured WCAG ratio for each text pairing.

| Role | Token | Value | Used for | Contrast |
|---|---|---|---|---|
| Primary action | `color-action-primary` | [#hex] | buttons, primary CTAs | [x:1 on bg] |
| Text default | `color-text-default` | [#hex] | body copy | [x:1 on bg] |
| Background | `color-bg-default` | [#hex] | page background | n/a |
| Feedback success | `color-feedback-success` | [#hex] | success states | [x:1] |

No decorative gradients. Color signals function and state (see `../standards/avoid-ai-tells.md`).

## 3. Typography rules

The type system. Full detail in `typography.md`; the essentials here:
- Display face: [face] for headings.
- Body face: [face] at 16px base, line height [1.5].
- Scale ratio: [1.25 / 1.333 / 1.5].
- A two-font system is required. No lone undifferentiated sans.

## 4. Component stylings (with states)

For each core component, define default plus states. States are not optional.

**Button (primary)**
- Default: [bg, text, padding from scale, radius]
- Hover: [change]
- Focus: [visible indicator, 3:1]
- Disabled: [treatment]

Repeat for: secondary button, input, card, nav link. Add components as the design needs them.

## 5. Layout principles and spacing

- Container: 1280px desktop floor (house rule). Center and pad; step max-width at breakpoints.
- Spacing scale: 8pt base (8/16/24/32/48/64), varied for hierarchy. Do not use one value
  everywhere.
- Grid: [columns, gutter]. Prefer some asymmetry over centered-everything.

## 6. Depth and elevation

Shadow and surface tokens, from flat to raised. Keep the set small and intentional.

| Level | Token | Value | Used for |
|---|---|---|---|
| Flat | `shadow-none` | none | page surface |
| Raised | `shadow-sm` | [value] | cards |
| Overlay | `shadow-lg` | [value] | modals, menus |

## 7. Do's and don'ts

Client-specific, on top of the global `../standards/avoid-ai-tells.md`.
- Do: [client-specific move that is on-brand]
- Do: [another]
- Don't: [client-specific thing to avoid, for example a competitor's look]
- Don't: [another]

## 8. Responsive behavior

- Breakpoints: sm 640, md 768, lg 1024, xl 1280, 2xl 1536.
- Mobile-first. Note any layout that reflows meaningfully (for example nav to hamburger,
  multi-column to stack) and at which breakpoint.
- Touch targets 24px minimum, prefer 44px for primary mobile actions.

## 9. Agent prompt guide

Reusable prompts for building with this system. Fill after the system is set.
- Scaffold a section: "[prompt that references this file and tokens.json]"
- Add a component: "[prompt]"
- Generate a variation: "[prompt that branches from the baseline]"
