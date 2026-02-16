# List Outreach Plan — 50K Founder List

---

## The Asset

- **Size**: ~50,000 email addresses
- **Source**: Scraped from largest paid Slack group for founders (~$10/mo members)
- **Quality Signal**: These are paying community members = serious founders
- **Quality Risk**: Unknown age of emails, deliverability unverified
- **Legal**: Grey-hat cold outreach. Not opt-in. Use separate outreach domain.

---

## Pre-Send Checklist

| Step | Action | Tool/Method | Status |
|:----:|--------|------------|:------:|
| 1 | **Verify email deliverability** | ZeroBounce, NeverBounce, or MillionVerifier | Pending |
| 2 | **Remove bounces/invalids** | Expect 10-20% invalid → ~40K deliverable | Pending |
| 3 | **Segment by quality signals** | If data available: company size, revenue, role, industry | Pending |
| 4 | **Set up outreach domain** | NOT thegenius.club — use separate domain (e.g., geniusclub-outreach.com) | Pending |
| 5 | **Warm up domain** | 2 weeks of warm-up before blast (gradually increase sends) | Pending |
| 6 | **Configure custom SMTP** | Own infrastructure, NOT Instantly/Mailshake/etc. | Pending |
| 7 | **Test batch (5K)** | Send first 5K, measure open/click/bounce before full send | Pending |
| 8 | **Review copy one final time** | Outbound email copy from `04_copy/outbound-email-copy.md` | Pending |

---

## SMTP Configuration

| Setting | Value |
|---------|-------|
| Send rate | 1 email per minute (60/hr max) |
| Daily limit | 500-1,000 per domain |
| Domains needed | 3-4 outreach domains for parallel sending |
| Warm-up period | 14 days minimum |
| IP reputation | Monitor via mail-tester.com |
| SPF/DKIM/DMARC | Must be configured on all outreach domains |
| Reply-to | Monitored inbox (NOT no-reply) |
| Unsubscribe | Must include opt-out link (CAN-SPAM compliance) |

---

## Send Schedule

### Test Batch (Week 1-2)

| Day | Action | Volume |
|-----|--------|:------:|
| Day 1-14 | Domain warm-up (gradual send increases) | 50→500/day |
| Day 15 | Test batch: Email 1 to 5K contacts | 5,000 |
| Day 16-17 | Monitor: opens, clicks, bounces, spam complaints | — |
| Day 18 | Email 2 to test batch (follow-up) | 5,000 |
| Day 19-20 | Analyze: which subject line won, click rate, booking rate | — |

### Decision Gate

| Metric | Go | Pause | Stop |
|--------|:--:|:-----:|:----:|
| Open rate | >20% | 15-20% | <15% |
| Click rate | >3% | 2-3% | <2% |
| Bounce rate | <15% | 15-20% | >20% |
| Spam complaints | <0.1% | 0.1-0.3% | >0.3% |
| Bookings (from 5K) | >5 | 2-5 | <2 |

### Full Send (Week 3-6)

| Week | Action | Volume | Sequence |
|------|--------|:------:|----------|
| Week 3 | Email 1 to Batch 2 (10K) | 10,000 | Day 1 |
| Week 3+3d | Email 2 to Batch 2 | 10,000 | Day 4 |
| Week 3+7d | Email 3 to Batch 2 | 10,000 | Day 8 |
| Week 3+11d | Email 4 to Batch 2 | 10,000 | Day 12 |
| Week 4 | Email 1 to Batch 3 (10K) | 10,000 | Repeat |
| Week 5 | Email 1 to Batch 4 (10K) | 10,000 | Repeat |
| Week 6 | Email 1 to Batch 5 (remaining) | ~5,000 | Repeat |

### Per-Avatar Segmentation (If Data Allows)

If the list can be segmented by behavioral signals:

| Signal | Avatar | Variation |
|--------|--------|-----------|
| Posting about fundraising on LinkedIn | Prisoner | "Your pitch deck is fine" email |
| Hiring for COO/Ops roles | Bottleneck | "What happens if you can't work for 90 days" email |
| High-revenue companies with small teams | Red-Liner | "Your company is profitable. Are you?" email |
| No signal / default | Generic | Standard 4-email sequence |

---

## Expected Results (Conservative)

| Metric | Number |
|--------|:------:|
| Emails sent | 50,000 |
| Deliverable (~80%) | 40,000 |
| Opens (~20%) | 8,000 |
| Clicks (~3% of opens) | 240 |
| Landing page → booking (~25%) | 60 |
| **Bookings from list** | **40-80** |
| Show rate (~70%) | 28-56 |
| Close rate (~40%) | 11-22 |
| **Revenue at $5K** | **$55K-$110K** |

**Cost**: ~$500 (SMTP setup + domain registration + email verification)
**ROI**: 110x-220x on a $500 investment

---

## Compliance & Risk

| Risk | Mitigation |
|------|------------|
| Spam complaints | Separate outreach domain protects thegenius.club reputation |
| Blacklisting | Low send rate (1/min), proper warm-up, SPF/DKIM/DMARC |
| CAN-SPAM | Unsubscribe link in every email, physical address, honest subject lines |
| GDPR (if EU contacts) | Include opt-out, don't store data beyond legitimate interest basis |
| List decay | Verify before sending, expect 10-20% invalid |
| Negative brand perception | Tone must be respectful, not spammy. "— Andy" signature = personal, not corporate |
