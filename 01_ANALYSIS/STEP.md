# STEP 1: ANALYSIS

**Before you build anything, understand the battlefield.**

**Depends on**: `00_CONTEXT/` loaded
**Produces**: `RESULTS/thegenius.club/01_analysis/`
**Agent**: `icp-filter`

---

## What This Step Does

Analyze the market, competitors, positioning gaps, and opportunity before touching avatars or offers. This prevents building on assumptions.

---

## 1a. Market Landscape

Answer these:
- Who else targets founders seeking funding? (competitors)
- What do they promise? What's their mechanism?
- What messaging do they use? (scrape their ads, landing pages, emails)
- Where do they run traffic? (Meta, LinkedIn, Google, cold email?)
- What's their pricing? What's their offer structure?
- What are their weak points? Where are they vulnerable?

**Output**: `RESULTS/thegenius.club/01_analysis/competitor-landscape.md`

---

## 1b. Audience Validation

Cross-reference ICP from `00_CONTEXT/01_icp.md` with reality:
- Are there enough founders in the $250K-$2M range actively seeking funding?
- Which communities have the highest concentration?
- What language do they actually use? (scrape forums, Slack, Reddit, LinkedIn)
- What have they already tried? (failed solutions = false beliefs to address)
- What do they complain about most? (real pain language, not our assumptions)

**Output**: `RESULTS/thegenius.club/01_analysis/audience-validation.md`

---

## 1c. Message-Market Fit Check

Before writing anything, validate:
- Does "get funding" resonate more than "scale your business" or "fix your operations"?
- Is the bait-and-switch angle (promise funding → sell readiness) already being used by anyone?
- What hooks have the highest engagement in founder communities right now?
- What's the current skepticism level toward funding consultants/programs?

**Output**: `RESULTS/thegenius.club/01_analysis/message-market-fit.md`

---

## 1d. Channel Analysis

Where does our ICP actually live and engage?
- Which Meta ad placements work for B2B founder targeting?
- LinkedIn vs Meta vs Google — which has better unit economics for this audience?
- Cold email: what response rates are realistic for founder outreach?
- What's the 50K Slack list likely to convert at? (cold list benchmarks)

**Output**: `RESULTS/thegenius.club/01_analysis/channel-analysis.md`

---

## 1e. Opportunity Map

Synthesize everything above into:
- **Our positioning**: how we're different from everything else in market
- **The gap**: what nobody else is doing (or doing badly)
- **The angle**: the ONE insight that makes our approach click
- **Risk factors**: what could kill this before it starts
- **Assumptions to test**: what we believe but haven't proven yet

**Output**: `RESULTS/thegenius.club/01_analysis/opportunity-map.md`

---

## Templates

| File | Purpose |
|------|---------|
| `templates/competitor-analysis.md` | Framework for analyzing each competitor |
| `templates/audience-research.md` | Questions to answer about the audience |
| `templates/positioning-canvas.md` | Map our position vs competitors |

---

## Done When

- [ ] 3+ competitors analyzed with messaging, pricing, and weak points documented
- [ ] Audience language scraped from at least 2 real communities
- [ ] Message-market fit hypothesis validated or adjusted
- [ ] Channel priorities ranked with reasoning
- [ ] Opportunity map complete with assumptions flagged
- [ ] All outputs saved to `RESULTS/thegenius.club/01_analysis/`

→ Proceed to Step 2 (Avatars)
