# Competitor Teardown — What Intel-Adjacent Sites Get Right (and Where RojasReport Should Diverge)

Six reference points, evaluated through the lens of *what RojasReport is trying to be* — a dynamic, multi-desk intelligence console with editorial interiors. The point isn't "copy them"; it's to map the category so we can deliberately stake a different position.

---

## 1. Semafor — semafor.com
**Grammar:** Tight grotesque type, pale background, a signature "Semaform" article structure (News / Reporter's view / Room for disagreement / The view from / Notable). Color is restrained — black text, occasional warm accents.
**What works:** The Semaform is genuinely a brand-defining template. A reader knows what they're getting. Authors are foregrounded.
**Where it falls short for our brief:** Light-mode default reads as "blog." No sense of *now-ness* — no live data anywhere. Subdomains? None — single-river feed.
**Diverge by:** Lead with darkness + live state. Make the *desk* (not the byline) the brand. We can borrow the structured-template idea for our `<Dossier>` component (e.g. "What's new / Who wrote it / What it costs / What dies in conference").

## 2. Puck — puck.news
**Grammar:** Cream/parchment background, big serif (looks like Editorial New / Tiempos), reporter portraits as the homepage. Subscription-first — paywall is the architecture.
**What works:** Personality. You buy "Tara Palmeri at Puck," not "Puck." Strong reporter brands.
**Where it falls short for our brief:** Same parchment-elegance trap we just argued against. Site feels like a magazine with a paywall. Static. No multi-desk routing — Puck isn't a hub, it's a roster.
**Diverge by:** Suppress reporter portraits at the chassis level (mono bylines only). RojasReport's gravity comes from *desks routing intelligence*, not personalities.

## 3. The Dispatch — thedispatch.com
**Grammar:** Conservative editorial — serif headlines, restrained palette, newsletter-first. Very text-forward.
**What works:** Trust signals. Methodology pages. Bylines with depth.
**Where it falls short for our brief:** Visually inert. Could pass for any midmarket think-tank site. Zero motion vocabulary. SEO is good; brand is forgettable.
**Diverge by:** Steal the *methodology-as-a-feature* idea — every dossier links to a "how we know this" sub-page. But render it inside our HUD chassis so the same trust reads as "rigor + tech," not "earnestness."

## 4. Axios — axios.com
**Grammar:** Smart Brevity™ — bullet-heavy, "Why it matters / The big picture / What's next" templated stories. Color: black + a single magenta accent. Cards everywhere.
**What works:** Readable on a phone in 30 seconds. Templates make the brand instantly recognizable.
**Where it falls short for our brief:** Smart Brevity is anti-depth. Long-form gets crushed into bullets. The card grid feels content-farm at scale.
**Diverge by:** Use the Smart Brevity discipline for the **ticker + HUD widgets** (where brevity is correct), but go fully editorial in dossiers. Best of both: snap-read at the chassis, deep-read at the article.

## 5. Bloomberg.com (and the Terminal aesthetic)
**Grammar:** Dense, data-first, signature **Bloomberg orange** (`#FA8C00`) on black for the Terminal; cleaner editorial layout on the public site. Big charts, lots of tickers.
**What works:** The Terminal *is* the gold standard for "professional intelligence as a UI." The orange-on-black is the most recognized intel palette in finance.
**Where it falls short for our brief:** The public site is a different brand from the Terminal — confused identity. The orange is *taken* in the financial intelligence space. We'd be cosplaying.
**Diverge by:** Use a **slightly different amber** (`#FF6A1F` — more red, less yellow than Bloomberg's `#FA8C00`) so we're adjacent without being derivative. Lean into HUD vocabulary the *public* Bloomberg site doesn't use — give us the Terminal's gravity in a consumer-friendly chassis.

## 6. Palantir / Recorded Future (the actual intelligence-tooling aesthetic)
**Grammar:** Deep navy/black, sharp grotesque type, network graphs, map overlays, lots of mono-spaced labels. Less playful than Bloomberg, more "operations center."
**What works:** Authority. You believe these people know things you don't.
**Where it falls short for our brief:** Cold. Inhuman. No editorial warmth. Reads as "tool you pay $200K/year for," not "publication you read with coffee."
**Diverge by:** Take the network-graph and map-overlay vocabulary (see `network-of-desks.html`), but soften with serif editorial interiors so the reader experience is *warmer than the chassis suggests*. That tonal contrast is uniquely ours.

---

## The RojasReport Position (after this teardown)

| Axis | Where the category sits | Where we sit |
|---|---|---|
| **Tone** | Earnest editorial (Dispatch, Puck) ↔ Cold tooling (Palantir) | **Cinematic editorial inside an ops-center chassis.** Warm interiors, sharp shell. |
| **Color** | Light + serif (Puck, Semafor) ↔ Bloomberg orange-on-black | **Off-Bloomberg amber + optional signal-green.** Adjacent, not copying. |
| **Structure** | Single-river (Semafor, Puck) ↔ Roster of personalities (Puck) | **Network of 23 sovereign desks** routed through a hub. Nobody else has this. |
| **Density** | Bullet-thin (Axios) ↔ Wall-of-text (Dispatch) | **Snap-read at chassis, deep-read at dossier.** Brevity where it serves, depth where it earns its keep. |
| **Motion** | Mostly none ↔ Hovers and slow fades | **Sub-second HUD eases + scroll choreography in dossiers.** Two motion grammars, deployed for two jobs. |

The single sentence that defines the position:

> **RojasReport is the only intelligence publication that looks like an operations console and reads like a magazine.**

That's the gap in the market. Everything in `mockups/` is in service of that sentence.
