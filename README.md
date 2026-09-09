# Wicked Design Kit

A context folder a designer loads into the Claude Code desktop app at the start of a client
project. It makes the AI smart about one specific client so it produces beautiful, highly
customized, user-centric and project-centric design, built in Figma and handed off to code.

The kit does not constrain your creativity. It arms the AI with context, guardrails, and a
process so you spend your time designing, not fighting generic output.

## What is in here

| Folder | What it is | Who fills it |
|---|---|---|
| `client/` | Who this client is, their audience, brand, and reference images | You, per project |
| `design-system/` | The checkable brand: tokens, type, the full design spec | You / AI, per project |
| `standards/` | Global rules: design norms, accessibility, anti-AI-tells, voice | Fixed. Reused every project |
| `workflow/` | The intake gap-check, design loop, and gate checklists | Fixed. Reused every project |
| `work/` | Your outputs: Figma links, per-page specs, exported assets, generated docs | You, per project |
| `.claude/skills/` | Design skills: the full Figma design-system build, plus style guide, component specs, critique, gap-check | Fixed |
| `CLAUDE.md` | The AI's operating manual | Fixed |

`standards/`, `workflow/`, and `CLAUDE.md` are the reusable core. `client/` and
`design-system/` are what you fill in for each new client. That split is the whole idea: a
starting point that gives freedom, not a cage.

## How to use it

You work locally, one folder per client. No git, no accounts.

1. **Make a folder for the client** on your machine, named after them (for example `ABC/`).
   This folder is the whole project home: context, design system, and later your work.
2. **Copy this kit into it.** The client folder now has `CLAUDE.md` at its root and the four
   layers inside. This is the client's design system and context in one place.
3. **Open the client folder in Claude Code desktop.** The AI reads `CLAUDE.md` first.
4. **Let the AI run intake.** It checks what context is missing (see `workflow/intake.md`),
   tells you the gaps, and asks what you want to fill. Paste your call notes or brief, drop
   the logo and competitor screenshots into `client/references/`, and it fills what it can,
   then asks a few sharp questions. You decide what to fill now and what to defer.
5. **Design in Figma with the AI** through the Figma MCP, following
   `workflow/design-process.md`. Run `workflow/checklist.md` before each client gate.

You stay in the driver's seat the whole time. The kit keeps the AI grounded in this client
and stops it drifting generic; it does not design for you.

## Worked examples

`examples/` has three filled-in clients you can read or start from: **Northwind Ledger** (B2B
SaaS with an established brand), **Fern & Fig** (a new local shop with no brand yet), and
**Lumen Skincare** (DTC ecommerce with a partial brand and a moodboard). Each shows the kit
adapting to a different starting point. See `examples/README.md` for the comparison.

## Design documentation

The kit can produce the documentation a real studio produces, on demand, grounded in the
client's real tokens and components (not templates). Ask for a style guide, a component spec, a
content/voice guide, design principles, or a developer handoff, and it writes them into
`work/docs/`. It also runs an expert **critique** of the work before client gates, and a
**docs-check** that tells you what documentation is missing or stale and offers to fill it. See
`.claude/skills/` for the full set.

## What makes this different

Most AI design setups ship tokens and aesthetic presets but nothing about the actual client.
This kit leads with the client: who they serve, the one job of each page, how they sound.
That grounding, plus hard standards and a plan-then-critique process, is what turns AI output
from generic to custom.

## Requirements

- Claude Code desktop app.
- The Figma MCP server connected (Dev Mode MCP), with a Figma file to build in.
