# Docs

Generated design documentation lives here: the deliverables the skills produce, distinct from
the *input* context in `client/`, `design-system/`, and `standards/`.

Typical contents as a project matures:
- `style-guide.md` (and optionally `style-guide.html`) — from `/style-guide`
- `content-guide.md` — from `/content-guide`
- `design-principles.md` — from `/design-principles`
- `components/<name>.md` — per-component specs, from `/component-spec`
- `handoff-<page>.md` — developer handoff packages, from `/handoff`

These are produced by the skills in `.claude/skills/`. Each is grounded in the client's real
tokens, components, and copy, not a template. Run `/docs-check` any time to see what is missing
or stale.

The distinction to hold: `client/` and `design-system/` are what the design is *built from*;
`work/docs/` is what gets *handed out* (to the client, to a developer, to the next designer).
