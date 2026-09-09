---
name: content-guide
description: Generate the client's content and voice style guide (voice profile with executable rules, tone by context, word list, UX-copy rules) grounded in the client's real voice and shipped copy. Use for a voice guide, content style guide, or copy guidelines.
when_to_use: content style guide, voice guide, tone of voice, copy guidelines, writing rules, word list, UX copy rules
paths:
  - "client/**"
  - "standards/**"
---

# Content and Voice Guide Generator

Produce a content guide that makes anyone (or the AI) write in this client's voice. The
difference between a great one and a generic one is **executable rules**, not adjectives.
"Second person, no exclamation points, lead with the benefit" beats "warm but professional."

## Ground first (required)

- Read `client/brand.md` (voice section) and `client/audience.md` (their vocabulary).
- Read `standards/voice-guide.md` (the Wicked house rules that always apply on top).
- Read any real shipped copy or examples in `client/references/`. If there are exemplary
  pieces, annotate each with *why* it works. Unannotated examples teach surface patterns;
  annotations teach the principle.

## Output structure

Write to `work/docs/content-guide.md`. Keep it 400 to 700 words of real rules; shorter usually
means you have not been specific enough.

1. **Voice** — the constant. Mapped on concrete dimensions (formality, energy, warmth,
   complexity) with executable rules, plus a one-line persona for cases the rules miss.
2. **Tone** — how it shifts by context and the reader's emotional state (a happy onboarding vs
   an error message).
3. **Writing principles** — a few, opinionated (clear over clever, active voice, lead with the point).
4. **Grammar and mechanics** — the choices this brand makes.
5. **Word list** — words to use and words to avoid (pull the client's avoid-words from `brand.md`).
6. **UX copy** — buttons, error messages, empty states, form labels.
7. **Channel notes** — web, email, social, blog, only those that apply.

## Rules

- The Wicked house rules in `standards/voice-guide.md` are enforced on top and are not relaxed:
  no em dashes, no filler words, no LLM cadence tics.
- Ground in the client's real words. Do not invent a voice from nothing; extract it.
- Append a `[progress]` line to `work/log.md` when done.
