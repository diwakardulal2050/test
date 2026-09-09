---
name: docs-check
description: Scan the project for missing or stale design documentation (style guide, component specs, content guide, principles, handoff, page specs), rank the gaps by importance, name each specific gap, and offer to create it without auto-writing. Use when asked what documentation is missing, or run proactively before a milestone.
when_to_use: what's missing, documentation gaps, do we have docs, docs check, what should we document, missing specs, is anything undocumented
paths:
  - "work/**"
  - "design-system/**"
  - "client/**"
---

# Docs Check (the proactive gap-asker)

Notice what design documentation is missing or out of date, and offer to fill it. This is
read-only; it reports and offers, it never auto-writes. The enemy is alert fatigue, so surface
the few gaps that matter, not every possible one.

## Scan for

- **Missing artifacts** — is there a style guide (`work/docs/style-guide.md`)? A content guide?
  Design principles? Do the site's built components have specs in `work/docs/components/`? Do
  shipped pages have a `work/pages/` spec and a handoff?
- **Staleness** — did `design-system/tokens.json` change after a doc was written? Did a
  component change but its spec did not? (Check `work/log.md` and file recency.)
- **Coverage gaps** — a heavily-used component or a key page with no documentation.

## Rank, do not dump

Prioritize by importance. A gap on the primary CTA button or the home page outranks one on an
obscure element. Surface the top few, not a wall. If everything is documented, say so plainly.

## For each gap, offer (never impose)

- Name the **specific** missing artifact: "The Button component has no accessibility spec,"
  not "want to add docs?"
- Say which skill would create it (for example "run `/component-spec` on Button").
- Offer it as a short, dismissible line. The designer decides.

## Tell a doc gap from a design question

Some gaps are not missing docs, they are unresolved design decisions or a broken token tier.
Flag those separately: "this is not undocumented, it is undecided," and hand it back as a
design question rather than papering over it with generated prose.

## Output

A short, ranked, scannable report: the gap, why it matters, and the one-line offer to fix it.
Keep the designer in control.
