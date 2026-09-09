# Design Process

The required loop for every design in this kit. It is deliberately plan-first: the AI plans
and critiques before it builds, because that is what stops generic output. The designer runs
this loop with the AI, redirecting at any step. The designer has full creative freedom; this
process is the rails that keep quality high, not a script that removes choice.

Do not skip to step 4. A design that was never planned or critiqued is the one that ends up
generic.

---

Intake (`intake.md`) runs before this loop, so the context is either filled or its gaps are
known. If it has not run, run it first.

## 1. Ground

Before any visual decision, read the grounding layer:
- `client/brief.md` — what this is, the page's single job, the business goal, the success metric.
- `client/audience.md` — who this is for, their jobs-to-be-done and pain points.
- `client/brand.md` — brand basics and voice.
- `client/references/` — the reference images and moodboard. Note what was measured vs inferred.

State back, in one or two sentences, the concrete subject: who it is for, what the one job of
this page is, and what the client sounds like. If you cannot state this, the grounding layer
is not filled in enough. Stop and ask.

## 2. Plan (compact)

Write a short plan before building. Not prose, just the decisions:
- **Color:** 4 to 6 named hex values with roles (from `design-system/tokens.json` if it
  exists; if not, propose and record them there).
- **Type:** the display face, the body face, and any utility face. Two-font system minimum.
- **Layout:** one sentence describing the structure, plus a quick ASCII wireframe of the page.
- **Signature:** the one element that carries the personality. Name it. Spend your boldness here.

## 3. Critique

Turn on the skeptic before you build. Check the plan against:
- `client/brief.md` — does it serve the one job and the audience, or is it decoration?
- `standards/avoid-ai-tells.md` — does it trip any tell? Is it one of the named default looks?
- The restraint rule — is the boldness concentrated in one place, or smeared everywhere?

If the plan reads generic, revise it and say what you changed and why. Do this before touching
Figma. It is cheap here and expensive later.

## 4. Build in Figma (via MCP)

Build the approved plan in Figma through the Figma MCP. File hygiene is not optional; the
downstream Figma-to-code tools fail on messy files:
- **Auto Layout by default** on frames.
- **Variables for every token.** No hardcoded hex or spacing. Pull from the design system.
- **Semantic layer names.** "PrimaryButton", "HeroHeadline", never "Frame 74".
- **Component variants for states** (default, hover, focus, disabled).
- **Flat hierarchy** over deep nesting.

Build to the plan exactly. If you discover the plan was wrong, go back to step 2, do not
improvise a different design silently.

## 5. Preview and iterate

- Preview in a real browser (via `design-system/tokens.css`) when possible, not only in Figma.
- Branch variations from the approved baseline rather than editing one file into mush. Keep
  the baseline; explore beside it.
- Bring the designer the strongest one or two, not ten.

## 6. Gate: client approval

The client sees and approves in this order:
1. **Brand** (color, type, feel).
2. **Styles** (the component system applied).
3. **Landing page** (the first real page).

Do not proceed past a gate without approval. Record what was approved in `client/brief.md`,
and append a `[gate]` entry to `work/log.md`.

## 7. Handoff

Figma to code:
- Map Figma components to real code components with **Code Connect** so the build uses the
  client's actual components, not generated defaults.
- Expect 20 to 40 percent manual cleanup on any generated code (accessibility, semantics,
  clean structure). Plan for it; do not ship raw tool output.
- Record the Figma file URL and any live/staging links in `work/links.md`, and keep per-page
  specs in `work/pages/` so the project's outputs stay in the client folder.

---

Run `checklist.md` before every gate and before handoff.
