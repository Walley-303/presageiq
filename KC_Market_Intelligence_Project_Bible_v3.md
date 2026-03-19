# PresageIQ — Project Bible
**Last Updated:** March 19, 2026  
**Owner:** Walley (CEO & Co-Founder, Towns & Walley Intelligence)  
**Status:** Active Development — v2.0 live at https://walley-303.github.io/kc-market-intel/  
**Version:** 3.0 — naming resolved, company structure locked, live deployment complete

---

## 1. What This Project Is

**PresageIQ** (formerly KC Market Intelligence) is a two-purpose product:

1. **Personal use tool** — Walley uses it to analyze Kansas City metro market gaps for his own research and entrepreneurial decision-making.
2. **Live working demo for Towns & Walley Intelligence** — proves the three-layer AI analysis methodology works in the real world before the full Presage platform is built.

This is the flagship product of Towns & Walley Intelligence. It lives in its own GitHub repo, deploys at its own URL, and is eventually white-labeled as a standalone market intelligence platform for other cities under the KansasCityIQ → ChicagoIQ → DenverIQ naming architecture.

---

## 2. Naming & Company Structure — LOCKED

### The Company
**Towns & Walley Intelligence**
- Co-founded by Walley and Emily Towns
- Replaces "InSight Technologies" — InSight had trademark conflicts (Insight Direct USA, active federal marks in tech)
- Towns & Walley is completely clean — zero trademark conflicts found anywhere
- Founding story: *"My co-founder's last name is Towns. We built a company to understand them — together."*
- Emily and Walley have built everything together for 11 years — the name reflects that

### The Product Family

| Product | Status | Purpose |
|---|---|---|
| **Presage** | Brand name — clean, no conflicts in market intelligence category | The platform brand |
| **PresageIQ** | Compound name — completely clean everywhere | The intelligence hub / platform |
| **KansasCityIQ** | First city deployment | Live at walley-303.github.io/kc-market-intel |
| **Presage Field** | Future | Smart glasses / on-the-ground layer |
| **Presage Brief** | Future | PDF export / branded deliverable |
| **ChicagoIQ / DenverIQ** | Future Phase 4 | Second and third city deployments |

### Tagline
*"Presage. See what's coming."*

### Names Checked & Eliminated
The following names were researched and ruled out during this session:
- **InSight / Insight** — Insight Direct USA has active federal marks in tech
- **MarketLens** — trademarked by Biolum Consulting 2017
- **MarketPulse** — trademarked by OANDA
- **CityPulse** — active UK company, widely used
- **FourSight** — registered trademark, psychological assessment firm
- **Augur** — registered by Augur Systems, saturated in cybersecurity/blockchain
- **Kairos** — multiple software registrations
- **Sightline** — multiple registrations including ICF International and Deere & Company
- **Liminal** — liminal.co is an active market intelligence company (direct conflict)
- **Aperture** — aperture.ai is active AI market intelligence SaaS (direct conflict)
- **Animus** — Ubisoft launched Animus Hub March 2026, active IP enforcement
- **Omnivex** — active Canadian software company, 11 registered trademarks since 1991
- **Presage Technologies** — active healthcare software company, Virginia, $3.8M revenue
- **Veridian Technologies** — existing web development company
- **Clairo** — registered trademark of musician Claire Cottrill

### Names Still Available (Reserve List)
- **DistrictIQ** — clean, could serve as sub-product or future hub name
- **Canvass** — clean, strong meaning, hold for potential future use
- **GroundLens** — clean, hold for potential future use
- **Presage Brief** — clean for PDF export product name
- **CityLens** — clean, hold for consumer-facing future product

---

## 3. The Core Methodology (Three-Layer Analysis)

Every neighborhood analysis uses three converging data layers:

| Layer | Source | What It Finds |
|---|---|---|
| Consumer Sentiment | Yelp / Google Reviews | Recurring complaints, unmet demands, gap signals |
| Keyword Clustering | NLP pattern analysis | What consumers ask for that doesn't exist nearby |
| Demographic Overlay | US Census Bureau API | Population, income, age — who lives there vs. what's there |

**Key principle:** No single layer is reliable alone. Convergence across all three = meaningful signal. Human judgment still required to interpret local context.

