# Post-Call Nurture (Attended But Didn't Buy)

**Trigger**: Call completed, lead marked as "not closed" in GHL
**Goal**: Convert to purchase or seed the 3-month boomerang
**Platform**: GHL automation
**Duration**: 14 days, 4 emails

---

## Email 1: Recap + Thank You (Day 1)

**Delay**: 24 hours after call
**Subject**: What we found in your audit

---

Hey {first_name},

Thanks for the honest conversation yesterday.

Here's a quick recap of what came up:

**What investors see when they look at {company_name}:**
- [Salesperson to customize: 2-3 specific gaps identified on the call]

**What needs to change (in order):**
1. [Most critical fix from the call]
2. [Second priority]
3. [Third priority]

These aren't opinions. They're the same structural issues we see in every founder who's been hearing "not yet" for 18+ months.

The path from here is clear. The question is whether you want to walk it alone — or with a system that's been built for exactly this.

If you're ready to talk about next steps, reply to this email or book a follow-up here:

[Book a Follow-Up →]

— Andy

*Note to sales team: customize the bracketed sections based on what was discussed on the call. This email should feel personal, not templated.*

---

## Email 2: Social Proof (Day 3)

**Delay**: 48 hours after Email 1
**Subject**: What the funded founders did differently

---

{first_name},

The gaps we identified in your business aren't unique to you. Every founder in the $250K-$2M range hits similar walls.

The ones who get past it do something different: they stop trying to pitch their way to funding and start building their way to it.

That's exactly what the 90-Day Funding Machine is designed around. Not a course. Not theory. A structured sprint that transforms the gaps investors are flagging into the infrastructure they're looking for.

When you're ready, we're here:

[Book a Follow-Up →]

— Andy

---

## Email 3: Value Drop (Day 7)

**Delay**: 4 days after Email 2
**Subject**: One thing to think about this week

---

{first_name},

Here's something worth 10 minutes:

**List everything that requires YOUR decision.**

Every escalation. Every approval. Every judgment call. The things that would stall if you were unreachable for a week.

Write them down. Look at the list.

That's the gap we're talking about. That list is what investors are seeing when they look past your pitch deck.

The question is: are you going to close those gaps alone, or with a system built for exactly this?

— Andy

---

## Email 4: Soft Close (Day 14)

**Delay**: 7 days after Email 3
**Subject**: The offer still stands

---

{first_name},

It's been two weeks since our call.

I'm not going to pretend I know what your days look like right now. But I do know this: the structural gaps we identified don't fix themselves. And every month that passes is another month of burned runway on a business that's not getting more fundable.

If you've decided to fix it on your own — respect. I hope it works.

If you want help — the Infrastructure Audit gave you the diagnosis. The Genius Club gives you the treatment. And the 90-Day Funding Machine is the fast track.

[Learn More About the Program →]

If you have questions, reply to this email. I read every one.

— Andy

---

## Automation Logic

```
[Call Completed — Not Closed]
    ├── +24 hrs: Email 1 (recap — REQUIRES SALES TEAM CUSTOMIZATION)
    ├── +3 days: Email 2 (social proof)
    ├── +7 days: Email 3 (value drop)
    └── +14 days: Email 4 (soft close)

    IF purchases at any point → STOP sequence, move to Onboarding
    IF no action after 14 days → move to 3-Month Boomerang list
```
