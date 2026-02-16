# No-Show Follow-Up Sequence

**Trigger**: Lead booked a call but did not attend (marked no-show in GHL)
**Goal**: Reschedule the call
**Platform**: GHL automation

---

## Message 1: Immediate (SMS)

**Delay**: 15 minutes after missed call time

### SMS

Hey {first_name} — looks like we missed you on the call. No worries. Want to reschedule? Grab a new time here: {reschedule_link} — Andy

---

## Message 2: Day After (Email)

**Delay**: 24 hours after missed call

### Email

**Subject**: We saved your spot

---

Hey {first_name},

We missed you on yesterday's call. Life happens — no judgment.

Your audit slot is still available. The diagnosis we were going to run hasn't changed:

- What investors actually see when they look at your business
- The 3-5 structural gaps causing "soft nos"
- What to fix first (and what doesn't matter)

30 minutes. Free. Same deal.

[Reschedule Your Audit Call →]

— Andy

---

## Message 3: 3 Days After (Email)

**Delay**: 72 hours after missed call

### Email

**Subject**: Still want to know why investors say no?

---

{first_name},

Last check-in.

You booked the Infrastructure Audit call because you wanted answers. Those answers are still here.

If the timing was off, reschedule:

[Reschedule Your Audit Call →]

If you've decided it's not for you, that's fine too. But the question that brought you here — why investors keep saying no — won't answer itself.

— Andy

---

## Automation Logic

```
[No-Show Detected]
    ├── +15 min: SMS (reschedule nudge)
    ├── +24 hrs: Email (value reminder + reschedule)
    └── +72 hrs: Email (last check-in)

    IF reschedules → move to Post-Booking Flow (restart reminders)
    IF no action after 72 hrs → move to Lead Nurture list (long-term)
```
