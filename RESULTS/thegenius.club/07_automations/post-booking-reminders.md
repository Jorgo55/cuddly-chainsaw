# Post-Booking Reminder Flow (Show-Up Maximizer)

**Trigger**: Lead completes booking on calendar
**Goal**: Maximize show-up rate (target: 70%+)
**Platform**: GHL automation

---

## Message 1: Instant Confirmation (Email + SMS)

**Trigger**: Booking confirmed
**Delay**: Immediate

### Email

**Subject**: You're booked — here's what to expect
**From**: Andy Murphy <andy@thegenius.club>

---

Hey {first_name},

Your Infrastructure Audit call is confirmed.

**Date**: {booking_date}
**Time**: {booking_time} ({timezone})
**Platform**: Google Meet — {meet_link}
**Duration**: 30 minutes

Here's what we'll cover:

1. Your business operations — how things actually run day-to-day
2. A mini Infrastructure Audit — identifying the gaps investors see
3. The honest diagnosis — why investors keep saying no
4. A clear path forward — what to fix and in what order

**One thing**: come prepared to be honest about your business. The more real you are, the more useful this call will be. We're not here to judge — we're here to diagnose.

Talk soon,
Andy

P.S. Can't make it? Reschedule here: {reschedule_link}

---

### SMS

Your audit call is confirmed for {booking_date} at {booking_time}. Meet link in your email. Come ready to be honest about your business — that's how you get the real answers. — Andy

---

## Message 2: Value Bridge (Email)

**Trigger**: Booking confirmed
**Delay**: 3-4 hours after booking

### Email

**Subject**: Before your call — read this (2 min)
**From**: Andy Murphy <andy@thegenius.club>

---

{first_name},

Quick thought before your call.

Most founders I talk to have spent $5K-$15K trying to fix their fundraising. Pitch deck consultants. Networking events. Accelerator applications.

None of it worked because they were fixing the wrong thing.

Investors don't evaluate pitches. They evaluate businesses. Specifically:
- Can this run without the founder in every room?
- Are there real systems or just one person holding it together?
- Would this survive a bad quarter?

That's what we'll look at on your call. The stuff behind the slides.

See you soon,
Andy

---

## Message 3: Day Before (SMS)

**Trigger**: Booking time - 24 hours
**Delay**: 24 hours before call

### SMS

Hey {first_name} — your audit call is tomorrow at {booking_time}. Quick reminder: think about what happens to your business if you can't work for a month. That's what investors think about too. See you tomorrow. — Andy

---

## Message 4: Morning Of (SMS)

**Trigger**: Day of booking, 9:00 AM local time
**Delay**: Morning of call day

### SMS

Today's the day, {first_name}. Your audit call is at {booking_time}. Google Meet link: {meet_link}. 30 minutes. The most honest conversation you'll have about your business this month. — Andy

---

## Message 5: 1 Hour Before (SMS)

**Trigger**: Booking time - 60 minutes
**Delay**: 60 minutes before call

### SMS

{first_name} — we're 1 hour out. {meet_link}. See you there.

---

## Automation Logic

```
[Booking Complete]
    ├── Instant: Email (confirmation) + SMS (confirmation)
    ├── +3-4 hrs: Email (value bridge)
    ├── -24 hrs: SMS (day before reminder)
    ├── Day of 9AM: SMS (morning of)
    └── -1 hr: SMS (final nudge)

    IF no-show → trigger No-Show Flow
    IF attended → trigger Post-Call Flow
```
