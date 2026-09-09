# Work

Where this project's outputs live. Everything else in the kit is context (`client/`),
standards, or process. This folder is what you actually produce, kept in the same client
folder so nothing is scattered across apps and drives.

## Structure

- `links.md` — the Figma file URL, the live and staging URLs, and any shared links or access
  notes. The one place to find "where is the thing."
- `log.md` — the worklog. A running, dated record of what happened and why (decisions, gate
  approvals, course corrections). The AI appends to it as work happens.
- `pages/` — one spec per page. Copy the template in `pages/README.md` for each new page
  (`home.md`, `wholesale.md`, `shop.md`). A page spec captures the page's single job, its
  sections, and the approval state.
- `assets/` — exported assets (PNG, SVG, source files). See `assets/README.md` for naming.

Keep `work/` for outputs and pointers. Keep facts about the client in `client/`. When in
doubt: if it describes the client, it goes in `client/`; if it is something you made or a
link to it, it goes here.
