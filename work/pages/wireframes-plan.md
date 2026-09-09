# ICC-IMS Full-Site Wireframe Plan

Grounded in three client documents (received 2026-09-09):
- **ICC-IMS Site Map Document – August 2026** (authoritative; supersedes the April
  "Comprehensive Site Map – Needs formatting" draft; adds site-wide search bar, Sidewalk
  Surface Tester, TSDD Network-Level Structural Testing, PMaaS, breadcrumbs schema)
- **Website Journey Mapping Analysis (04/2026, We-NDT Marketing Network)** — 3 primary
  personas (State DOT engineer, Municipal/County public works director, AEC project manager),
  2 secondary (Airport ops, Concessionaire asset manager). Core finding: replace
  seller-centric parallel nav (Markets/Services/Equipment/Software) with buyer-centric journeys.
- **Navigation Changes** — per-segment service groupings for the Who We Serve mega-menu
  (Municipal/County: data collection + consulting; State/Provincial; Civil Engineering firms).

Wireframes live in Figma on the **🖌 Sitemap & Wireframes** page, desktop 1440px, low-fi
grayscale, real headlines and CTA labels from the site map (no lorem). One template frame
covers each repeating page type (equipment detail ×10, software detail ×6, case study ×n).

## Global elements (every page wireframe)
- Utility bar with **site-wide search** (August doc requirement)
- Primary nav: Who We Serve | Solutions | Projects & Case Studies | Resources | Procurement |
  Company + persistent Request a Quote CTA
- Breadcrumbs on all interior pages (August: breadcrumbs schema site-wide)
- Answer-first intro block on every major page (GEO: key facts in first 100–150 words)
- FAQ section on major service/equipment/audience pages (FAQPage schema)
- Footer: nav mirror, NAP, contract vehicle logos

## Frame inventory (21)
1. **Site Map** — visual tree of the August architecture (reference frame)
2. **Navigation & Mega-Menus** — utility bar + nav + expanded panels (Who We Serve ×6,
   Solutions 3-column, Resources) + mobile note: streamlined segment routing
3. **Home** — hero "The Complete Pavement Intelligence Platform — From Data Collection to
   Decision-Making"; 3 persona-routing CTAs; trust bar (50+ yrs, 700+ agencies, 15+ PMS,
   $5M software, largest municipal fleet); three pillars; social proof grouped by segment;
   3 featured case studies; cooperative purchasing banner; CTA row
4. **Who We Serve — State DOTs** — "Precision Pavement Data Collection Equipment & Services
   for State Highway Programs"; compliance lead; equipment grid (7 models); standards matrix
   table; network-level services; ESP + LCMS-2 differentiators; DOT logos/testimonials;
   filtered case studies; coop purchasing vehicles; spec sheets; SurPRO/MAP-21; CTAs
5. **Who We Serve — Municipalities & Counties** — "Know Your Roads. Prioritize Your Budget.
   Show Your Council Actionable Data."; outcomes; How-It-Works 6 steps; surveys; sidewalk/ADA;
   plans; budget scenarios; council presentations; ESA/ESWA/Inform; ROI ($1 vs $6–10/sq yd,
   5–7 yr life extension); GASB 34; testimonials; coop fast-track; sample deliverables; CTAs
6. **Who We Serve — AEC Firms** — "Your Trusted Pavement Data Collection Partner — Seamless
   Integration Into Your Project Team"; subcontract services; PMS integrations + export
   formats; QC/QA; specialized services; equipment; compliance; turnaround; insurance/bonding;
   NAICS; capability statement; CTAs
7. **Who We Serve — Airports** — "Airfield Pavement Intelligence — FAA-Compliant Data
   Collection, Day and Night"; FAA; friction testing; HFST; night ops; LCMS-2; surveys;
   DFW case study; CTA
8. **Who We Serve — Concessionaires** — "Performance Monitoring & Lifecycle Optimization for
   Toll Roads and PPP Highways"; monitoring; compliance reporting; methodology; lifecycle
   cost; ROI one-sheet; CTA
9. **Who We Serve — Federal Agencies** — FHWA LTBP; assessments; GSA vehicles; federal spec
   equipment; military installations; CTA
10. **Equipment Overview** — heritage; US-manufactured; category nav (Profilers | Survey
    Vehicles | Friction Testers | Reference Devices | Sidewalk Surface Tester); consolidated
    compliance matrix; spec library link; CTAs
11. **Equipment Detail template** (IrisPRO Every Speed; covers all 10 product pages) —
    answer-first hero; ESP any-speed differentiator; standards table; specs; vehicle
    compatibility; gallery; FAQ; CTAs (Download Spec Sheet | Request a Quote | View
    Cooperative Purchasing Options)
12. **Services Overview** — 12 service blocks (surveys, sidewalks/ADA, plans, budget
    scenarios, council presentations, network-level, airfield, friction, TSDD structural,
    PMaaS, consulting, SaaS monitoring), each cross-linking; CTA Book a Discovery Call |
    Request a Proposal
13. **Software Overview** — ecosystem + $5M; use-case nav (Unify workflow | ESA | ESWA |
    Integrations); platform cards; CTAs
14. **Software Detail template** (ESA) — outcome-first hero; capabilities; screenshots;
    expandable tech section; FAQ; demo CTA
15. **Projects & Case Studies** — filters (Segment | Service | Outcome); outcome-focused
    cards (challenge → solution → results); embedded testimonials; per-card CTAs
16. **Case Study Detail template** — segment tag; challenge/solution/results; metrics;
    gallery; related links; "Request a Similar Assessment"
17. **Resources Hub** — Blog; Whitepapers & Guides (3 pillar guides); Spec Sheets; Sample
    Reports; Capability Statement; Industry Glossary (IRI, PCI, PMS, HFST, PROWAG, FWD,
    GASB 34); Learning Portal; gated-download pattern
18. **Procurement Hub** — coop purchasing explainer (6-month RFP → 2-week execution);
    contract vehicles + numbers (GSA, Sourcewell, NASPO ValuePoint); partner logos;
    step-by-step; buyer-type quote form; capability statement; insurance/NAICS; CTAs
19. **Company — About Us** — 2022 merger story (ICC ~50 yrs + IMS 38 yrs); credentials;
    US manufacturing; NAP block
20. **Company — Team** — consultant profile grid, leadership, cross-link note
21. **Company — Careers** + **Contact** — positions/culture; inquiry-type contact form,
    offices, support links

## Self-critique before build
- Risk: 21 frames of uniform gray = unreadable wall. Mitigation: consistent section labels,
  real headlines, varied block heights mirroring content weight.
- Risk: duplicating the already-designed homepage. The wireframe reflects the NEW site map
  home (persona routing), which differs from the current designed homepage — that difference
  is the point; flagged for the designer.
- Deliberately deferred: mobile wireframes (desktop first, per current project stage);
  individual wireframes for all 10 equipment / 6 software pages (template frames instead).
