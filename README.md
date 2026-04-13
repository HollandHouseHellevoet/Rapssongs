# RojasReport.com — Redesign Brainstorm Mockups

Static HTML mockups exploring a **dynamic standing-intelligence console** redesign for RojasReport.com — the central hub that will route to `waysandmeans.rojasreport.com`, `poh.rojasreport.com`, and ~20 more subdomain "desks" to come.

## Positioning

> **RojasReport is the standing intelligence console for American healthcare policy — the reference registry of who pays whom.**

Not a news ticker. Not a blog. A reference console for four readers asking the same question from different angles:

1. **The Lobbyist** — who does AHIP, AHA, and Abbott Labs pay?
2. **The Physician** — can I build a micro-hospital next to this POH?
3. **The Lawmaker** — who could be an ally on 340B reform?
4. **The Voter** — what is Abbott Labs spending in my district?

Full design brief: [`docs/design-brief.md`](./docs/design-brief.md).

## How to view

All mockups are self-contained — no build step, no dependencies beyond CDN fonts (+ d3 for the network graph).

1. **raw.githack.com (recommended — renders HTML live):**
   - Main hybrid homepage: https://raw.githack.com/HollandHouseHellevoet/Rapssongs/claude/redesign-rojasreport-dynamic-1Olfj/mockups/index.html
   - Replace `index.html` with any filename from the index below.
2. **Clone + open in a browser:**
   ```
   git clone -b claude/redesign-rojasreport-dynamic-1Olfj git@github.com:HollandHouseHellevoet/Rapssongs.git
   open Rapssongs/mockups/index.html
   ```
3. **GitHub Pages:** enable Pages on this branch in repo Settings → Pages, then visit `https://hollandhousehellevoet.github.io/Rapssongs/mockups/`.

## Mockup index

| File | What it explores |
|---|---|
| [`mockups/index.html`](./mockups/index.html) | Main hybrid homepage — console chassis + editorial interiors + four-personas section. **Start here.** |
| [`mockups/use-cases.html`](./mockups/use-cases.html) | The four readers as the site's spine — each with the question they ask and the answer-shape RojasReport returns (entity graph, proximity map, ally ranking, district dashboard). |
| [`mockups/hero-signal.html`](./mockups/hero-signal.html) | Amber-only identity study — the "Signal" palette. |
| [`mockups/network-of-desks.html`](./mockups/network-of-desks.html) | Interactive `d3-force` network of the 23 healthcare registries orbiting the RR hub. Drag the nodes. |
| [`mockups/dossier-reading-view.html`](./mockups/dossier-reading-view.html) | Long-form `/dossiers/[slug]` reading view — editorial interior with rails, pull-quote widget, embedded vote tracker, crossrefs. |
| [`mockups/logomarks.html`](./mockups/logomarks.html) | Six SVG logomark directions: hex badge, circular seal, monogram, waveform, target reticle, dispatch dot. |
| [`mockups/competitor-teardown.md`](./mockups/competitor-teardown.md) | Semafor / Puck / The Dispatch / Axios / Bloomberg / Palantir design grammars + where RojasReport should diverge. |

## Decisions made (so far)

- **Positioning:** standing healthcare-policy intelligence, not breaking news
- **Lane:** hybrid Signal console + Editorial interiors
- **Identity:** amber (`#FF6A1F`) on black; no green (rejected); Fraunces serif + Geist sans/mono
- **Brand scope:** full visual identity redesign on the table
- **Hub role:** start as pure router (Option A), toggle to hub-publisher (Option B) later
- **Rejected:** Hermès-style elegance grammar (wrong semantic payload for an intel site)

## Status

This branch is **brainstorm**, not production code. Once the identity + hub role are fully locked, the next phase scaffolds Next.js 15 + Tailwind v4 + shadcn/ui on this same branch and lifts these visual decisions into real components.
