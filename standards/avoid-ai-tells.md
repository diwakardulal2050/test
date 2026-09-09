# Avoid AI Tells

The recurring giveaways that make a site read as "made by AI." Each entry is the tell, why
it happens, and the fix. Run a design against this list before it goes to a client (see
`../workflow/checklist.md`). If a design trips three or more of these, it is generic. Rework it.

The goal is not novelty for its own sake. It is a design that looks like it was made *for
this client* by someone with taste, not assembled from defaults.

---

## Layout

1. **Centered-everything symmetry.** AI defaults to one centered column, everything
   balanced, grid-locked. Fix: use asymmetry, off-center anchors, and deliberate
   grid-breaking. Let one element sit where it is not "expected."
2. **Too-narrow desktop containers.** ~1000 to 1100px containers read as dated. Fix: hold
   the 1280px floor (see `design-rules.md`).
3. **Uniform spacing and radius.** Identical 24px padding on every block, one 16px radius
   everywhere, equal card heights. This is the single most common tell. Fix: vary padding
   and radius to encode hierarchy (see `design-rules.md`).

## Typography

4. **Undifferentiated sans as the only typeface.** The dominant tell is Inter (or system
   sans) used alone with no intentional pairing. Note the reframe: **serif is not the tell.**
   A serif or distinctive display face for headlines is a recommended *fix* (see Stripe,
   editorial layouts). Fix: a real two-font system (distinctive display + clean body).
5. **Type too small.** Fix: hold the 16px body floor.
6. **Eyebrow-label spam.** Tiny labels stacked on every heading, usually restating the
   section name. Fix: cut them, or write a line with personality (house rule).

## Color and graphics

7. **Purple-to-blue gradients.** The number-one "this looks professional" AI default, in
   heroes, CTAs, and backgrounds. Fix: kill decorative gradients. Use color to signal
   function and state, from the semantic tokens.
8. **Gradient-blob / emoji graphics.** Faking in-page graphics with gradient shapes or
   emoji bullets. Fix: real assets (Figma/Canva), unDraw illustrations, Phosphor icons.
   Flag placeholders as placeholders.
9. **Generic stock imagery and plastic AI illustrations.** The diverse-group-at-laptops
   photo; too-smooth, too-symmetrical generated illustration. Fix: real product
   screenshots, real team photos, or custom illustration with intent.

## Motion and copy

10. **Snap or no motion, or identical fade-ins on everything.** Fix: purposeful
    micro-interactions on primary CTAs and inputs only, not everywhere.
11. **Vague aspirational copy.** "Build the future of work," "all-in-one platform," "scale
    without limits." Fix: specific, concrete copy in the client's own voice (see
    `voice-guide.md`). Headline test: would this client actually say this out loud?

---

## Named AI-default looks to avoid

Whole aesthetic combos that signal "generated." If a plan lands on one of these, revise:

- Cream (#F4F1EA) + serif + terracotta accent (the "tasteful AI" default).
- Near-black background + acid-green accent (the "AI SaaS dark" default).
- Purple/indigo primary + soft blue gradient + Inter + glassmorphism cards.
- Broadsheet hairline columns pretending to be editorial.

Spend boldness in one place. Pick one signature move per design and let the rest be quiet.
If everything is bold, nothing is.

---

### Sources
- 925 Studios AI-slop web-design guide; AXE-WEB on AI sameness; Unpromptable AI design tips;
  AIToolPick AI-website checklist.
- Serif reframe and two-font fix corroborated against the same sources (the tell is
  undifferentiated sans, not serif).
