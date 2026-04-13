# RojasReport.com — Design Brief & Brainstorm (Rolling)

> Working document. Captures the brainstorm that produced `/mockups/` and carries forward for the eventual Phase-1 scaffold (Next.js + Tailwind + shadcn).

## Positioning (locked after user feedback)

**RojasReport is the standing intelligence console for American healthcare policy — the reference registry of who pays whom.**

Not a news ticker. Not a blog. A **reference console** — closer to OpenSecrets + ProPublica's Dollars-for-Docs + Bloomberg Terminal than to any editorial site in the category. The bulk of the intelligence is *standing* (entity cards, registries, relationships, histories, cross-references), not breaking. Dossiers are the editorial layer that earns attention on top of the registries.

The single sentence:

> **RojasReport is the only healthcare intelligence publication that looks like an operations console and reads like a magazine.**

## Four readers (the persona quartet)

Every desk, dossier, and registry is built to serve these four:

1. **The Lobbyist** — *Who does AHIP, AHA, and Abbott Labs pay — and who writes the checks back?*
2. **The Physician** — *Can I build a micro-hospital next to this POH — and who's going to try to block it?*
3. **The Lawmaker** — *Who could be a co-sponsor on 340B reform — and who already owes a favor?*
4. **The Voter** — *What is Abbott Labs spending in my district — and is my hospital sending me bills I don't owe?*

The intelligence doesn't change — who's asking does.

## Visual identity (locked)

- **Canvas:** `#0A0A0B` black
- **Text:** `#F5F5F4` near-white, `#8A8A88` dim for secondary
- **Accent:** `#FF6A1F` amber — used sparingly as emphasis and signal
- **Rejected:** any green (read as "weed shop + video game" / new money)
- **Rejected:** Hermès-style elegance grammar (luxury leisure; narrows audience; fights data density). Same amber *can* stay, but in HUD grammar, not haute grammar.
- **Type:**
  - Display: **Fraunces** (open-source serif, italic variant as the signature accent)
  - Body sans: **Geist**
  - Mono/micro-labels: **Geist Mono**
- **Hairlines:** `rgba(255,255,255,.08)`
- **Motion:** sub-second eases `cubic-bezier(.2,.8,.2,1)`, HUD lines drawing on, amber pulse rings on indexed items. No bouncy or slow elegance eases.

## Layout grammar

- **Console chassis** (homepage + navigation + HUD widgets + question strip + desk grid) — dark, mono micro-labels, sharp.
- **Editorial interiors** (dossiers, reading views, long-form) — serif headlines, scroll choreography, generous measure, drop-cap-worthy.
- **Civic OS embeds** (ally rankings, proximity maps, district dashboards) — sit *inside* articles and as panels on the homepage.

## Information architecture

```
/                       Console hero · four personas · desk grid · recent dossiers
/desks                  All 23 registries, sortable
/desks/[slug]           Per-desk landing page (lives on subdomain for active desks)
/dossiers               Long-form archive
/dossiers/[slug]        Long-form reading view (Option B)
/entities/[slug]        Entity card (AHIP, Abbott Labs, specific POH, legislator)
/method                 How we source and verify — the trust layer
/search                 ⌘K-powered cross-desk search
```

Each subdomain (`waysandmeans.`, `poh.`, `payers.`, …) is its own deploy consuming shared `packages/ui`.

## The 23 desks (healthcare-policy registries)

