# Wicked Design Kit — Getting Started

A folder you load into the Claude Code desktop app so the AI designs like a Wicked designer for
one specific client: on-brand, highly customized, built in Figma, without generic AI output. You
stay in the driver's seat the whole time.

If you want the short version: **make a folder for the client, copy the kit into it, open it in
Claude Code, and start chatting.** Everything below is the detail.

---

## What you get

- **A per-client context folder** that becomes the AI's memory for that client.
- **AI that designs in Figma with you**, grounded in the client's real tokens, brand, and voice.
- **Generated documentation** on demand: a style guide, component specs, a content/voice guide,
  design principles, and a developer handoff.
- **A complete design system Figma file** when you want one: design tokens as variables, color,
  text and effect styles, a component library, a style guide, and page designs.

The kit does not replace your taste. It arms the AI with context, guardrails, and a process so
you spend your time designing, not fighting generic output.

---

## Before you start (one-time setup)

You need three things:

1. **Claude Code desktop app** — where you chat and where the AI reads and writes the folder.
2. **Figma desktop app** with the **Dev Mode MCP server** enabled (Figma menu, Preferences,
   turn on "Dev Mode MCP server"). It runs locally at `http://127.0.0.1:3845/mcp`. This needs a
   Figma paid seat.
3. **This kit folder** on your machine.

**Connect Figma to Claude Code once:** add the Figma MCP server in Claude Code so the AI can
build in Figma. You do not repeat this per project. To confirm it works, ask Claude "who am I in
Figma?" and it should return the Wicked Figma account.

---

## Start a client project

1. **Make a folder named for the client**, for example `ABC/`, anywhere on your machine.
2. **Copy the kit into it.** The client folder now has `CLAUDE.md` at its top level and the
   folders (`client/`, `design-system/`, `standards/`, `workflow/`, `work/`, `.claude/`) inside.
3. **Open the client folder in Claude Code desktop** (the Code tab).
4. **Start chatting.** Say something like "let's get started on this client." The AI reads
   `CLAUDE.md` and takes over from there.

That is the whole ritual. No accounts, no git, no commands to memorize.

---

## Project management in Claude Code desktop

Claude Code desktop is your workspace, and it works like a project system if you treat it like
one.

- **The Code tab is where projects live.** Open the Code tab and point it at a folder. That
  folder is the project. Everything the AI reads and writes lives there.
- **One folder per client.** Each client is its own folder (`ABC/`, `Lumen/`). To switch
  projects, open a different folder. Nothing leaks between clients.
- **The folder is the memory (local context).** There is no cloud project to manage. The
  client's context, decisions, tokens, page specs, generated docs, and the worklog are all files
  on disk. Close the laptop, reopen the folder next week, and the AI reads its own files and
  picks up where it left off.
- **The worklog is the project history.** `work/log.md` is a running, dated record the AI keeps
  as it works. Read it to see what happened and why, at a glance.
- **Large builds are resumable.** Building a full design system is a staged, multi-session job.
  The AI keeps a state ledger, so you can stop and resume without losing your place.
- **Back up the folder like any project** (a synced drive, a copy, or git if you use it).

The model in one line: a folder per client, opened in the Code tab, with all context and history
living locally in the folder.

---

## What happens when you chat

1. **Intake.** The AI checks what context is missing and tells you, then asks what to fill.
   Paste your call notes or brief, drop the logo and competitor screenshots into
   `client/references/`, and share the project's Figma file link. It fills what it can and asks
   a few sharp questions. You decide what to fill now and what to defer.
2. **Design loop.** For each page, the AI writes a short plan first (colors, type, layout, one
   signature element), critiques it against the anti-generic rules, and only then builds it in
   Figma. You redirect at any point.
3. **Gates.** The client approves brand, then styles, then the page. The AI logs each approval.
4. **Documentation and handoff.** Ask for a style guide, component specs, a content guide, or a
   developer handoff, and it writes them into `work/docs/`, grounded in the client's real values.
5. **Full design system (optional).** Ask for the whole professional Figma file and the AI runs
   a staged build: tokens as variables, color/text/effect styles, a component library, a style
   guide, and page designs. It works in phases and is resumable.

Everything the AI learns and decides is saved as files in the client folder, so you can stop and
pick up later exactly where you left off.

---

## What is in the folder

- `client/` — who this client is (brief, audience, brand, references). Filled during intake.
- `design-system/` — the design tokens (`tokens.json`), the full spec, and the type system.
  See `design-system/README.md` for how tokens map to Figma variables.
- `standards/` — the always-on rules: design norms, accessibility, the anti-AI-tells list, the
  voice guide, and the image rules. Same for every client.
- `workflow/` — how the AI works: intake, the design loop, the gate checklists, and how project
  Figma files are set up.
- `work/` — your outputs: Figma links, per-page specs, exported assets, generated docs, and the
  worklog (`log.md`).
- `.claude/skills/` — the AI's design skills, including the full Figma design-system build. They
  run automatically when relevant.

---

## Tips for great results

- **Give the AI real material.** The more real context you paste (call notes, the logo,
  reference sites), the less it guesses and the more custom the output. Vague input is where
  generic output comes from.
- **Stay in control.** The AI plans before it builds so you can redirect cheaply. Read the plan,
  steer it, then let it build.
- **Use the client's real assets.** The AI never generates photos. Drop real photography into
  `work/assets/` and it places them; until then it uses a clearly labeled placeholder.
- **Run the checklist.** Before you show the client anything, have the AI run
  `workflow/checklist.md`. It catches contrast failures, generic tells, and voice slips.

---

## Troubleshooting

- **"It cannot reach Figma."** Make sure the Figma desktop app is open and the Dev Mode MCP
  server is enabled in Preferences, then re-check the connection in Claude Code.
- **"The design looks generic."** The context is probably thin. Fill more of `client/` (the
  audience and the page's single job especially), and make sure the tokens are real, not the
  example defaults.
- **"It invented a color."** Point it back at `design-system/tokens.json` and tell it to use the
  named tokens. Never ask for "the brand colors" in the abstract.

---

## Worked examples

If you have the **kit-with-examples** pack, the `examples/` folder holds three fully filled-in
sample clients you can read or start from: **Northwind Ledger** (established brand), **Fern &
Fig** (no brand yet), and **Lumen Skincare** (partial brand plus a full design-system file). Each
shows the kit adapting to a different starting point. See `examples/README.md` for the comparison.
When you copy the kit into a real client folder, leave the `examples/` folder out.
