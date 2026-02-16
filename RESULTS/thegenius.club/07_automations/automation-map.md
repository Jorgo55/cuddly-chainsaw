# Automation Map — All Triggers, Conditions, Branches

---

## Master Flow

```
                        ┌─────────────┐
                        │  COLD EMAIL  │
                        │  (50K list)  │
                        └──────┬──────┘
                               │ click
                        ┌──────▼──────┐         ┌──────────────┐
                        │   META AD   │         │  LINKEDIN    │
                        │             │         │  ORGANIC     │
                        └──────┬──────┘         └──────┬───────┘
                               │ click                  │ click
                        ┌──────▼────────────────────────▼──────┐
                        │                                       │
                        │          LANDING PAGE                 │
                        │     thegenius.club                    │
                        │                                       │
                        │  [Video → Gated Form]                │
                        │                                       │
                        └──────────────────┬───────────────────┘
                                           │
                              ┌────────────▼────────────┐
                              │     FORM SUBMITTED      │
                              │  → GHL Contact Created  │
                              │  → Tag: funnel-lead     │
                              └────────────┬────────────┘
                                           │
                              ┌────────────▼────────────┐
                              │    BOOKING PAGE         │
                              │  Qual Qs + Calendar     │
                              └─────┬──────────┬────────┘
                                    │          │
                            ┌───────▼───┐  ┌───▼────────────┐
                            │  BOOKED   │  │  NOT BOOKED    │
                            │           │  │  (2hr+ delay)  │
                            └─────┬─────┘  └───────┬────────┘
                                  │                 │
                   ┌──────────────▼──┐    ┌────────▼─────────┐
                   │  POST-BOOKING   │    │  LEAD NURTURE    │
                   │  REMINDERS      │    │  (6 emails/9d)   │
                   │  (5 messages)   │    └────────┬─────────┘
                   └────────┬───────┘             │
                            │                     │ books?
                   ┌────────▼───────┐    ┌────────▼─────────┐
                   │   CALL DAY     │    │  YES → post-     │
                   │                │    │  booking flow     │
                   └──┬──────────┬──┘    └──────────────────┘
                      │          │
              ┌───────▼──┐  ┌───▼────────┐
              │ ATTENDED  │  │  NO-SHOW   │
              │           │  │            │
              └─────┬─────┘  └──────┬─────┘
                    │               │
           ┌───────▼──────┐  ┌─────▼──────────┐
           │   ON CALL    │  │  NO-SHOW       │
           │              │  │  FOLLOW-UP     │
           └──┬────────┬──┘  │  (3 messages)  │
              │        │     └────────┬────────┘
      ┌───────▼──┐ ┌───▼───┐        │
      │  CLOSED  │ │  NOT  │   reschedules?
      │  (SALE)  │ │ CLOSED│        │
      └─────┬────┘ └──┬────┘  ┌─────▼──────┐
            │         │       │ YES → back  │
            │         │       │ to booking  │
            │         │       └────────────┘
    ┌───────▼──┐  ┌───▼──────────┐
    │ONBOARDING│  │ POST-CALL    │
    │          │  │ NURTURE      │
    │  (GHL   │  │ (4 emails/   │
    │  pipeline│  │  14 days)    │
    │  change) │  └──────┬───────┘
    └──────────┘         │
                         │ 14 days, no buy
                   ┌─────▼──────────┐
                   │  3-MONTH       │
                   │  BOOMERANG     │
                   │  (3 emails)    │
                   └──────┬─────────┘
                          │
                   ┌──────▼─────────┐
                   │  LONG-TERM     │
                   │  BROADCASTS    │
                   │  (weekly)      │
                   └────────────────┘
```

---

## Trigger-to-Sequence Matrix

| Trigger Event | Sequence | Duration | Messages | CRM Tag |
|--------------|----------|----------|:--------:|---------|
| Form submitted, no booking (2hr+) | Lead Nurture | 9 days | 6 emails | `nurture-active` |
| Booking completed | Post-Booking Reminders | Until call | 2 emails + 3 SMS | `booked` |
| No-show (missed call) | No-Show Follow-Up | 3 days | 1 SMS + 2 emails | `no-show` |
| Call attended, not closed | Post-Call Nurture | 14 days | 4 emails | `called-not-closed` |
| 90 days post-call, not converted | 3-Month Boomerang | 7 days | 3 emails | `boomerang-active` |
| Ongoing (all non-purchased leads) | Weekly Broadcasts | Ongoing | 1/week | `broadcast-list` |

---

## CRM Tag Logic

| Action | Tags Added | Tags Removed |
|--------|-----------|-------------|
| Form submit | `funnel-lead` | — |
| Booking complete | `booked`, `avatar:{type}` | `nurture-active` |
| Call attended | `call-completed` | `booked` |
| Closed (purchased) | `customer`, `genius-club-member` | all nurture tags |
| Not closed (post-call) | `called-not-closed` | `call-completed` |
| No-show | `no-show` | `booked` |
| Boomerang sent | `boomerang-active` | `called-not-closed` |
| Disqualified (<$250K) | `disqualified` | — |
| Unsubscribed | `unsubscribed` | all sequence tags |

---

## Sequence Conflict Rules

| Situation | Rule |
|-----------|------|
| Lead in Nurture + books call | STOP Nurture → START Post-Booking |
| Lead in No-Show + reschedules | STOP No-Show → START Post-Booking (reset) |
| Lead in Post-Call + purchases | STOP Post-Call → START Onboarding |
| Lead in Boomerang + books call | STOP Boomerang → START Post-Booking |
| Lead in ANY sequence + unsubscribes | STOP ALL sequences immediately |

**Rule**: A lead should never be in more than one active sequence at a time. New triggers override old sequences.

---

## GHL Implementation Notes

| Configuration | Detail |
|---------------|--------|
| Workflows | 6 separate workflows (one per sequence) |
| Triggers | Based on pipeline stage changes + tag additions |
| Wait steps | Use GHL "wait" actions with time delays |
| Branching | Use "if/else" on tags for conflict resolution |
| Email sender | Andy Murphy <andy@thegenius.club> |
| SMS sender | Same GHL number for all SMS |
| Timezone | Respect lead's detected timezone for send times |
| Throttling | No more than 1 email + 1 SMS per day to any lead |
| Compliance | Unsubscribe link in every email, STOP keyword for SMS |

---

## KPIs to Track Per Sequence

| Sequence | Primary Metric | Target |
|----------|---------------|--------|
| Post-Booking Reminders | Show-up rate | 70%+ |
| Lead Nurture | Booking conversion rate | 15%+ |
| No-Show Follow-Up | Reschedule rate | 30%+ |
| Post-Call Nurture | Purchase rate | 10%+ |
| 3-Month Boomerang | Re-booking rate | 15%+ |
| Weekly Broadcasts | Click rate | 3%+ |
