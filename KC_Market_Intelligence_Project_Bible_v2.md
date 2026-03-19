# KC Market Intelligence — Project Bible
**Last Updated:** March 19, 2026  
**Owner:** Walley (CEO & Co-Founder, InSight Technologies)  
**Status:** Active Development — v1.0 artifact built, roadmap in progress  
**Version:** 2.0 — expanded with academic context, ethical framework, and presentation layer

---

## 1. What This Project Is

**KC Market Intelligence** (working title — see naming section below) is a two-purpose product:

1. **Personal use tool** — Walley uses it to analyze Kansas City metro market gaps for his own research and entrepreneurial decision-making.
2. **Live working demo for InSight Technologies** — proves the three-layer AI analysis methodology works in the real world before the full InSight platform is built.

This is a **sister product** to InSight, not a subfolder or feature. It lives in its own GitHub repo, deploys at its own URL, and is eventually white-labeled as a standalone market intelligence platform for other cities.

---

## 2. The Core Methodology (Three-Layer Analysis)

Every neighborhood analysis uses three converging data layers:

| Layer | Source | What It Finds |
|---|---|---|
| Consumer Sentiment | Yelp / Google Reviews | Recurring complaints, unmet demands, gap signals |
| Keyword Clustering | NLP pattern analysis | What consumers ask for that doesn't exist nearby |
| Demographic Overlay | US Census Bureau API | Population, income, age — who lives there vs. what's there |

**Key principle:** No single layer is reliable alone. Convergence across all three = meaningful signal. Human judgment still required to interpret local context.

**Additional layers active in v1.0:**
- Business Density (KC Open Data Portal)
- Historical Disinvestment (HUD / NCRC Mapping)
- Opportunity Zone Status (IRS / Treasury Data)

---

## 3. What's Already Built (v1.0)

A fully functional HTML artifact — dark-themed dashboard with:

- **25 KC metro neighborhoods** covered, scored, and filterable by region and opportunity level
- **Sidebar** with search, filter chips (All / High Opportunity / North / South / East / West-JoCo)
- **Metrics panel** per neighborhood: Opportunity Score, Population, Median Income, Review Signal Volume
- **Six active data layers** displayed per analysis
- **Opportunity gap cards** — 4 per neighborhood with Demand, Saturation, and Viability bar scores
- **Risk signals** — color-coded contextual warnings per neighborhood
- **Live Claude AI chat** — each neighborhood has its own AI analyst session, powered by Claude API (claude-sonnet-4-20250514)
- **Quick select buttons** for Waldo, Crossroads, Brookside, Westport
- **Export Report button** (placeholder — full PDF export is future build)

**Five neighborhoods with full custom deep analysis built in:**
- Waldo
- Crossroads Arts District
- Kansas City KS / Wyandotte County
- Argentine / Rosedale
- East Side / Prospect

All other neighborhoods auto-generate analysis from their demographic/score data profile.

**File:** `kc-market-intelligence.html` (single file, self-contained, runs in browser)

---

## 4. Data Sources — Current & Planned

### Currently in Tool (Static/Estimated)
- Demographic data (population, income, median age) — manually researched estimates
- Review signal volume — indexed estimates
- Opportunity scores — composite AI-generated scores

### Planned Live API Integration (Priority Order)
1. **Reddit API** — r/kansascity, r/KCFoodScene, r/leessummit, r/overlandpark (free, open, high signal)
2. **US Census Bureau API** — fully free, live demographic data by tract
3. **KC Open Data Portal** (data.kcmo.org) — business licenses, permits, zoning (free, monthly updates)
4. **YouTube Data API** — KC food/local content, comment analysis, view counts (free tier)
5. **Google Places API** — business listings, ratings, review counts (free tier, limited calls)
6. **Yelp Fusion API** — business search by location/category (free tier, 500 calls/day)
7. **OpenStreetMap / Overpass API** — fully free, business type density by geography
8. **FDIC API** — bank branch locations for financial services gap analysis
9. **HUD datasets** — opportunity zones, historically underserved areas (free downloads)

### Manual Import Workflow (To Be Built)
- Import panel inside dashboard
- Paste raw text from Facebook groups, Nextdoor, neighborhood forums
- AI processes through same three-layer framework, adds to neighborhood signal
- **Key Facebook communities to monitor:**
  - KC Foodies
  - Kansas City Food Scene
  - Buy Nothing KC groups
  - Living in [Neighborhood] groups
  - Nextdoor exports

