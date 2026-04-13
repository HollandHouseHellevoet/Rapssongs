# RojasReport.com — Redesign Brainstorm Mockups

Static HTML mockups exploring a **dynamic, intelligence-console** redesign for RojasReport.com — the central hub that will route to `waysandmeans.rojasreport.com`, `poh.rojasreport.com`, and ~20 more subdomain "desks" to come.

All mockups are self-contained — no build step, no dependencies. Each file pulls fonts from Google Fonts and (where needed) `d3` from a CDN.

## How to view

Three options, fastest first:

1. **raw.githack.com (recommended — renders HTML live):**
   - Index: https://raw.githack.com/HollandHouseHellevoet/Rapssongs/claude/redesign-rojasreport-dynamic-1Olfj/mockups/index.html
   - Replace `index.html` with any filename below.
2. **Clone + open in a browser:**
   ```
   git clone -b claude/redesign-rojasreport-dynamic-1Olfj git@github.com:HollandHouseHellevoet/Rapssongs.git
   open Rapssongs/mockups/index.html
   ```
3. **GitHub Pages:** enable Pages on this branch in repo Settings → Pages, then visit `https://hollandhousehellevoet.github.io/Rapssongs/mockups/`.

## Mockup index

| File | What it explores |
|---|---|
| `mockups/index.html` | The **main hybrid homepage** — Signal console chassis + Editorial interiors. Start here. |
| `mockups/hero-signal.html` | Identity bake-off · **Amber-primary** (closest to LAYER-X reference). |
| `mockups/hero-green.html` | Identity bake-off · **Signal-green primary** — full terminal aesthetic. |
| `mockups/hero-two-accent.html` | Identity bake-off · **Amber + green two-accent** — editorial vs live state. |
| `mockups/network-of-desks.html` | A `d3-force` network of 23 desks orbiting the RR hub. The "this single component is the brand" idea. |
| `mockups/dossier-reading-view.html` | Long-form `/dossiers/[slug]` editorial reading view (Option B preview). |
| `mockups/logomarks.html` | Six SVG logomark directions: hex badge, circular seal, monogram, waveform, target reticle, dispatch dot. |
| `mockups/competitor-teardown.md` | Semafor / Puck / The Dispatch / Axios / Bloomberg design grammars + where RojasReport should diverge. |

## Status

This is **brainstorm**, not production code. Once a direction is locked, the next session scaffolds Next.js + Tailwind + shadcn on this same branch and lifts these visual decisions into real components.

See `/root/.claude/plans/moonlit-squishing-petal.md` (off-repo) for the full design rationale, including the Hermès-trap analysis and the hub-role decision tree.