| # | Desk | Focus |
|---|---|---|
| 01 | Ways & Means | Tax writing & entitlement financing |
| 02 | POH | Physician-Owned Hospitals |
| 03 | AHIP & Payers | Insurer trade groups, MCOs, MA plans |
| 04 | Pharma & 340B | Manufacturers, PBMs, drug discount program |
| 05 | Hospitals | Systems, pricing, mergers |
| 06 | CMS | Medicare, Medicaid, rule-making |
| 07 | FDA | Drug & device approvals, enforcement |
| 08 | Physicians | Practice ownership, referrals, conflicts |
| 09 | Lobbyists | Disclosures, revolving door |
| 10 | Donors | Campaign finance → healthcare policy |
| 11 | States | 50-state Medicaid & insurance regulation |
| 12 | Courts | SCOTUS, circuit, healthcare dockets |
| 13 | Devices | Med device industry, recalls, pricing |
| 14 | Digital Health | Telehealth, EHR, RPM, reimbursement |
| 15 | Rural Health | CAHs, FQHCs, shortage areas |
| 16 | Mental Health | Parity, reimbursement, access |
| 17 | Maternal | Outcomes, closures, Medicaid coverage |
| 18 | Seniors / LTC | Nursing homes, home health, hospice |
| 19 | Research | NIH grants, IRBs, disclosures |
| 20 | Workforce | Nursing, GME, physician supply |
| 21 | Prices | Hospital transparency, surprise billing |
| 22 | Oversight | HHS OIG, GAO, Congressional inquiries |
| 23 | Briefs | Daily & weekly cross-desk summaries |

## Key components (for the eventual scaffold)

- `<ConsoleShell>` — chassis with top bar + question strip + desk-grid footer
- `<QueryStrip>` — rotating four-persona questions (replaces the old "live ticker")
- `<EntityCard>` — the atomic unit (AHIP card, POH card, legislator card)
- `<DeskCard>` — grid tile linking to subdomain
- `<Dossier>` — long-form reading view with rails + crossrefs
- `<NetworkOfDesks>` — d3-force hero component
- `<CommandPalette>` — cmdk-based ⌘K across entities, desks, dossiers
- `<AllyScore>`, `<ProximityMap>`, `<DistrictDashboard>` — Civic OS embeds

## Recommended stack

- Next.js 15 (App Router) + React Server Components
- Tailwind v4 + shadcn/ui
- Framer Motion for choreography; d3 for the network graph
- MDX + Contentlayer for dossiers; or Sanity if non-devs will publish
- pnpm + Turborepo monorepo — `packages/ui` shared across 23 subdomain deploys
- Cloudflare/Vercel Edge

## Competitor-teardown one-liners

- **Semafor** → great templated article structure; wrong color/mode (light, blog-feeling)
- **Puck** → strong reporter brands; paywall-first parchment elegance (reject)
- **The Dispatch** → trust signals; visually inert (reject look, keep methodology-as-feature)
- **Axios** → Smart Brevity discipline (borrow for ticker & HUD); anti-depth elsewhere
- **Bloomberg** → Terminal is the gold standard; use adjacent amber (`#FF6A1F` vs their `#FA8C00`)
- **Palantir / Recorded Future** → network-graph grammar is ours to adapt; soften with editorial interiors

## What NOT to do

- No stock Capitol photos
- No navy+gold "authority" palette
- No avatar-first bylines (brand is the desk, not the reporter at chassis level)
- No carousels, ever
- No green accent (rejected as "weed shop + video game")
- No Hermès-style elegance grammar (even with the same amber)

## Open threads

- Hub role: start as **Option A** (pure router) with a feature flag for **Option B** (hub + flagship publisher). Revisit after first desk publishes its flagship dossier.
- Logomark: six directions explored in `mockups/logomarks.html`. Recommendation leans **Hex Badge** (MARK/01) or **Monogram Slash** (MARK/03). Final call pending.
- Hero asset: Kling/Veo3 pre-rendered loop, or React Three Fiber scene? Budget vs. flex.
- Publishing workflow: MDX-in-repo vs. Sanity — depends on who writes.

## Mockups on this branch

- `mockups/index.html` — the main hybrid homepage
- `mockups/use-cases.html` — the four personas as the site's spine
- `mockups/hero-signal.html` — amber-only identity study
- `mockups/network-of-desks.html` — d3-force hero, 23 healthcare registries
- `mockups/dossier-reading-view.html` — long-form `/dossiers/[slug]` reading view
- `mockups/logomarks.html` — six SVG mark directions
- `mockups/competitor-teardown.md` — category positioning analysis
