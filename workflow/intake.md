# Intake

The first conversation on a new project. The point: make the AI's context gaps visible so the
designer knows exactly what to fill, and the AI knows what to work on and how. The designer
stays in control. The AI does the checking and the filling; the designer supplies the facts
and the taste.

Run this when a project starts, and again whenever the designer says the context changed
(new call notes, a brand update, a new page).

---

## 1. Scan for gaps

Read `client/` and `design-system/`. A gap is any of:
- A `[BRACKETED]` placeholder still in place.
- An empty section or an obvious "fill me" blank.
- A design-system value still set to the example defaults (for example brand color still
  `#2563EB`, fonts still `[Display face]`).

## 2. Report gaps, grouped

Give the designer a short, scannable report. Group by priority, do not dump a wall of text.

**Required before designing** (the AI will guess and go generic without these):
- **The project's Figma file link** (the file you design in). The real work happens in Figma,
  so get this first and save it in `work/links.md`. If there is no file yet, ask the designer
  to create a Figma file and paste the link.
- `client/brief.md`: the page's single job, the design problem, success metric.
- `client/audience.md`: at least one primary persona with their job-to-be-done.
- `client/brand.md`: color, type, and voice (or a decision to establish them now).
- `design-system/tokens.json`: real brand colors and the two-font system.

**Helpful, can follow** (design can start, fill as you go):
- Competitor references and the concept image in `client/references/`.
- Elevation, secondary personas, the agent prompt guide.

Say clearly which required items are missing and which are already good.

## 3. Ask, do not interrogate

- **First, make sure you have the project's Figma file link.** If `work/links.md` does not
  have it, ask for it before anything else; without it you cannot do the actual design work.
- Offer to fill gaps from material the designer already has. Invite them to paste call notes
  or a brief, and to drop the logo, brand assets, and competitor screenshots into
  `client/references/`. Fill what you can from that first.
- Then ask at most three or four sharp questions for what is still missing. Prioritize the
  page's single job, the primary audience, the success metric, and the voice do/don'ts.
- Never ask for something you can reasonably pull from what they already gave you.

## 4. Fill, and mark inferred vs confirmed

When you write into `client/` or `design-system/` from what the designer gave you:
- Fill the fields plainly.
- Mark anything you inferred (not stated) so the designer can confirm or correct it. Use a
  short `(inferred, confirm?)` note.
- For colors pulled from a logo or reference, record the measured hex and compute the WCAG
  ratio. Do not eyeball.

## 5. Hand control back

- The designer decides what to fill now and what to defer. If they choose to proceed with
  gaps, list the known gaps in one place (a short "known gaps" note in `client/brief.md`) so
  nobody forgets, and go.
- When required context is filled or explicitly deferred, confirm in one line what you now
  understand (who it is for, the page's one job, how they sound) and move to
  `design-process.md`.
- Append a short `[progress]` entry to `work/log.md` noting intake is done and what was
  established or deferred.

---

Intake is not a form the designer fills alone. It is the AI reading the room, saying what it
is missing, and filling the rest from what the designer hands over. Fast, then out of the way.
