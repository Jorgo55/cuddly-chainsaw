# STEP 7: EMAIL & SMS AUTOMATIONS

**Build the machine that runs without you.**

**Depends on**: Step 6 (Funnel Build) complete → funnel live + CRM connected
**Produces**: `RESULTS/07_automations/`
**Agent**: `email-sequence`

---

## What This Step Does

Build all automated email/SMS sequences that trigger from funnel actions. Uses templates from `templates/` adapted with offer data and avatar language.

---

## Input

From `RESULTS/03_offer/`:
- Offer package (for value props, bonuses, guarantee language)

From `RESULTS/02_avatars/`:
- Avatar voice lines and pain points (for personalization)

From `RESULTS/04_copy/`:
- Tone and messaging (for consistency)

Templates in `templates/`:
- `appointment-reminder-templates.md`
- `lead-magnet-delivery-nurture-flow.md`
- `broadcast-email-strategy.md`
- `ecom/` (additional flow references — welcome, abandonment, testimonials, re-engagement, broadcasts)

---

## Sequences to Build (in Order)

### 7a. Post-Booking Reminder Flow (Show-Up Maximizer)
Template: `templates/appointment-reminder-templates.md`

| Timing | Channel | Content |
|--------|---------|---------|
| Instant | Email + SMS | Confirm booking + Meet link + social proof |
| 3-4 hrs | Email | Fast results examples / case studies |
| Day before | SMS | Personal reminder + expectations |
| Morning of | SMS | Recent success story + confidence |
| 1 hr before | SMS | Final friendly nudge |

### 7b. Lead Nurture (Entered Funnel But Didn't Book)
Template: `templates/lead-magnet-delivery-nurture-flow.md`

| Day | Content |
|-----|---------|
| 0 | Deliver value + set expectations |
| 1 | Myth-busting: why most fundraising fails |
| 3 | Case study / social proof |
| 5 | Objection handling |
| 7 | Direct CTA: book a call |
| 9 | FOMO / last chance |

### 7c. No-Show Follow-Up
| Timing | Channel | Content |
|--------|---------|---------|
| 15 min after | SMS | "Hey, we missed you — want to reschedule?" |
| 1 day after | Email | Reschedule link + brief value reminder |
| 3 days after | Email | Social proof + last reschedule offer |

### 7d. Post-Call Nurture (Didn't Buy)
| Day | Content |
|-----|---------|
| 1 | Thank you + recap of key insights from the call |
| 3 | Case study of similar founder who joined |
| 7 | "Still thinking about funding? Here's what changed for others" |
| 14 | Soft nudge + bonus/incentive if applicable |

### 7e. 3-Month Boomerang (Rejected Leads)
| Month | Content |
|-------|---------|
| 3 | "Did you get your funding? If not — let's talk again." |
| 3 + 3 days | Case study: founder who came back and succeeded |
| 3 + 7 days | "The offer still stands. Book when ready." |

### 7f. Weekly Broadcast Strategy (Ongoing)
Template: `templates/broadcast-email-strategy.md`

| Day | Theme |
|-----|-------|
| Monday | Social proof (founder transformations) |
| Tuesday | Value/education (fundraising myths, mistakes) |
| Wednesday | Process demo (audit framework, what we check) |
| Thursday | Soft sell (limited call slots, book now) |
| Friday | Story (Andy's journey, lessons, philosophy) |

---

## Email/SMS Rules

1. Every email has ONE goal — don't dilute
2. Every email includes a CTA (even value emails: "If you're ready…")
3. Subject lines: curiosity or benefit, never clickbait
4. SMS: max 160 chars, conversational, direct
5. Tone matches messaging DNA: confident, direct, no fluff
6. Sell the FUNDING angle in nurture — not the club
7. Urgency/scarcity only when genuine

---

## Output

Save to `RESULTS/07_automations/`:
- `post-booking-reminders.md` — full sequence with exact copy
- `lead-nurture.md` — full 6-email sequence
- `no-show-followup.md` — full sequence
- `post-call-nurture.md` — full sequence
- `boomerang-3month.md` — full sequence
- `weekly-broadcasts.md` — 4 weeks of broadcast templates
- `automation-map.md` — visual map of all triggers, conditions, branches

---

## Done When

- [ ] All 6 sequences written with exact copy (subject, body, CTA per email)
- [ ] All SMS messages written (under 160 chars each)
- [ ] Automation logic documented (triggers, conditions, branches)
- [ ] 4 weeks of broadcast templates ready
- [ ] All outputs saved to `RESULTS/07_automations/`

→ Proceed to Step 8 (Traffic)
