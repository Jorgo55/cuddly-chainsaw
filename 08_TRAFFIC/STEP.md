# STEP 8: TRAFFIC

**Everything is built. Now drive people to it.**

**Depends on**: Steps 6 + 7 complete → funnel live + automations connected
**Produces**: `RESULTS/thegenius.club/08_traffic/`
**Agent**: `icp-filter`

---

## What This Step Does

Execute the traffic strategy in phases. List first, ads second, scale third.

---

## Input

From `RESULTS/thegenius.club/04_copy/`:
- Ad copy per avatar (audited + passed)
- Outbound email copy

From `RESULTS/thegenius.club/02_avatars/`:
- Avatar profiles (for targeting)

From `00_CONTEXT/04_traffic_and_data.md`:
- 50K list details, channel strategy

From `00_CONTEXT/01_icp.md`:
- Scraping targets, Apollo/ZoomInfo filters

---

## Phase 1: Test with 50K List

### 8a. List Preparation
- Verify email deliverability
- Segment by quality signals (if data available)
- Prepare custom SMTP infrastructure

### 8b. Cold Outreach
- Send rate: 1 email per minute (avoid blocks)
- 3-4 touches per contact
- Full list contactable in 5-10 days
- Track: open rate, click rate, booking rate

### 8c. Meta Custom Audience
- Upload list to Meta as custom audience
- Build lookalike audiences (1%, 3%, 5%)
- This seeds the algorithm with real founder data

### Goal
First data through the funnel. Test messaging. Validate conversion path.

---

## Phase 2: Paid Ads (After List Data)

### 8d. Meta Ads Setup
- Use audited ad copy from `RESULTS/thegenius.club/04_copy/`
- Per-avatar ad sets (Red-Liner, Prisoner, Bottleneck)
- Headline filtering ($250K+) protects algorithm
- Lookalike audiences from Phase 1
- Test: hooks, audiences, placements

### 8e. Optimization
- Kill ads that don't earn clicks in 48 hrs
- Scale winners
- Use funnel data to refine targeting
- A/B test: hook variations, audiences, placements

---

## Phase 3: Scale (Future)

- Referral partners / JVs
- Dedicated sales teams
- Google Ads (intent-based — different dynamic)
- LinkedIn (if unit economics work for B2B)

---

## Key Principle

**Test with list → collect data → optimize → THEN scale with ads.**

Don't burn ad budget on an unproven funnel.

---

## Output

Save to `RESULTS/thegenius.club/08_traffic/`:
- `list-outreach-plan.md` — segmentation, send schedule, SMTP config
- `meta-ads-plan.md` — audiences, ad sets, budgets, testing plan
- `tracking-setup.md` — what to measure, KPIs, dashboards
- `results-log.md` — ongoing: what's working, what's not, what to adjust

---

## Done When

- [ ] 50K list segmented and outreach plan documented
- [ ] SMTP infrastructure ready
- [ ] Meta custom + lookalike audiences created
- [ ] Ad sets configured per avatar
- [ ] Tracking/KPIs defined
- [ ] First outreach launched
- [ ] All outputs saved to `RESULTS/thegenius.club/08_traffic/`
