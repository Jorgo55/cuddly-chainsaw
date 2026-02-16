# 3-Month Boomerang Sequence (Rejected Leads)

**Trigger**: 90 days after call (lead went through Post-Call Nurture and didn't convert)
**Goal**: Re-engage leads who tried fundraising alone and failed
**Platform**: GHL automation
**Duration**: 7 days, 3 touchpoints

---

## The Psychology Behind This Sequence

These leads:
- Heard "you're not ready" on the call
- Rejected the diagnosis (partially or fully)
- Went back to fundraising on their own
- Had 3 more months of "soft nos"
- Are now MORE receptive because the seed was planted and reality confirmed it

The boomerang is the highest-conversion sequence in the system. These leads already know Andy, already heard the diagnosis, and have now experienced the proof firsthand.

---

## Email 1: The Check-In (Month 3)

**Delay**: 90 days after original call
**Subject**: Did you get your funding?
**From**: Andy Murphy <andy@thegenius.club>

---

Hey {first_name},

It's been about 3 months since we talked about {company_name} and your fundraising.

Honest question: did you close your round?

If yes — congratulations. Genuinely. That's great news.

If not — we should talk again. The gaps we identified on our call haven't disappeared. And you've now got 3 more months of data confirming what we saw.

Same offer: 30-minute call, free, we look at what's changed and what hasn't.

[Book a Follow-Up Call →]

— Andy

---

## Email 2: Case Study / Pattern (Month 3 + 3 days)

**Delay**: 3 days after Email 1
**Subject**: The founder who came back

---

{first_name},

Most founders who hear "you're not ready" react the same way: "Yes I am."

Then they spend 3 more months pitching. 3 more months of "soft nos." 3 more months of burning runway.

When they come back, the conversation is completely different. They're not defensive anymore. They're ready.

The diagnosis is the same. The path forward is the same. But now they're listening — because 3 months of reality did what I couldn't do in 30 minutes.

If that sounds familiar, the call is still free:

[Book a Follow-Up Call →]

— Andy

---

## Email 3: Last Touch (Month 3 + 7 days)

**Delay**: 4 days after Email 2
**Subject**: Open invitation

---

{first_name},

Last note on this.

The Infrastructure Audit we discussed 3 months ago is still available. The gaps we identified are still the same gaps investors are seeing.

The only thing that's changed is your runway — you have 3 months less of it.

When you're ready, book the call:

[Book a Follow-Up Call →]

No expiration. No pressure. But the math gets harder every month.

— Andy

---

## Automation Logic

```
[90 Days After Original Call — Lead Not Converted]
    ├── Day 90: Email 1 (check-in)
    ├── Day 93: Email 2 (case study / pattern)
    └── Day 97: Email 3 (last touch)

    IF books call → move to Post-Booking Flow
    IF purchases → move to Onboarding
    IF no action → move to Long-Term Nurture list (monthly broadcasts)

    OPTIONAL: Run a second boomerang at Month 6 (same structure,
    adjusted copy: "It's been 6 months...")
```

---

## Boomerang Conversion Expectations

| Metric | Conservative | Optimistic |
|--------|:----------:|:---------:|
| Open rate (Email 1) | 35%+ | 45%+ |
| Reply rate | 5%+ | 10%+ |
| Re-booking rate | 10%+ | 20%+ |
| Close rate (re-booked) | 50%+ | 65%+ |

**Why these are higher than cold metrics**: These leads already know Andy, already heard the diagnosis, and now have empirical evidence (3 more months of failure) confirming what we told them. The resistance has been dissolved by reality.
