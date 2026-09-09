# Typography — [CLIENT NAME]

The type system for this client. Fill the brackets. This expands section 3 of
`design-system.md` and must agree with the font tokens in `tokens.json`.

---

## The two-font system

A two-font system is required. A lone undifferentiated sans is an AI tell (see
`../standards/avoid-ai-tells.md`).

- **Display face:** [face]. For headings and the one signature moment. [Why this face fits
  the client: what it signals.]
- **Body face:** [face]. Clean and readable at 16px. [Why.]
- **Utility face (optional):** [face or "same as body"]. For labels, captions, code.

Pairing rationale: [one line on why these two work together and match the brand].

## Scale

- **Base: 16px** (the accessible floor). Never smaller for body.
- **Ratio: [1.25 major third / 1.333 perfect fourth / 1.5].** Pick one and hold it.
- Example scale at 1.25: 16 / 20 / 25 / 31 / 39 / 49.

| Tier | Size | Line height | Weight | Use |
|---|---|---|---|---|
| Body | 16px | 1.5 | 400 | paragraphs |
| Body large | 20px | 1.5 | 400 | lead paragraphs |
| H3 | 25px | 1.3 | 600 | sub-sections |
| H2 | 31px | 1.25 | 700 | section titles |
| H1 | 39px+ | 1.15 | 700 | page title |

## Rules

- **Line height:** 1.4 to 1.6 for body, tighter (1.1 to 1.3) for large headings only.
- **Measure:** 50 to 75 characters per line. Cap text column width to hold this.
- **Weights:** define which weights are used. Do not rely on fake bold or synthetic italics.
- **Long-form:** for blog and article body, consider 18px and the upper line-height range.

## Fallbacks

Always ship a fallback stack so the page is readable before web fonts load.
- Display fallback: [serif / sans stack].
- Body fallback: `system-ui, -apple-system, sans-serif` (or a closer match).
