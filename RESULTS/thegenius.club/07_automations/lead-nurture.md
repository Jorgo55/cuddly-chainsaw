# Lead Nurture Sequence (Captured But Didn't Book)

**Trigger**: Lead submits form on landing page BUT does not complete booking within 2 hours
**Goal**: Convert lead to booked call
**Platform**: GHL automation
**Duration**: 9 days, 6 emails

---

## Email 1: Delivery + Expectation (Day 0)

**Delay**: 2 hours after form submit (if no booking)
**Subject**: You started something — let's finish it
**From**: Andy Murphy <andy@thegenius.club>

---

Hey {first_name},

You took the first step — you signed up to find out why investors keep saying no.

But you didn't book the call yet.

I get it. You're busy. You've been burned before. Another "fundraising expert" is the last thing you need.

Here's the thing: this isn't a pitch deck review. It's not a coaching session. It's a 30-minute diagnostic where we look at your business through the investor's lens and tell you exactly what they see.

No cost. No commitment. Just clarity.

[Book Your Free Audit Call →]

— Andy

---

## Email 2: Myth Bust (Day 1)

**Delay**: 24 hours after Email 1
**Subject**: The #1 myth killing your fundraise

---

{first_name},

The myth: "If I just fix my pitch deck, investors will say yes."

The truth: Investors look past the deck in the first 5 minutes. They're evaluating:
- Can this business survive without you?
- Are there real systems or just heroic effort?
- Would $1M in funding make this bigger — or just louder?

I've watched 10+ pitch deck consultants deliver "perfect" decks that still got "soft nos." The deck was never the problem.

The Infrastructure Audit shows you what actually is.

[Book Your Free Audit Call →]

— Andy

---

## Email 3: Social Proof / Pattern (Day 3)

**Delay**: 48 hours after Email 2
**Subject**: Every founder who got funded did this first

---

{first_name},

After 23 years working with founders, I've noticed a pattern:

The ones who get funded aren't smarter or luckier. They just did one thing differently — they stopped pitching and fixed the business behind the pitch.

They addressed founder dependency. Built real systems. Created a team that could operate without them in every meeting.

Then, when they went back to investors, the conversation was completely different.

That's what the Infrastructure Audit reveals — the specific gaps between where you are and where investors need you to be.

30 minutes. Free. The most useful half-hour you'll spend this week.

[Book Your Free Audit Call →]

— Andy

---

## Email 4: Objection Handling (Day 5)

**Delay**: 48 hours after Email 3
**Subject**: "I don't have time for another program"

---

{first_name},

I hear this from every founder I talk to. And I agree with it.

You don't have time for another program, another course, another 12-month commitment.

That's not what this is.

The audit call is 30 minutes. You tell us about your business. We tell you what investors see. You leave with clarity you don't have right now.

If there's a fit after that, we talk about next steps. If there isn't, you still walk away with the most honest assessment of your fundraising readiness that anyone's ever given you.

Zero commitment beyond 30 minutes.

[Book Your Free Audit Call →]

— Andy

---

## Email 5: Direct CTA (Day 7)

**Delay**: 48 hours after Email 4
**Subject**: Let's just do this

---

{first_name},

5 days ago you signed up because you wanted to know why investors keep saying no.

You still don't have that answer.

I can give it to you in 30 minutes.

Free. On Google Meet. No pitch deck review. No generic advice. The real diagnosis.

[Book Your Free Audit Call →]

— Andy

---

## Email 6: Last Chance (Day 9)

**Delay**: 48 hours after Email 5
**Subject**: Last note from me (for now)

---

{first_name},

This is my last email about booking the audit call.

If the timing isn't right, I get it. Building a company while trying to raise capital is one of the hardest things a founder can do.

But here's what I know: the longer you wait to find out why investors say no, the more runway you burn on a business that isn't getting more fundable on its own.

When you're ready, the link is here:

[Book Your Free Audit Call →]

No expiration. No pressure. But the sooner you know, the sooner you can fix it.

— Andy

---

## Automation Logic

```
[Form Submit] → Wait 2 hours
    └── IF no booking:
        ├── Day 0: Email 1 (delivery)
        ├── Day 1: Email 2 (myth bust)
        ├── Day 3: Email 3 (social proof)
        ├── Day 5: Email 4 (objection)
        ├── Day 7: Email 5 (direct CTA)
        └── Day 9: Email 6 (last chance)

    IF booking at any point → STOP sequence, move to Post-Booking Flow
```