### Social Listening (Future)
- Reddit webhooks for real-time new post notifications
- YouTube push notifications for new KC food/local content
- TikTok hashtag monitoring: #KCfoodie, #KansasCityEats, #KClocal
- Facebook: Phase 3 (API restrictions make this lower priority — manual import covers it for now)

---

## 5. Build Roadmap (In Order)

### Phase 1 — Complete
- [x] v1.0 artifact built with 25 neighborhoods, AI chat, opportunity analysis

### Phase 2 — Current (Start Here)
- [ ] **Manual import panel** — paste Facebook/forum content, AI processes into neighborhood signals
- [ ] **Census API** — replace static demographic data with live Census Bureau data
- [ ] **Reddit API integration** — pull live posts from r/kansascity and r/KCFoodScene
  - *Note: Reddit moved to paid API in 2023. Free tier is limited (100 QPM). Browser-based implementation requires backend proxy to protect credentials. Build mock Reddit data structure now; wire real API calls once backend exists.*

### Phase 3
- [ ] **Map visualization** — geographic display of opportunity scores across KC metro
- [ ] **YouTube comment analysis** — KC food/local content signal layer
- [ ] **Expand deep custom analysis** — build full custom data for all 25 neighborhoods

### Phase 4
- [ ] **Real-time alert layer** — notify when new high-signal content hits monitored sources
- [ ] **PDF export** — branded market intelligence brief for entrepreneurs/investors
- [ ] **Second city deployment** — prove the platform scales beyond KC (Denver or Chicago likely)
- [ ] **Facebook API integration** — revisit after InSight has formal business presence for Meta approval

---

## 6. Project Structure & Repo

**Recommended setup:**
- Own GitHub repo: `kc-market-intel` (separate from `insight` repo)
- Deploy via GitHub Pages at its own URL
- InSight links to KC Intel as live demo; KC Intel has InSight badge linking back

**Relationship to InSight:** Sister products. KC Intel is Case Study #1 and proof of methodology. Not a feature — a standalone product.

---

## 7. Product Family & Naming (CRITICAL — Unresolved)

### The Product Family Vision
**InSight Technologies** (parent company) owns three products:

| Product | Purpose | Audience |
|---|---|---|
| **InSight** | AI platform + smart glasses | Professionals, B2B |
| **MarketLens** *(name TBD)* | Market intelligence, city-by-city | Entrepreneurs, CDFIs, economic dev orgs |
| **CityLens** | Consumer city exploration | Residents, tourists — HELD for future |

### Naming Issues — Must Resolve Before Public Launch

| Name | Status | Action |
|---|---|---|
| **InSight** | ⚠️ CONFLICT — insight-glasses.com exists (tourist AR glasses) | Needs IP attorney review ASAP |
| **MarketLens** | ❌ TAKEN — trademarked 2017 by Biolum Consulting (market research) | Do not use |
| **MarketPulse** | ❌ TAKEN — trademarked, used by OANDA (financial data) | Do not use |
| **CityPulse** | ⚠️ RISKY — active UK company, name widely used | Avoid |
| **CityLens** | ✅ Available as far as known — HOLD for consumer product | Reserve |

### Alternative Names Being Considered (for market intelligence product)
- GroundLens
- DistrictIQ
- ClearSignal
- Aperture (if InSight needs full rebrand)
- Vantage
- Focal
- Meridian

### Next Step on Naming
Consult UMKC Law School Small Business Clinic (free consultations). Bring:
- Description of InSight platform (smart glasses, AI, professional tool)
- Description of market intelligence product
- Timeline of development
- Question: Does insight-glasses.com have a registered federal trademark?
- Question: Is our use case distinct enough to coexist?
- Question: What's the filing strategy for the methodology as a provisional patent?

---

## 8. The Reddit Community Idea

**Concept:** Create a subreddit (r/KCMarketWatch or r/BuildingKC) as a community for KC entrepreneurs and residents discussing business gaps, neighborhood needs, and market observations.

**Value:** 
- Generates proprietary signal no other tool has
- Builds audience of exact InSight target market
- Replicable playbook for other cities

**Workflow:** Walley manages the community; Claude helps draft posts, responses, and engagement strategy. Walley executes. Not autonomous posting.

**Status:** Not started. Low priority for now — create it, seed with 5-10 posts, let it grow organically while building the tool.

---

## 9. Working Protocols

Two protocols established for all collaborative sessions:

