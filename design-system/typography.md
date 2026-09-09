# Typography — ICC-IMS

The type system for this client, taken from the Figma file's `Desktop/*` text variables
(the file's own source of truth). This expands section 3 of `design-system.md` and agrees
with the font tokens in `tokens.json`.

---

## The two-font system

- **Display face: Barlow SemiBold (600).** All headings (Hero, H1, H2, H3). A slightly
  condensed grotesque that reads engineered and road-sign-adjacent, which fits an
  infrastructure equipment manufacturer. (rationale inferred, confirm?)
- **Body face: Open Sans.** Regular 400 for paragraphs; SemiBold 600 for buttons, eyebrows,
  H4/H5 labels. Clean and highly readable at small sizes.
- **Utility face:** same as body.

## Scale (from the Figma Desktop variables)

| Variable | Face / weight | Size | Line height | Letter spacing | Use |
|---|---|---|---|---|---|
| Hero Heading | Barlow 600 | 48px | 58px | 0 | hero title only |
| H1 | Barlow 600 | 35px | 48px | 0 | section titles, stat numbers |
| H2 | Barlow 600 | 24px | 100% | 0 | card titles, sub-sections |
| H3 | Barlow 600 | 18px | 26px | 0 | small headings |
| H4 | Open Sans 600 | 16px | 26px | 0 | labels, list leads |
| H5 | Open Sans 600 | 14px | 18px | 0 | small labels |
| Eyebrow | Open Sans 600 | 16px | 100% | 3px | uppercase kickers, red |
| Paragraph 01 | Open Sans 400 | 16px | 25px | 0 | lead/body paragraphs |
| Paragraph 02 | Open Sans 400 | 14px | 21px | 0 | card body, dense UI text |
| Paragraph 03 | Open Sans 400 | 12px | 18px | 0 | captions, fine print |

## Rules

- Headings are always Barlow SemiBold; no other heading weight appears in the file.
- Eyebrows are uppercase, 3px tracking, brand red `#EF4238`.
- Body on light is `#53636E`; headings on light are `#1A395B`; on navy, body is white at
  80–85% opacity and links are teal `#7DCECA`.
- 14px body (Paragraph 02) is common in cards; do not go below 12px anywhere.
- Measure: keep text columns near the file's widths (hero paragraph is 880px at 16px).

## Fallbacks

- Display fallback: `"Arial Narrow", system-ui, sans-serif`.
- Body fallback: `system-ui, -apple-system, sans-serif`.
- Both faces are on Google Fonts (Barlow, Open Sans).
