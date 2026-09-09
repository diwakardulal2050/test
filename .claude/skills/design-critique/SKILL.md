---
name: design-critique
description: Run an expert self-critique of the current design against a rubric (first impression, hierarchy, consistency, accessibility, brand fit, AI-tells) before it is shown to the client, tying every point to the page's objective and keeping each finding Specific, Justified, and Actionable. Use before any client gate or handoff, or when asked to review or critique a design.
when_to_use: critique, design review, review this design, is this good, feedback on the design, pre-gate check, before showing the client
paths:
  - "work/**"
  - "design-system/**"
---

# Design Critique

Review the work to an expert standard before anyone else sees it. This is read-only analysis;
it does not change the design, it reports. It complements `workflow/checklist.md`: the checklist
is pass/fail gates, this is qualitative expert judgment.

## Start from the objective, not taste

First restate, in one line, the page's single job and its audience (from `client/`). Every
finding is evaluated against that objective. Not "this layout feels off," but "this layout
buries the one action the page exists to drive."

## The lenses

Assess through each, quickly:
1. **First impression** — in three seconds, is the one job obvious? Does it look made for this client?
2. **Visual hierarchy** — does emphasis match importance? Is the boldness spent in one place?
3. **Consistency** — are tokens used, or are there ad-hoc colors, spacings, radii?
4. **Accessibility** — contrast, target sizes, focus, per `standards/accessibility.md`.
5. **Brand fit** — does it match `client/brand.md` and the design system?
6. **AI-tells** — run it against `standards/avoid-ai-tells.md`.

## Every finding must pass three tests

- **Specific** — names the exact element and place.
- **Justified** — ties to the objective or a standard, with the reason (cap rationale at two sentences).
- **Actionable** — states the fix.

Drop any "finding" that fails these. Vague opinion is not critique.

## Output

Emit terse, scannable markdown. Rank findings, and split them into **must fix before the client**
and **worth improving**. Do not write an essay. Optionally append a one-line `[progress]` note
to `work/log.md` that a critique pass ran.
