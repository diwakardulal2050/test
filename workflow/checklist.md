# Checklist

Run the relevant block before each gate and before handoff. This is a pass/fail gate, not a
suggestion. If an item fails, fix it before the client or the developer sees the work.

---

## Before the brand gate

- [ ] The concrete subject is stated: who it is for, the page's one job, how the client sounds.
- [ ] Color: 4 to 6 roles chosen, recorded in `tokens.json`, each pairing's WCAG ratio measured.
- [ ] Type: a real two-font system, not a lone sans. Body face is readable at 16px.
- [ ] The plan named one signature element and did not smear boldness everywhere.
- [ ] Plan does not trip any named default look in `avoid-ai-tells.md`.

## Before the styles gate

- [ ] Spacing comes from the 8pt scale and is *varied* to show hierarchy (not uniform).
- [ ] Radius is a small intentional set, not one value everywhere.
- [ ] Components have real states (default, hover, focus, disabled).
- [ ] Body text is 16px+, line height 1.4 to 1.6, measure 50 to 75 characters.

## Before the landing-page gate

- [ ] Desktop holds the 1280px floor. Content does not run edge to edge on wide screens.
- [ ] No eyebrow-label spam. No section-name eyebrows.
- [ ] No purple-to-blue gradients, no gradient-blob or emoji graphics.
- [ ] Imagery is real or a flagged placeholder, not generic stock or plastic AI illustration.
- [ ] Copy passes `voice-guide.md`: no em dashes, no banned words, no LLM cadence tics.
- [ ] Layout is not centered-everything symmetry.

## Accessibility gate (every gate, non-negotiable)

- [ ] Text contrast 4.5:1 (3:1 for large text), measured not guessed.
- [ ] Non-text contrast 3:1 on borders, icons, focus, and state graphics.
- [ ] Interactive targets 24x24px or larger.
- [ ] Focus indicators visible at 3:1 and not removed.
- [ ] Color is never the only signal for state or meaning.

## Before code handoff

- [ ] Figma file is clean: Auto Layout, Variables for all tokens, semantic names, variants.
- [ ] Components mapped via Code Connect to the client's real components.
- [ ] Generated code was cleaned for semantics and accessibility, not shipped raw.

---

If more than one landing-page item fails, the design is drifting generic. Return to
`design-process.md` step 2, do not patch it in place.
