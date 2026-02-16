# Tracking & KPIs — The Genius Club

---

## Tracking Stack

| Tool | Purpose | Events |
|------|---------|--------|
| **Google Analytics 4** | Full funnel analytics | PageView, VideoStart, VideoComplete, FormSubmit, BookingComplete |
| **Meta Pixel** | Ad optimization + retargeting | PageView, Lead, BookingComplete |
| **Meta CAPI** | Server-side conversion tracking | BookingComplete (deduplicated with pixel) |
| **GHL CRM** | Lead management + automation triggers | Contact created, booked, attended, closed, no-show |
| **UTM parameters** | Source/medium/campaign attribution | On all ad links and email links |

---

## Event Tracking Map

| Event | Where | GA4 | Meta Pixel | GHL |
|-------|-------|:---:|:----------:|:---:|
| PageView (Landing) | Landing page | ✓ | ✓ | — |
| VideoStart | Landing page | ✓ | — | — |
| VideoComplete (80%) | Landing page | ✓ | — | — |
| FormVisible | Landing page (post-gate) | ✓ | — | — |
| FormSubmit (Lead) | Landing page | ✓ | ✓ (Lead) | ✓ (Contact) |
| PageView (Booking) | Booking page | ✓ | ✓ | — |
| QualComplete | Booking page | ✓ | — | ✓ (Tags) |
| BookingComplete | Booking page | ✓ | ✓ (CAPI) | ✓ (Booked) |
| PageView (ThankYou) | Thank you page | ✓ | ✓ | — |
| BonusVideoStart | Thank you page | ✓ | — | — |
| CallAttended | Post-call | — | — | ✓ |
| CallClosed | Post-call | — | — | ✓ |
| CallNotClosed | Post-call | — | — | ✓ |
| NoShow | Post-call | — | — | ✓ |

---

## UTM Structure

### Meta Ads
```
?utm_source=meta
&utm_medium=paid
&utm_campaign={campaign_name}
&utm_content={ad_set_name}_{ad_name}
```

### Cold Email
```
?utm_source=email
&utm_medium=outbound
&utm_campaign=50k_list
&utm_content=email_{number}
```

### LinkedIn Organic
```
?utm_source=linkedin
&utm_medium=organic
&utm_campaign=thought_leadership
```

---

## KPI Dashboard

### Top-Level KPIs (Weekly Review)

| KPI | Target | Formula |
|-----|:------:|---------|
| **Cost Per Lead (CPL)** | <$100 | Ad spend ÷ form submissions |
| **Cost Per Booking (CPB)** | <$200 | Ad spend ÷ completed bookings |
| **Show Rate** | >70% | Calls attended ÷ calls booked |
| **Close Rate** | >40% | Deals closed ÷ calls attended |
| **Cost Per Acquisition (CPA)** | <$500 | Total spend ÷ customers acquired |
| **Revenue Per Lead** | >$50 | Total revenue ÷ total leads |

### Funnel Conversion Rates (Weekly Review)

| Stage | Target | Formula |
|-------|:------:|---------|
| Click → Landing Page View | >90% | (page views ÷ clicks) |
| Landing Page → Video Start | >60% | (video starts ÷ page views) |
| Video Start → Video Complete | >50% | (video completes ÷ video starts) |
| Video Complete → Form Submit | >40% | (form submits ÷ video completes) |
| Form Submit → Booking | >50% | (bookings ÷ form submits) |
| Booking → Show | >70% | (attended ÷ booked) |
| Show → Close | >40% | (closed ÷ attended) |

### Channel-Level KPIs

| Channel | Primary KPI | Secondary KPI |
|---------|------------|---------------|
| Cold Email (50K list) | Open rate >20%, Click rate >3% | Booking rate from opens >1% |
| Meta Ads | CPL <$100, CTR >1% | Booking rate from leads >50% |
| LinkedIn Organic | Impressions >5K/week | Click-through to landing page |

---

## Reporting Cadence

| Frequency | What | Who |
|-----------|------|-----|
| **Daily** | Ad performance (spend, CPL, CTR) | Martin/Jorgo |
| **Weekly** | Full funnel report (all KPIs) | Team review |
| **Monthly** | Channel comparison, CAC, LTV projection | Andy + Florian |
| **Quarterly** | Strategy review, channel allocation, scaling decisions | Full team |

---

## Dashboard Setup

### Recommended Tool
**Google Looker Studio** (free) connected to:
- GA4 (funnel events)
- Meta Ads API (ad performance)
- GHL (CRM pipeline data)

### Dashboard Pages

| Page | Metrics |
|------|---------|
| **Overview** | Total leads, bookings, calls, closes, revenue, spend, CPA |
| **Funnel** | Stage-by-stage conversion rates with drop-off visualization |
| **Ads** | Per-campaign, per-ad-set, per-ad performance (CTR, CPL, conversions) |
| **Email** | Open rates, click rates, booking rates per email in sequence |
| **Pipeline** | GHL pipeline stages, conversion by avatar type, boomerang tracking |

---

## What to Track That Most People Forget

| Metric | Why It Matters |
|--------|---------------|
| **Video completion rate** | If people aren't finishing the video, the gate kills leads |
| **Form-to-booking drop-off** | If people submit form but don't book, the booking page has friction |
| **Booking-to-show gap** | If show rate is <60%, reminder sequence needs work |
| **Avatar distribution** | Which avatar type books most? Closes most? Informs ad spend allocation |
| **Time to booking** | How long between ad click and booking? Same day = high intent |
| **Boomerang conversion** | % of 3-month boomerang leads who re-book and close |
| **Email engagement decay** | At which email in the nurture sequence do people stop opening? |
