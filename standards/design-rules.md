# Design Rules

Global, non-negotiable design norms. These apply to every Wicked project regardless of
client or aesthetic. They are numbers the AI can hit and a human can check. When a design
choice conflicts with a rule here, the rule wins unless `client/` or `design-system/`
overrides it on purpose and says why.

Two kinds of rules live here:
- **Cited norms** — industry-standard values with a source. Follow them by default.
- **House rules** — Wicked's own opinions, labeled as such. Follow them, but know they are
  house preference, not universal law.

---

## Typography

- **Body text: 16px minimum.** 16px is the accessible floor (1rem). Use 16 to 18px on
  desktop, up to 18 to 20px for long-form reading, 14 to 16px on mobile. Never ship body
  copy below 16px.
- **Line height: 1.4 to 1.6 for body.** 1.5 is a safe default. Tighter (1.1 to 1.3) is for
  large headings only.
- **Measure: 50 to 75 characters per line.** Set a `max-width` on text columns to hold this.
  Full-width paragraphs across a 1280px container are a readability failure.
- **Heading scale: a 1.25x to 1.5x step ratio** rooted at the 16px base. Pick one modular
  scale (1.25 "major third", 1.333 "perfect fourth", or 1.5) and use it consistently. Do
  not eyeball heading sizes.
- **Never block user zoom.** No `user-scalable=no`, no `maximum-scale=1`.

## Spacing and layout

- **4/8-point base grid.** All spacing steps come from an 8px base (8, 16, 24, 32, 48, 64)
  with 4px for fine adjustments. Spacing lives in tokens, not in ad-hoc pixel values.
- **Vary spacing to build hierarchy.** The scale exists so you apply *different* steps for
  different relationships. Identical padding on everything is an AI tell (see
  `avoid-ai-tells.md`). Tight groups, generous section breaks.
- **Vary corner radius the same way.** One radius value on every element reads as generated.
  Choose a small set (for example 4px inputs, 8px cards, pill buttons) with intent.

## Responsive

- **Breakpoints (Tailwind de-facto standard):** sm 640px, md 768px, lg 1024px, xl 1280px,
  2xl 1536px. Design mobile-first (`min-width` queries).
- **Container behavior:** center, pad, and step the `max-width` at each breakpoint. Do not
  let content run edge to edge on wide screens.

## House rules (Wicked preference, labeled as such)

- **1280px desktop floor.** Hold a 1280px minimum design width for desktop layouts (1440px
  when chosen). AI defaults to ~1000 to 1100px containers from old training. Never ship
  narrower. This is a house rule, not a widely cited norm, but it is one of the fastest
  ways to stop a site looking dated.
- **No eyebrow-label spam.** Do not stack a tiny label above every large heading, and never
  auto-print the section name as its own eyebrow ("OUR SERVICES" above a Services heading).
  Either cut the eyebrow, or write a real line with personality. House rule.
- **Real assets over generated graphics.** Prefer assets the designer makes in Figma or
  Canva, illustrations from unDraw, and icons from Phosphor (see
  `../client/references/README.md` for links). Do not fake in-page graphics with gradient
  blobs or emoji. Flag any placeholder as a placeholder.

---

### Sources
- Body size / line height / measure: greadme font-size guide; Design Shack responsive
  typography; ScopeDesign UX typography 2025.
- Modular type scale: Design Shack; standard typographic practice.
- Breakpoints: Tailwind CSS responsive docs; Tailkits breakpoints guide.
- 4/8-point grid: common design-system practice (Material, standard token systems).
