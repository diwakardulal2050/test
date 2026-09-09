# Brand — ICC-IMS

The client's brand, in human-readable form. This is the reference. The machine-readable
version (exact tokens) lives in `../design-system/tokens.json`; keep the two in agreement.
Everything below was pulled from the ICC-IMS Figma file (Homepage_08/20/2026 frame) on
2026-09-09; items marked `(inferred, confirm?)` were read out of the design, not stated by
the client.

---

## 1. Brand basics
- Name: ICC-IMS (International Cybernetics Company / Infrastructure Management Services) (inferred from logo lockup, confirm?)
- Tagline: "One Pavement Intelligence Partner. Built for Every Road Program." (hero headline; treat as positioning line, confirm if official tagline)
- Mission / what they stand for: connects road-measuring equipment, field data collection, and pavement-management software so agencies make defensible infrastructure decisions. (from hero copy)
- Positioning: the one accountable partner across the whole chain — "from the laser to the council vote." Equipment + services + software under one roof; 50 years of US equipment manufacturing; 700+ agencies served. (from homepage copy)

## 2. Logo
- Files / location: not in `references/` yet — currently only visible inside the Figma file (nav node 10479:1764). Export and drop into `client/references/`.
- Variations: full-color on light (nav) and reversed on navy (footer) observed. (confirm full set)
- Clear space and minimum size: not documented. (gap)
- Misuse: not documented. (gap)

## 3. Color
Exact values and computed WCAG ratios live in `../design-system/tokens.json`.
- Primary: Navy `#1A395B` — headings, nav, full-bleed bands, footer.
- Deep navy: `#0E1F33` — dark caption panels over imagery (at 92% opacity).
- Accent / CTA: Red `#EF4238` — primary buttons, eyebrows, section kickers.
- Secondary accent: Teal `#7DCECA` — links and dividers on dark surfaces only.
- Neutrals: white surfaces, `#D9E1E5` hairlines, `#53636E` body text.
- Known contrast risk (computed): white on red CTA and red eyebrow text are both 3.81:1 —
  AA large-text only. The file uses them at 14–16px. Flag before handoff.

## 4. Typography
- Display: Barlow SemiBold (headings).
- Body: Open Sans (400 body, 600 labels/buttons).
- Full system in `../design-system/typography.md`.

## 5. Imagery
- Photography style: real field photography — crews in hi-vis, instrumented survey vans on
  location, equipment close-ups, roadway scenes. No studio stock. (from homepage imagery)
- Illustration style: subtle geometric vectors and soft ellipse glows over navy; no character
  illustration. (from homepage)
- Iconography: line icons (Phosphor-compatible names appear in the file: Buildings,
  ClipboardText, FlowArrow, PhoneCall, CalendarCheck, FileText).
- What to avoid: generic stock, AI-generated photos, consumer-tech gradients.

## 6. Voice and tone
- How the brand sounds: plain, concrete, engineering-credible; sells accountability and
  defensibility, not hype. Speaks procurement's language (RFP, capability statement,
  cooperative purchasing). (inferred from homepage copy, confirm?)
- Words they use: pavement intelligence, network-level data, defensible decisions,
  council-ready reporting, standards-aligned, discovery call, capability statement.
- Words they avoid: vague aspirational claims; superlatives without numbers. (inferred)
- Note: the global `../standards/voice-guide.md` rules apply on top of this.

## 7. Do's and don'ts
- Do: lead with proof (50 years, 700+ agencies, $5M in Unify™); pair every claim with a
  concrete artifact (report, dataset, machine); keep dark panels for captions over photos.
- Don't: use red for anything but action/emphasis; put teal on light backgrounds (it is an
  on-dark accent); soften the industrial tone with consumer-brand playfulness.
