# Meta Ads Plan — The Genius Club

---

## When to Launch

**AFTER** the 50K list produces first data through the funnel. Do NOT run ads on an unproven funnel.

**Trigger**: At least 20 bookings from list outreach + first conversion data (show rate, close rate)

---

## Campaign Structure

### Account Level

| Setting | Value |
|---------|-------|
| Business Manager | Set up under Genius Club business |
| Pixel | Installed on all funnel pages |
| Conversions API (CAPI) | Server-side tracking for BookingComplete event |
| Domain verification | thegenius.club verified in Business Manager |
| Attribution | 7-day click, 1-day view |

### Campaign Level

| Campaign | Objective | Budget | Notes |
|----------|-----------|:------:|-------|
| **Campaign 1: Custom Audience** | Conversions (BookingComplete) | $50/day | 50K list uploaded as custom audience |
| **Campaign 2: Lookalike** | Conversions (BookingComplete) | $75/day | 1% lookalike from list + 1% from converters |
| **Campaign 3: Interest-Based** | Conversions (BookingComplete) | $75/day | Startup/founder interests |

### Ad Set Level (Per Campaign)

Each campaign has 3 ad sets — one per avatar:

| Ad Set | Avatar | Targeting Layer |
|--------|--------|----------------|
| Ad Set A | Red-Liner | Broad within campaign audience |
| Ad Set B | Prisoner | Broad within campaign audience |
| Ad Set C | Bottleneck | Broad within campaign audience |

**Budget**: $25/day per ad set (at campaign level, let Meta optimize distribution)

### Ad Level (Per Ad Set)

Each ad set runs 3-5 ad variations (hooks):

| Ad Set | Ads |
|--------|-----|
| Red-Liner | Hook 1, Hook 2, Hook 5 (from ad copy file) |
| Prisoner | Hook 1, Hook 2, Hook 5 (from ad copy file) |
| Bottleneck | Hook 2, Hook 3, Hook 4 (from ad copy file) |

**Format**: Single image + text (primary). Test video after initial data.

---

## Audiences

### Custom Audience (Campaign 1)

| Audience | Source | Size |
|----------|--------|:----:|
| 50K List | Email upload from verified list | ~30-35K matches |

### Lookalike Audiences (Campaign 2)

| Audience | Source | Size | Seed |
|----------|--------|:----:|------|
| LAL 1% from list | 50K list upload | ~2.5M | All list contacts |
| LAL 1% from converters | Leads who booked calls | ~2.5M | BookingComplete events |
| LAL 1% from customers | Closed deals | ~2.5M | Available after first sales |

### Interest-Based (Campaign 3)

| Interest Stack | Targeting |
|---------------|-----------|
| Stack A | Startup founders + SaaS + Fundraising |
| Stack B | Venture capital + Angel investing + Series A |
| Stack C | Business scaling + CEO + Founder |

**Exclusions**: Exclude all custom audiences (no overlap between campaigns)

---

## The $250K+ Filter Effect

The headline filter ("For founders making $250K+") will:
- **Increase CPL** — fewer people qualify
- **Dramatically improve lead quality** — only serious founders engage
- **Train the algorithm correctly** — Meta learns from qualified clicks
- **Protect ad spend** — wrong traffic teaches Meta to find more wrong people

**Do NOT remove the $250K+ filter to get cheaper leads. Cheap leads = bad algorithm training = worse leads at scale.**

---

## Budget Plan

### Phase 1: Testing (Month 1)

| Campaign | Daily | Monthly | Goal |
|----------|:-----:|:-------:|------|
| Custom Audience | $50 | $1,500 | Validate funnel with known audience |
| Lookalike | $75 | $2,250 | Find new founders similar to list |
| Interest-Based | $75 | $2,250 | Test cold interest targeting |
| **Total** | **$200** | **$6,000** | **30-60 leads** |

### Phase 2: Optimization (Month 2)

- Kill losing ad sets (no clicks in 48 hours)
- Scale winning hooks (increase budget 20% every 3 days)
- Add new creative variations for winners
- Expected: CPL stabilizes, volume increases

| Scenario | CPL | Monthly Budget | Leads |
|----------|:---:|:--------------:|:-----:|
| Conservative | $100 | $6,000 | 60 |
| Moderate | $70 | $6,000 | 85 |
| Optimistic | $40 | $6,000 | 150 |

### Phase 3: Scale (Month 3+)

- Scale budget on proven campaigns
- Add new creative angles monthly
- Build retargeting audiences
- Test LinkedIn as secondary channel

---

## Testing Protocol

### Week 1-2: Hook Testing

| What to Test | How | Kill Criteria |
|-------------|-----|---------------|
| 3 hooks per avatar (9 total) | Run simultaneously at $10/day each | No clicks after 48 hrs → kill |
| Image vs. video | Test top hook in both formats | Lower CTR after 500 impressions → kill |
| Long-form vs. short body | Test top hook with both | Lower booking rate → kill |

### Week 3-4: Audience Testing

| What to Test | How | Kill Criteria |
|-------------|-----|---------------|
| Custom vs. Lookalike vs. Interest | Compare CPL and lead quality | CPL 3x higher than best → kill |
| LAL 1% vs. 3% vs. 5% | Run on best-performing hook | Lower conversion rate → kill |

### Ongoing: Creative Refresh

- New hook variations every 2 weeks
- Creative fatigue sets in after ~2-4 weeks at scale
- Rotate: new hooks use same body, new body uses winning hook

---

## Optimization Rules

| Rule | Action |
|------|--------|
| Ad gets 0 clicks in 48 hours | KILL — move to next variation |
| Ad gets clicks but 0 bookings in 7 days | REVISE — check landing page message match |
| CPL > $150 for 7 days | KILL ad set, test new audience |
| CPL < $50 consistently | SCALE — increase budget 20% every 3 days |
| Winning hook found | Create 3 variations of the winning hook (different angles, same core message) |
| Creative fatiguing (CPL rising, CTR dropping) | REFRESH — new creative, same targeting |

---

## Retargeting (Week 3+)

| Audience | What They Did | Ad Content |
|----------|--------------|------------|
| Video viewers (50%+) | Watched landing page video | Testimonial / social proof ad |
| Page visitors (no form) | Visited landing page, didn't submit | "Still thinking about it?" + BIA reminder |
| Form submits (no booking) | Submitted form, didn't book | "Your audit spot is still open" |
| Booking no-shows | Booked but didn't show | "We missed you — reschedule?" |

**Retargeting budget**: 10% of total ad spend
**Placement**: Feed + Stories (same as prospecting)
