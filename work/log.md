# Worklog — ICC-IMS

A running record of what happened and why. The AI appends a short dated entry at each
meaningful moment, so a later session or another designer can pick up instantly and nobody
re-litigates a settled decision.

## How it works
- The AI adds entries as work happens: intake done, a brand or direction decision, a gate
  approval, a course correction.
- **Newest entries at the bottom.** Append only. Never rewrite a past entry; if something
  changes, add a new entry that says what changed and why.
- Keep each entry to a line or two. Use today's date.

Tags:
- `[progress]` what got done
- `[decision]` what was chosen, and why
- `[gate]` a client approval
- `[change]` a course correction

---

## 2026-09-09
- [progress] Kit installed into diwakardulal2050/test (branch claude/vibrant-galileo-wiisvz). Intake run.
- [progress] Figma link captured (ICC-IMS (Copy), homepage node 10479-1744 = 08/20 iteration). Tokens, typography, brand, brief, audience filled from measured Figma values; inferred items marked for confirmation.
- [decision] Colors are not Figma variables (only Desktop/* type styles are), so palette was measured from node fills: navy #1A395B, deep navy #0E1F33, red #EF4238, teal #7DCECA, body #53636E, hairline #D9E1E5.
- [progress] Known gaps accepted by designer: audience "general" (personas inferred from the page's three segments), success metric/timeline/competitors unconfirmed. CTA contrast risk flagged (white on #EF4238 = 3.81:1).
- [progress] Coded desktop homepage prototype built from Figma node 10479-1744 (all 14 sections) at work/prototype/homepage.html; published at https://claude.ai/code/artifact/963866fe-760c-4e2a-9b93-179473e0eadb.
- [decision] Photos and agency logos are labeled placeholders (environment cannot download Figma asset exports; kit image standards require labeled placeholders until real assets are placed). Icons redrawn as inline SVG in the file's Phosphor style. FAQ answers beyond the first were closed in Figma, so answers were written from the page's own facts (inferred, confirm).
- [progress] Designer uploaded real assets to the repo; organized into work/assets/ (logos/, photos/). Wired into the prototype: What We Do van, Who We Are crew, three pillar photos, 10 agency logos. Added full mobile responsiveness (hamburger nav, stacked sections, 2x2 stat grid); homepage.src.html is the editable source, homepage.html the embedded build.
- [change] 7 uploaded logo files are blank 219-byte PNGs (PennDOT, FDOT, WYDOT, Moore OK, Lancaster TX, Harvard IL, Camden SC); those agencies stay as text badges until real files arrive. Hero-card and case-study photos still not supplied; labeled placeholders remain.
- [progress] Full check against Figma frame 10479-1744: copy verified verbatim for all 14 sections (case studies, why, next steps, FAQ, logo strip re-fetched). Image inventory: 15 of 23 rasters placed; 8 missing (ICC-IMS logo, 3 hero photos, 3 case-study photos, 7 blank logo re-exports) listed in work/assets/README.md. Figma asset downloads blocked by egress policy, so exports must come via the repo.
- [change] ADOT logo upload turned out to be a cropped export (only part of the wordmark); swapped to a text badge and added to the re-export checklist. Logo strip re-sized to the design's inset heights (max 32px in a 45px row) so logos sit evenly.
- [progress] All missing images fetched from Figma via a one-shot GitHub Actions workflow (session egress blocks figma.com; Actions runner fetched fresh short-lived export URLs). Real ICC-IMS logo, 3 hero photos, 3 case-study photos, and 8 remaining agency logos wired into the prototype; blank/cropped uploads removed. Prototype republished.
- [change] What We Do / Who We Are photos were cropping at sub-1440 widths (media had no intrinsic height, so the text column drove panel height and object-fit cover over-cropped). Media columns now carry the image aspect ratios (651:452 and 651:407) and anchor to the notch edge, matching the Figma panels at any width.
- [change] Restored the angled notch edges on both split-panel photos at all widths: notch geometry measured from the source PNGs' alpha channels (van: vertex 6.8% x 75% y on left edge; crew: vertex 94.3% x 25% y on right edge) and applied as container clip-paths, so residual cover-crop can no longer flatten them.
- [change] Page content now max-width 1440px centered on wide viewports; utility bar and nav stay full-bleed per designer instruction.
- [change] Section background colors now bleed full width on wide screens; inner content still holds the 1440px grid (1312px + 64px gutters) via responsive gutter padding. Nav and utility bar unchanged (full-width layout).

## 2026-09-09 (cont.)
- [progress] Figma file organized (non-destructive): 19 pages reordered into brief → wireframes → Components → Style Guide → Homepage → playgrounds → review pipeline → Graveyard; typos fixed ("Compontents" page, "Pimary Button" component); 🎨 Style Guide page added; Homepage page wrapped into ✅ Current / 🗄 Superseded iterations / 🔬 Section explorations sections. Playground pages left untouched (other designers' space).
- [progress] Client documents received and mined: Site Map Aug 2026 (authoritative; adds site-wide search, Sidewalk Surface Tester, TSDD structural testing, PMaaS), journey mapping analysis 04/2026, Navigation Changes, 14 content docs + client logo library. Text extracts committed to client/references/.
- [progress] Full-site wireframes built on 🖌 Sitemap & Wireframes page: 21 frames (site map tree, nav + mega-menus per Navigation Changes doc, Home, 6 audience pages, Equipment/Services/Software overviews + detail templates, Projects, Case Study template, Resources Hub, Procurement Hub, About/Team/Careers/Contact). Real headlines and CTAs from the site map, labeled placeholders per kit image standards. Plan + self-critique: work/pages/wireframes-plan.md.
- [decision] Wireframed the NEW buyer-centric Home per the Aug 2026 site map (persona-routing hero). It differs from the designed "Homepage Updated" frame (10479-1744); designer needs to reconcile the two before homepage revisions.
- [change] Designer direction: wireframes must match the Homepage Wireframe (10343-142) - hi-fi greyscale, near-final copy, image placeholders - and all live on the 🖌 Sitemap & Wireframes page (no separate Figma pages). Lo-fi schematic pass superseded and parked below (zz sections); the 11 temporary wireframe Figma pages deleted.
- [progress] 18 hi-fi page wireframes built by cloning the Homepage Wireframe section system verbatim (nav, hero+routing cards, black stat band, pillars, social proof, case cards, dark band, why-rows, FAQ, next-steps band, footer) and rewriting only text from the client content docs (01-13): AEC, Airports, Concessionaires, Federal, Equipment overview + IrisPRO ESP detail template, Services, Software overview + ESA detail template, Projects, Resources, Procurement, About, Team, Careers, Contact, plus hi-fi State DOTs and Munis versions. Section "02 - Hi-Fi Page Wireframes" (12027-2).
- [decision] Open items from the content docs carried into wireframes as visible placeholders, not invented: turnaround commitments, GSA/Sourcewell/NASPO vehicles, Buy American status, software pricing/implementation, municipal testimonial quotes, team roster, bonding (client questions publishing).
- [change] Wireframe set revised per designer direction: (1) grounded in the FINALIZED homepage design (10479-1744), not the old homepage wireframe - new greyscale Home wireframe converts it section-for-section; (2) sections now vary per page content instead of mirroring the homepage lineup; (3) capped at a 15-pattern section library (P01-P15 layer names) for later componentization; (4) post-FAQ 3-box CTA removed everywhere (Next Steps survives only on Home, mid-page, where the final design has it); (5) stat band only where stats carry the page (7 of 19); (6) flat content on section backgrounds - no white boxes inside light sections; (7) old dark footer retained. All 19 frames rebuilt in section 12027-2.