1. **Anchor protocol** — Claude keeps the main thread visible when thinking branches. Flags when we're drifting and brings focus back.
2. **Cross-reference protocol** — Claude actively flags integration opportunities between KC Intel, InSight, MRT, Emotional Praxis, and other projects during development work.

---

## 10. Broader Context (For Claude in New Sessions)

**Who Walley is:**
- CEO & Co-Founder of InSight Technologies (co-founded with fiancée Emily Towns)
- Non-traditional university student (post-military service) on PhD trajectory in Anthropology
- Enrolled in History 488: AI, History & Entrepreneurship at UMKC (active course — KC Intel and InSight are live academic deliverables, not just side projects)
- Interdisciplinary thinker — gender studies, media studies, political philosophy, cosmology
- Web-like nonlinear pattern recognition style — benefits from structured anchoring

**Other active projects (cross-reference when relevant):**
- **Emotional Praxis** — original academic framework; how emotional narratives function as tools of power across politics, media, culture. Most original academic contribution.
- **Membrane Resonance Theory (MRT)** — cosmological framework; spacetime as continuous elastic resonant medium, dark energy/matter as different frequency expressions of same underlying medium. Grant-application and graduate-program versions drafted.
- **Crack Baby Capstone Thesis** — media framing, racialized policy consequences, moral panic analysis.
- **Healing Through Justice** — political vision, campaign letter manifesto project.

**Migration note:** Walley is migrating work history from ChatGPT to Claude. MRT documents are priority extraction target from conversations.json file.

**Key stats to know (use in pitches and presentations):**
- Less than 3% of small businesses use formal market research before launching — primarily due to cost
- The US market research industry is valued at over $47 billion annually
- A 2018 NCRC study found the economic effects of redlining persist in 61% of formerly redlined neighborhoods across major US cities, including Kansas City
- Kansas City is among the top 20 US cities with expanding food desert corridors, with closures concentrated in historically redlined neighborhoods
- KC Open Data Portal: 40,000+ active business licensing records, updated monthly, free

---

## 11. How to Start the Next Session

Paste this document into a fresh Claude conversation, then say:

> "I'm continuing work on KC Market Intelligence. Here's the project bible. Let's pick up at [specific phase or task]."

Claude will have full context and can begin building immediately.

---

## 12. Origin Story & Academic Layer

**This section documents where KC Market Intelligence actually came from — context that shapes how it's pitched, built, and positioned.**

### The Origin
KC Market Intelligence did not begin as a product. It began as Walley's midterm proposal for **History 488: AI, History & Entrepreneurship** at UMKC — a course focused on how AI intersects with real-world evidence, decision-making, and institutional practice, with explicit requirements for ethical reflection and entrepreneurial innovation analysis.

The original proposal was titled: *"Using Artificial Intelligence to Identify Underserved Local Business Opportunities in Kansas City."* The research question: *How can AI-driven analysis of consumer reviews, demographic data, and business location patterns reveal underserved market niches within Kansas City's local economy?*

When it became clear the methodology was producing real results — and that InSight was the natural platform to house it — the project evolved from academic exercise into active product development. The capstone became Case Study #1 for InSight.

**This origin matters because:**
- The methodology has been academically stress-tested, not just entrepreneurially iterated
- The ethical framework was developed under academic rigor, not as an afterthought
- The project has built-in credibility for institutional audiences (CDFIs, economic development orgs, university partners) because it emerged from a research context
- The History 488 framing — showing how past entrepreneurial gaps in KC neighborhoods created long-term economic consequences — strengthens the case for proactive data-driven opportunity identification

