# Accessibility

WCAG 2.2 AA essentials. These are legal-reference standards (ADA, Section 508, EAA) and a
baseline of craft. Every design ships meeting these. Treat them as pass/fail, not aspiration.

WCAG 2.2 was published 5 October 2023. The contrast numbers are unchanged from 2.1; the
2.2 additions are focus appearance, target size, dragging, and consistent help.

---

## Contrast (the ones you check on every screen)

- **Text contrast 4.5:1** (WCAG 1.4.3) for normal text against its background.
- **Large text 3:1** — large = 18pt (24px) regular, or 14pt (18.66px) bold and up.
- **Non-text contrast 3:1** (WCAG 1.4.11) for UI components and meaningful graphics: button
  borders, input outlines, icons that carry meaning, focus indicators, and state graphics
  (for example a filled vs empty checkbox). A pale gray border on white usually fails this.

Record the actual measured ratio next to each color pairing in
`../design-system/tokens.json`. Do not assert "looks fine"; compute it.

## Focus and targets (new in 2.2)

- **Focus appearance (2.4.11, AA):** the focus indicator must be at least 3:1 contrast
  between focused and unfocused states, and cover an area at least equal to a 2px perimeter
  of the component. No removing focus outlines without a stronger replacement.
- **Target size (2.5.8, AA):** interactive targets are at least **24 x 24 CSS px**, or have
  equivalent spacing around them. Prefer 44px for primary touch targets on mobile.

## General

- **Never block zoom** (repeat of the type rule; it is also an accessibility failure).
- **Color is never the only signal.** Pair color with text, icon, or shape for states,
  errors, and links.
- **Semantic structure.** One `h1` per page, headings in order, real landmarks, alt text on
  meaningful images, labels on inputs. This is a handoff-to-code rule; note it in the design
  so the build inherits it.

---

### Sources
- W3C WCAG 2.2 (w3.org/TR/WCAG22).
- W3C Understanding 1.4.11 Non-text Contrast.
- Target size guidance (TestParty WCAG target-size guide).
