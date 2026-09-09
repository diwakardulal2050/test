---
name: design-principles
description: Generate 3 to 5 project-specific design principles (name, statement, what it means, an example, the tradeoff it resolves) grounded in the client's brand, audience, and goals. Use when asked for design principles or a design north star.
when_to_use: design principles, design north star, guiding principles, design values, what should guide this design
paths:
  - "client/**"
---

# Design Principles Generator

Write 3 to 5 principles that help decide fast and consistently on this project. Principles are
decision heuristics, not rules and not taste. A good one is opinionated enough that you could
have chosen the opposite, and it settles real arguments.

## Ground first (required)

- Read `client/brief.md` (the goal, the page's single job), `client/audience.md` (who and their
  pain), and `client/brand.md` (personality).
- The principles must be about THIS client. "Be clear" applies to everyone and is therefore
  useless. "Prove it before you promise it" is a real principle for a skeptical finance buyer.

## Output structure

Write to `work/docs/design-principles.md`. For each principle:

- **Name** — short and memorable.
- **Statement** — one line.
- **What it means** — two or three lines of plain explanation.
- **In practice** — a concrete example of applying it on this project.
- **The tradeoff it resolves** — what you give up, and why that is the right call here. This is
  what makes it a principle and not a platitude.

## Rules

- 3 to 5, no more. If everything is a principle, nothing is.
- Tie each to something real in `client/`. Avoid the generic set (simple, consistent,
  delightful) unless you make it specific to this client.
- Obey `standards/voice-guide.md`.
- Append a `[decision]` line to `work/log.md` noting the principles were set.