### The Academic Deliverable Status
- Midterm proposal: submitted (KC Research as InSight Case Study #1)
- Capstone presentation: built and functional (see Section 13)
- AI disclosure: documented and compliant with History 488 policy
- Course requirement met: AI use permitted; all interpretation and conclusions are Walley's own

### The Institutional Market — Distinct Revenue Tier
Beyond individual entrepreneurs, three institutional audiences need exactly what KC Intel produces and currently pay consultants for it or go without:

1. **CDFIs (Community Development Financial Institutions)** — federally certified lenders prioritizing underserved markets; need neighborhood-level market intelligence to make lending decisions
2. **City planning and economic development offices** — KC's economic development office needs the kind of continuous, updatable analysis KC Intel can deliver
3. **University research centers** — natural partners given the academic origin; also potential funding sources

This is not an afterthought audience. It's a distinct B2B revenue tier that justifies institutional pricing and opens grant funding pathways.

---

## 13. Presentation & Demo Ecosystem

**This section documents the full artifact ecosystem — not just the dashboard, but everything that's been built around the KC research.**

### Artifact 1: KC Market Intelligence Dashboard (v1.0)
The primary product. Described in full in Section 3.
- File: `kc-market-intelligence.html`
- Status: Built, functional, Phase 2 in progress

### Artifact 2: InSight Capstone Presentation
A fully functional presentation tool built for the History 488 capstone, with:
- **Slide deck with teleprompter mode** — scrollable speaker notes in HUD-style UI
- **Live Q&A mode** — pre-loaded responses for anticipated questions, expandable from short to full answer
- **KC Research findings section** — Waldo/Brookside and Crossroads/Midtown as the two core case study neighborhoods with inverse opportunity profiles
- **InSight product section** — positions the KC research as InSight's live proof of concept
- **Ethical reflection section** — three documented risks with methodological responses (see Section 14)
- **AI disclosure statement** — fully compliant with History 488 policy

Built in: InSight chat (separate from KC Intel sessions). Lives in the InSight GitHub repo or as a standalone HTML artifact.

### Artifact 3: InSight HUD / Field Demo
A smart glasses simulation demo showing how the KC market intelligence data would surface in field mode — overlaying opportunity signals, demographic data, and competitor distance onto a simulated street view. Used in the capstone presentation to show the full InSight architecture (dashboard layer + field layer).

### The Demo Narrative That Ties It Together
The standard demo sequence for any audience:

1. **Dashboard layer** (KC Intel): "You run this analysis before going into the field. It tells you *where* to look."
2. **Field layer** (HUD demo): "You then walk the neighborhood. InSight surfaces what you're seeing in real time."
3. **The gap it closes**: Yelp and Google index what exists. InSight identifies where businesses *should* exist but don't. That forward-looking gap analysis is what no existing platform provides.

---

## 14. Ethical Framework (Methodology Defense)

**This section documents the three ethical risks and their methodological responses — developed under academic rigor, usable in any pitch or presentation.**

### Risk 1: Review Data Demographic Bias
**The problem:** Online review platforms over-represent younger, more affluent, and more tech-engaged demographics. A 2020 MIT study found AI sentiment tools misclassify African American Vernacular English at rates up to 2.5x higher than standard English.

**The methodological response:** Review data is never used alone. Cross-referencing against Census demographic data is built into the three-layer structure. Where review signal and demographic data diverge, human judgment interprets the cause before any opportunity designation is made.

### Risk 2: Redlining Amplification
**The problem:** AI pattern recognition applied to geographic and economic data can amplify historical disinvestment patterns rather than correct them. KC has documented redlining history with measurable present-day effects.

**The methodological response:** Opportunity signals are explicitly cross-referenced against historical disinvestment maps (HUD / NCRC data). The methodology uses business density *relative to population* — not absolute metrics — which avoids penalizing historically underinvested areas. The goal is to distinguish genuine unmet demand from structurally suppressed demand.

**The counter-argument:** Redlining persisted because investment decisions were made on subjective, bias-laden grounds with no systematic data to challenge them. Done responsibly, AI market analysis makes the objective economic case for overlooked neighborhoods — it can undermine the reasoning that allowed redlining to persist, not reinforce it. A CDFIS using KC Intel to identify where to develop affordable commercial space is the same tool used differently.

### Risk 3: AI Overreliance
**The problem:** Treating AI output as determinative rather than as pattern-detection requiring human interpretation.

**The methodological response:** The division of labor is explicit and non-negotiable: AI surfaces the pattern. Human judgment interprets the cause. Every output requires contextual interpretation. This is framed as a feature, not a limitation — it's the methodologically correct approach.

### Standard Counter-Arguments (For Q&A)
- *"Isn't this just Yelp?"* — Yelp surfaces existing businesses. KC Intel identifies where businesses should exist but don't. That's the gap no existing platform addresses.
- *"Who decides what counts as underserved?"* — The methodology defines it as high documented demand signal against low business density — objective and auditable. Human judgment determines the response, not the identification.
- *"Won't this accelerate gentrification?"* — The tool is agnostic. A CDFIS preventing displacement uses the same tool as an outside investor. Policy determines the outcome, not the methodology.
- *"What about sample size?"* — The methodology uses full-population public data, not statistical sampling. AI enables full-population analysis that traditional methods couldn't run at this scale.

---

*Update this document at the end of every working session with new decisions, completed items, and changes to the roadmap or naming situation.*