**Additional layers active in v2.0:**
- Business Density (KC Open Data Portal)
- Historical Disinvestment (HUD / NCRC Mapping)
- Opportunity Zone Status (IRS / Treasury Data)

---

## 4. What's Been Built

### v2.0 Dashboard — Live
**URL:** https://walley-303.github.io/kc-market-intel/
**File:** `index.html` in `C:\Users\usgho\OneDrive\Documents\Ideas\KC Intel\`
**GitHub repo:** https://github.com/Walley-303/kc-market-intel

Features:
- **25 KC metro neighborhoods** covered, scored, filterable by region and opportunity level
- **Sidebar** with search and filter chips (All / High Opportunity / North / South / East / West-JoCo)
- **Metrics panel** per neighborhood: Opportunity Score, Population, Median Income, Review Signal Volume
- **Six active data layers** displayed per analysis
- **Opportunity gap cards** — 4 per neighborhood with Demand, Saturation, and Viability bar scores
- **Risk signals** — color-coded contextual warnings per neighborhood
- **Live Claude AI chat** — each neighborhood has its own AI analyst session (claude-sonnet-4-20250514)
- **Manual Import Panel** (Phase 2 — built into v2.0) — paste Facebook/Nextdoor/forum text, select neighborhood and source type, Claude processes into structured gap signals with strength rating

**Five neighborhoods with full custom deep analysis:**
- Waldo
- Crossroads Arts District
- Kansas City KS / Wyandotte County
- Argentine / Rosedale
- East Side / Prospect

**Note on AI features:** The AI chat and import panel require an Anthropic API key configured server-side to function. Works fully without API key for all static dashboard features. API key integration is the next infrastructure step before full public demo.

---

## 5. Data Sources — Current & Planned

### Currently in Tool (Static/Estimated)
- Demographic data (population, income, median age) — manually researched estimates
- Review signal volume — indexed estimates
- Opportunity scores — composite AI-generated scores

### Planned Live API Integration (Priority Order)
1. **US Census Bureau API** — fully free, live demographic data by tract
2. **KC Open Data Portal** (data.kcmo.org) — business licenses, permits, zoning (free, monthly updates)
3. **Reddit API** — r/kansascity, r/KCFoodScene (note: paid API since 2023, requires backend proxy)
4. **YouTube Data API** — KC food/local content, comment analysis (free tier)
5. **Google Places API** — business listings, ratings, review counts (free tier, limited calls)
6. **Yelp Fusion API** — business search by location/category (free tier, 500 calls/day)
7. **OpenStreetMap / Overpass API** — fully free, business type density by geography
8. **FDIC API** — bank branch locations for financial services gap analysis
9. **HUD datasets** — opportunity zones, historically underserved areas (free downloads)

### Manual Import Workflow — BUILT (v2.0)
- Paste zone for raw community text (Facebook, Nextdoor, Reddit, forums, any source)
- Neighborhood selector (all 25 KC metro neighborhoods)
- Source type tagger
- Claude AI processes through three-layer framework
- Returns: gap signals, demand indicators, risk flags, recommended categories, signal strength (HIGH/MEDIUM/LOW)
- Session import history tracked

### Key Facebook Communities to Monitor (Manual Import)
- KC Foodies
- Kansas City Food Scene
- Buy Nothing KC groups
- Living in [Neighborhood] groups
- Nextdoor exports

---

## 6. Build Roadmap

### Phase 1 — Complete
- [x] v1.0 concept and methodology established (History 488 capstone)
- [x] Capstone presentation built with KC research findings

### Phase 2 — Complete
- [x] v2.0 full dashboard built (25 neighborhoods, AI chat, opportunity analysis)
- [x] Manual import panel built and integrated
- [x] Deployed live to GitHub Pages
- [x] Company and product naming resolved

### Phase 2 — Remaining
- [ ] **Anthropic API key integration** — configure server-side so AI features work on live URL
- [ ] **Census API** — replace static demographic data with live Census Bureau data
- [ ] **Reddit mock data structure** — build UI ready for real API, mock data until backend exists

### Phase 3
- [ ] **Map visualization** — geographic display of opportunity scores across KC metro
- [ ] **YouTube comment analysis** — KC food/local content signal layer
- [ ] **Expand deep custom analysis** — build full custom data for all 25 neighborhoods
- [ ] **Rebrand dashboard** — update UI to reflect Towns & Walley Intelligence / Presage / PresageIQ branding

### Phase 4
- [ ] **Real-time alert layer** — notify when new high-signal content hits monitored sources
- [ ] **PDF export (Presage Brief)** — branded market intelligence deliverable
- [ ] **Second city deployment** — ChicagoIQ or DenverIQ
- [ ] **Backend infrastructure** — move from static GitHub Pages to hosted backend for API key security and Reddit integration
- [ ] **Facebook API integration** — revisit after formal business presence for Meta approval

### Phase 5 (Business Infrastructure)
- [ ] **Register Towns & Walley Intelligence** as LLC in Missouri
- [ ] **File trademark application for PresageIQ** — USPTO, Class 42 (software/SaaS)
- [ ] **Secure domains** — townsandwalley.com, presageiq.com, kansascityiq.com
- [ ] **Missouri veteran-owned business certification** — opens grant and procurement pathways
- [ ] **UMKC Regnier Institute connection** — entrepreneurship resources, potential pitch competition

---

## 7. Immediate Next Steps (Do These First)

### Today / This Week
1. **Secure the domains** — go to Namecheap or Google Domains right now and register:
   - townsandwalley.com (or .io)
   - presageiq.com
   - kansascityiq.com
   - Cost: ~$12/year each. Do this before anyone else does.

2. **Configure Anthropic API key** — so the AI features work on the live URL. This requires either a backend proxy or a temporary workaround. Next build session priority.

3. **Update GitHub repo** — rename and rebrand the repo description to reflect PresageIQ / Towns & Walley Intelligence.

### This Month
4. **Register the LLC** — Missouri LLC filing is ~$50 online at sos.mo.gov. File as "Towns & Walley Intelligence LLC." This gives you a legal entity before you approach any investors or institutions.

5. **File USPTO trademark for PresageIQ** — can be done at USPTO.gov for ~$350/class. File in Class 42 (computer software, SaaS, AI services). Use intent-to-use basis since the product is being actively developed. This starts your priority date.

6. **UMKC Regnier Institute** — pitch competition and entrepreneurship resources. Your profile (veteran, Summa Cum Laude, live product, academic origin) is exactly what they fund.

---

## 8. The Reddit Community Idea

**Concept:** Create a subreddit (r/KCMarketWatch or r/BuildingKC) as a community for KC entrepreneurs and residents discussing business gaps, neighborhood needs, and market observations.

**Value:**
- Generates proprietary signal no other tool has
- Builds audience of exact PresageIQ target market
- Replicable playbook for other cities

**Status:** Not started. Low priority — create it, seed with 5-10 posts, let it grow organically.

---

## 9. Working Protocols

1. **Anchor protocol** — Claude keeps the main thread visible when thinking branches. Flags when drifting and brings focus back.
2. **Cross-reference protocol** — Claude actively flags integration opportunities between PresageIQ, Presage Field, MRT, Emotional Praxis, and other projects during development work.

---

## 10. Broader Context (For Claude in New Sessions)

**Who Walley is:**
- CEO & Co-Founder of Towns & Walley Intelligence (co-founded with fiancée Emily Towns)
- Non-traditional university student (post-military service, 100% disabled veteran) on PhD trajectory in Anthropology
- Graduating Summa Cum Laude with History BA, minors in Race/Ethnic/Gender Studies and Anthropology
- Enrolled in History 488: AI, History & Entrepreneurship at UMKC (active course — PresageIQ is a live academic deliverable)
- Interdisciplinary thinker — gender studies, media studies, political philosophy, cosmology
- Web-like nonlinear pattern recognition style — benefits from structured anchoring
- Emily and Walley have been together 11 years, returned to college together, share most classes

**Veteran / Funding Context:**
- 100% disabled veteran — opens VA Veteran Entrepreneur Portal, SBA Boots to Business, Missouri veteran business grants, SBIR/STTR veteran preference weighting
- Missouri-based — Missouri Technology Corporation, KC-specific angel investor networks
- CDFI angle — Kansas City Community Capital Fund makes loans to veteran entrepreneurs specifically

**Other active projects (cross-reference when relevant):**
- **Emotional Praxis** — original academic framework; how emotional narratives function as tools of power across politics, media, culture
- **Membrane Resonance Theory (MRT)** — cosmological framework; spacetime as continuous elastic resonant medium
- **Crack Baby Capstone Thesis** — media framing, racialized policy consequences, moral panic analysis
- **Healing Through Justice** — political vision, campaign letter manifesto project

**Key stats for pitches:**
- Less than 3% of small businesses use formal market research before launching — primarily due to cost
- US market research industry valued at over $47 billion annually
- 2018 NCRC study: redlining effects persist in 61% of formerly redlined neighborhoods including KC
- KC is among top 20 US cities with expanding food desert corridors
- KC Open Data Portal: 40,000+ active business licensing records, updated monthly, free

---

## 11. How to Start the Next Session

Paste this document into a fresh Claude conversation, then say:

> "I'm continuing work on PresageIQ. Here's the project bible. Let's pick up at [specific phase or task]."

---

## 12. Origin Story & Academic Layer

KC Market Intelligence / PresageIQ began as Walley's midterm proposal for **History 488: AI, History & Entrepreneurship** at UMKC. Original title: *"Using Artificial Intelligence to Identify Underserved Local Business Opportunities in Kansas City."*

When the methodology produced real results, the project evolved from academic exercise into active product development. The capstone became Case Study #1 for what is now Towns & Walley Intelligence.

**Why the academic origin matters:**
- Methodology is academically stress-tested, not just entrepreneurially iterated
- Ethical framework developed under academic rigor
- Built-in credibility for CDFIs, city planners, and university partners
- History 488 framing strengthens the case for proactive data-driven investment

**Institutional Market — Three Distinct Revenue Tiers:**
1. **Entrepreneurs / small business owners** — primary consumer audience
2. **CDFIs and economic development organizations** — B2B institutional tier, currently pay consultants for this analysis
3. **University research centers and city planning offices** — potential funding sources and long-term partners

---

## 13. Presentation & Demo Ecosystem

### Artifact 1: PresageIQ Dashboard (v2.0) — LIVE
- URL: https://walley-303.github.io/kc-market-intel/
- Status: Live, functional, Phase 2 remaining items in progress

### Artifact 2: History 488 Capstone Presentation
- Full presentation with teleprompter, Q&A mode, KC research findings
- Built in InSight chat session, lives in InSight GitHub repo
- Status: Complete, used for academic submission

### Artifact 3: InSight HUD / Field Demo
- Smart glasses simulation showing field intelligence layer
- Used in capstone to show full platform architecture
- Status: Complete, needs rebranding to Towns & Walley / Presage

### Standard Demo Narrative
1. **Dashboard layer**: "You run this before going into the field. It tells you where to look."
2. **Field layer**: "You walk the neighborhood. Presage surfaces what you're seeing in real time."
3. **The gap**: "Yelp indexes what exists. PresageIQ identifies where businesses should exist but don't."

---

## 14. Ethical Framework

### Risk 1: Review Data Demographic Bias
Online review platforms over-represent younger, more affluent demographics. 2020 MIT study: AI sentiment tools misclassify AAVE at rates up to 2.5x higher than standard English.
**Response:** Review data never used alone. Always cross-referenced against Census demographic data.

### Risk 2: Redlining Amplification
AI pattern recognition on geographic data can amplify historical disinvestment.
**Response:** Opportunity signals cross-referenced against HUD/NCRC historical disinvestment maps. Business density measured relative to population, not absolute. AI flags pattern; human judgment interprets cause.
**Counter:** Done responsibly, AI market analysis makes the objective economic case for overlooked neighborhoods — undermining, not reinforcing, redlining logic.

### Risk 3: AI Overreliance
**Response:** AI surfaces the pattern. Human judgment interprets the cause. Non-negotiable division of labor.

### Standard Q&A Counters
- *"Just Yelp?"* — Yelp indexes what exists. PresageIQ identifies where businesses should exist but don't.
- *"Who decides underserved?"* — High demand signal + low business density = objective and auditable.
- *"Gentrification?"* — Tool is agnostic. Policy determines outcome, not methodology.
- *"Sample size?"* — Full-population public data, not statistical sampling.

---

*Update this document at the end of every working session.*
