# CLAUDE.md — The Genius Club Pipeline

Sequential funnel-building system. Each step gates the next. No skipping.

---

## ALWAYS LOADED (Context Layer)

This is plugged in at all times. Every step reads from here.

**Location**: `00_CONTEXT/` (8 files)

**The Business**: The Genius Club — 12-month membership ($5K) + 90-day accelerator ($10K). Prepares founders for funding. Graduates move to Capital Connections for actual funding.

**The Mechanism**: Promise funding → on call reveal they're NOT ready → sell readiness program → rejected leads boomerang 3 months later.

**The ICP**: $250K–$2M/yr profit, 5–25 employees, 2–5 yrs old. B2B SaaS, Fintech, AI Infra, High-Ticket Agencies. Seed/Pre-Seed >18 months. 10+ failed investor meetings.

**The 3 Avatars** (sketches — fully built in Step 2):
- **Red-Liner** — profitable but burning out
- **Pitch-Deck Prisoner** — 10+ soft nos, can't see operational mess
- **Expert Bottleneck** — can't delegate, IS the business

**The Team**: Andy Murphy (founder), Florian Hugues (strategy), Martin (ads/dev), Jorgo (dev)

---

## THE PIPELINE

```
Step 1: ANALYSIS  →  understand the battlefield
     ↓
Step 2: AVATARS   →  know the customer
     ↓
Step 3: OFFER     →  structure what we sell
     ↓
Step 4: COPY      →  write everything
     ↓
Step 5: AUDIT     →  test everything (PASS or go back)
     ↓
Step 6: FUNNEL    →  build the pages
     ↓
Step 7: AUTOMATIONS → build email/SMS machine
     ↓
Step 8: TRAFFIC   →  drive people to it
```

Each step:
- Has its own folder with `STEP.md` instructions + `templates/`
- Reads results from previous steps as input
- Produces output saved to `RESULTS/[step]/`
- Must complete before the next step starts

---

## STEP 1: ANALYSIS → `01_ANALYSIS/`

**What**: Market research, competitor analysis, audience validation, positioning.
**Why first**: Don't build on assumptions. Understand the battlefield.
**Agent**: `icp-filter`
**Input**: `00_CONTEXT/`
**Output**: `RESULTS/thegenius.club/01_analysis/` — competitor landscape, audience validation, message-market fit, channel analysis, opportunity map
**Gate**: 3+ competitors analyzed, audience language mined, positioning defined

---

## STEP 2: AVATARS → `02_AVATARS/`

**What**: Full 14-section avatar profiles for all 3 targets.
**Why here**: Avatars need real data from Step 1, not guesses.
**Agent**: `icp-filter`
**Input**: `RESULTS/thegenius.club/01_analysis/` + `00_CONTEXT/01_icp.md`
**Output**: `RESULTS/thegenius.club/02_avatars/` — 3 complete avatar files + summary matrix
**Gate**: All 14 sections filled for all 3 avatars, zero blanks

---

## STEP 3: OFFER → `03_OFFER/`

**What**: Complete offer package — value equation, transformation statement, mechanism, naming, pricing, bonuses, guarantee, urgency, credibility, CTAs. Scored on 54-point rubric.
**Why here**: Offer is built FROM avatar data, not before it.
**Agent**: `offer-builder`
**Input**: `RESULTS/thegenius.club/02_avatars/` + `RESULTS/thegenius.club/01_analysis/` + `00_CONTEXT/`
**Output**: `RESULTS/thegenius.club/03_offer/` — offer package, score, avatar fit matrix
**Gate**: Offer score ≥ 35/54, all avatar fits addressed

---

## STEP 4: COPY → `04_COPY/`

**What**: All copy — landing page, booking page, thank you page, ads (per avatar), outbound emails. Through ben heath system + value equation.
**Why here**: Copy is the offer expressed in words. Can't write without the offer.
**Agent**: `copy-engine`
**Input**: `RESULTS/thegenius.club/03_offer/` + `RESULTS/thegenius.club/02_avatars/` + `RESULTS/thegenius.club/01_analysis/`
**Output**: `RESULTS/thegenius.club/04_copy/` — all copy assets per page + per avatar
**Gate**: All funnel copy + all ad variations + outbound email written

---

## STEP 5: AUDIT → `05_AUDIT/`

**What**: Run every creative through 5 audit personas (Ezra→Sophia→Paula→Devin→Avery). Score conversion radar. Trust score. Verdict: PASS / REVISE / KILL.
**Why here**: Nothing goes live unaudited. This is quality control.
**Agent**: `creative-auditor`
**Input**: `RESULTS/thegenius.club/04_copy/` + `RESULTS/thegenius.club/03_offer/` + `RESULTS/thegenius.club/02_avatars/`
**Output**: `RESULTS/thegenius.club/05_audit/` — audit per creative + master verdict table
**Gate**: ALL creatives must PASS. REVISE → back to Step 4 → re-audit. KILL → rewrite → re-audit.

