# Brand — [CLIENT NAME]

The client's brand, in human-readable form. This is the reference. The machine-readable
version (exact tokens) lives in `../design-system/tokens.json`; keep the two in agreement.

Structured on the standard brand-guideline sections. Fill what exists. If the client has no
brand yet, this file is where you establish one, then encode it in the design system.

---

## 1. Brand basics
- Name: [name]
- Tagline: [if any]
- Mission / what they stand for: [one or two lines]
- Positioning: [who they serve and why they are the right choice, in plain words]

## 2. Logo
- Files / location: [link or `references/` path]
- Variations: [primary, mark-only, reversed]
- Clear space and minimum size: [rules]
- Misuse: [what not to do with it]

## 3. Color
- Primary: [name + hex]
- Secondary: [name + hex]
- Accent: [name + hex]
- [Note the role of each. Encode exact values and WCAG ratios in `tokens.json`.]

## 4. Typography
- Display: [face]
- Body: [face]
- [Full system in `../design-system/typography.md`.]

## 5. Imagery
- Photography style: [describe, or "none yet"]
- Illustration style: [describe. Prefer real or unDraw over plastic AI illustration]
- Iconography: [Phosphor by default unless the brand has its own]
- What to avoid: [generic stock, off-brand styles]

## 6. Voice and tone
- How the brand sounds: [describe in the client's terms]
- Words they use / words they avoid: [list]
- Note: the global `../standards/voice-guide.md` rules apply on top of this (no em dashes,
  no LLM cadence tics, no filler). This file adds client-specific voice; it does not relax
  those rules unless it says so explicitly.

## 7. Do's and don'ts
- Do: [on-brand moves]
- Don't: [off-brand moves, competitor looks to avoid]