---

## STEP 6: FUNNEL → `06_FUNNEL/`

**What**: Build the actual pages. Landing page, booking page, thank you page. CRM integration.
**Why here**: Pages are built from audited copy. No copy changes at this stage.
**Agent**: `funnel-architect` + `page-builder`
**Input**: `RESULTS/thegenius.club/04_copy/` (passed) + `00_CONTEXT/05_tech_and_automation.md`
**Output**: `RESULTS/thegenius.club/06_funnel/` — page files, specs, screenshots
**Gate**: All pages built, functional, mobile-responsive, CRM connected, <3s load

---

## STEP 7: AUTOMATIONS → `07_AUTOMATIONS/`

**What**: All email/SMS sequences — booking reminders, lead nurture, no-show follow-up, post-call nurture, 3-month boomerang, weekly broadcasts.
**Why here**: Automations trigger from funnel actions. Funnel must exist first.
**Agent**: `email-sequence`
**Input**: `RESULTS/thegenius.club/03_offer/` + `RESULTS/thegenius.club/02_avatars/` + `RESULTS/thegenius.club/04_copy/`
**Output**: `RESULTS/thegenius.club/07_automations/` — all sequences with exact copy + automation map
**Gate**: All 6 sequences written, SMS under 160 chars, automation logic documented

---

## STEP 8: TRAFFIC → `08_TRAFFIC/`

**What**: Execute traffic plan. Phase 1: 50K list outreach. Phase 2: Meta ads. Phase 3: Scale.
**Why last**: Don't drive traffic to an unproven funnel.
**Agent**: `icp-filter`
**Input**: `RESULTS/thegenius.club/04_copy/` (ads) + `RESULTS/thegenius.club/02_avatars/` + `00_CONTEXT/04_traffic_and_data.md`
**Output**: `RESULTS/thegenius.club/08_traffic/` — outreach plan, ad plan, tracking setup, results log
**Gate**: List segmented, SMTP ready, audiences built, first outreach launched

---

## HARD RULES (Every Step)

1. Sell FUNDING on the page — club revealed on call ONLY
2. $250K+ filter visible on EVERY entry point
3. Clarity > cleverness. 3-second comprehension test.
4. Every claim needs proportional proof. No proof = soften the claim.
5. No creative gets ad spend without PASS verdict from Step 5
6. One promise, one ICP, one mechanism per piece of copy
7. Use real audience language (from Step 1), not marketing jargon
8. When uncertain → direct, confident, no-fluff

---

## AGENTS

| Agent | Steps | Purpose |
|-------|-------|---------|
| `icp-filter` | 1, 2, 8 | Analysis, avatars, targeting, scraping |
| `offer-builder` | 3 | Offer structure, scoring, avatar fit |
| `copy-engine` | 4 | All copy through ben heath + value equation |
| `creative-auditor` | 5 | 5-persona audit, scoring, verdicts |
| `funnel-architect` | 6 | Page structure, flow, conversion logic |
| `page-builder` | 6 | HTML/CSS implementation |
| `email-sequence` | 7 | Email/SMS sequences, automations |

---

## FILE MAP

```
00_CONTEXT/              ← ALWAYS LOADED (business intel from transcript + docs)
01_ANALYSIS/             ← Step 1: market, competitors, positioning
│   ├── STEP.md
│   └── templates/       (competitor-analysis, audience-research, positioning-canvas)
02_AVATARS/              ← Step 2: customer profiles
│   ├── STEP.md
│   └── templates/       (14-section avatar template)
03_OFFER/                ← Step 3: offer architecture
│   ├── STEP.md
│   └── templates/       (value equation, pricing, naming, bonuses, guarantees, etc.)
04_COPY/                 ← Step 4: copywriting
│   ├── STEP.md
│   └── templates/       (hook frameworks, ben heath angles)
05_AUDIT/                ← Step 5: creative audit
│   ├── STEP.md
│   ├── AUDIT_SYSTEM.md
│   ├── trust-rubric.md
│   ├── output-standards.md
│   └── personas/        (Ezra, Sophia, Paula, Devin, Avery)
06_FUNNEL/               ← Step 6: page implementation
│   └── STEP.md
07_AUTOMATIONS/          ← Step 7: email/SMS
│   ├── STEP.md
│   └── templates/       (reminders, nurture, broadcasts + additional flows)
08_TRAFFIC/              ← Step 8: drive traffic
│   └── STEP.md
RESULTS/                 ← ALL OUTPUTS (one subfolder per project)
│   └── thegenius.club/  ← The Genius Club project
│       ├── 01_analysis/
│       ├── 02_avatars/
│       ├── 03_offer/
│       ├── 04_copy/
│       ├── 05_audit/
│       ├── 06_funnel/
│       ├── 07_automations/
│       └── 08_traffic/
.claude/agents/          ← 7 specialized agents
```
