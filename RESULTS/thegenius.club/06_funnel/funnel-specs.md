# Funnel Specs — The Genius Club

---

## Funnel Architecture

```
Meta Ad / Cold Email
        ↓
   Landing Page (thegenius.club)
        ↓
   [3-min Video — gated]
        ↓
   Lead Capture Form
        ↓
   Booking Page (calendar + qual questions)
        ↓
   Thank You Page (confirmation + bonus video)
        ↓
   [Automated: email + SMS confirmation]
        ↓
   [Automated: 24hr prep email]
        ↓
   [Automated: 30min reminder]
        ↓
   Google Meet Call (salesperson)
        ↓
   [Post-call: follow-up sequence OR boomerang]
```

**Type**: Simple Lead-to-Booking. NOT VSL. NOT questionnaire-first.
**Why**: The qualification call IS the selling point. The "you're not ready" reveal happens live, not in a video.

---

## Page 1: Landing Page

### URL
`thegenius.club` (root domain)

### Layout (Mobile-First)

```
┌─────────────────────────────────┐
│         HEADER / NAV            │
│  Logo (left)    [No menu items] │
├─────────────────────────────────┤
│          HERO SECTION           │
│                                 │
│  H1: Get Funding for Your       │
│      Business.                  │
│                                 │
│  Sub: For founders making       │
│  $250K+ who keep hearing        │
│  "not yet" from investors.      │
│                                 │
│  Supporting: Book a free        │
│  Infrastructure Audit call...   │
│                                 │
│  [Book Your Free Audit Call →]  │
├─────────────────────────────────┤
│      PROBLEM AGITATION          │
│                                 │
│  H2: You've Done Everything     │
│      Right. Except One Thing.   │
│                                 │
│  Body: 3 paragraphs             │
│  (profitable but not fundable,  │
│  10+ meetings, deck isn't why)  │
├─────────────────────────────────┤
│         THE REFRAME             │
│                                 │
│  H2: Investors Don't Fund       │
│      Pitches. They Fund         │
│      Machines.                  │
│                                 │
│  Bullet checklist of what       │
│  investors actually evaluate    │
├─────────────────────────────────┤
│       VIDEO SECTION             │
│                                 │
│  H2: Watch This Before You      │
│      Book (3 min)               │
│                                 │
│  [VIDEO PLAYER — 16:9]          │
│  Progress bar visible           │
│  Gated: form hidden until       │
│  video reaches 80% completion   │
├─────────────────────────────────┤
│      MECHANISM SECTION          │
│                                 │
│  H2: The Business               │
│      Infrastructure Audit       │
│                                 │
│  5 sub-components listed:       │
│  • Founder Dependency Score     │
│  • Operational Repeatability    │
│  • Investor Red Flag Map        │
│  • Team Depth Assessment        │
│  • Scale Readiness Rating       │
├─────────────────────────────────┤
│     WHO THIS IS FOR             │
│                                 │
│  Two columns:                   │
│  ✓ This Is For You If:          │
│  ✗ This Is NOT For You If:      │
├─────────────────────────────────┤
│   WHAT HAPPENS ON THE CALL      │
│                                 │
│  4 numbered steps with icons    │
├─────────────────────────────────┤
│      CREDIBILITY BAR            │
│                                 │
│  Andy headshot + brief bio      │
│  "23 years • IPO founders •     │
│  Infrastructure audit pioneer"  │
├─────────────────────────────────┤
│        FINAL CTA                │
│                                 │
│  H2: Find Out Why Investors     │
│      Really Say No.             │
│                                 │
│  [Book Your Free Audit Call →]  │
│                                 │
│  Micro: No pitch deck review.   │
│  No generic advice. Just truth. │
├─────────────────────────────────┤
│         FOOTER                  │
│  © The Genius Club              │
│  Privacy Policy | Terms         │
└─────────────────────────────────┘
```

### Video Gating Logic

```javascript
// Pseudocode
const video = document.querySelector('#hero-video');
const form = document.querySelector('#lead-capture-form');

form.style.display = 'none'; // Hidden initially

video.addEventListener('timeupdate', () => {
  const percentWatched = (video.currentTime / video.duration) * 100;
  if (percentWatched >= 80) {
    form.style.display = 'block';
    form.scrollIntoView({ behavior: 'smooth' });
  }
});
```

### Lead Capture Form Fields

| Field | Type | Required | Validation |
|-------|------|:--------:|------------|
| First Name | text | YES | Min 2 chars |
| Last Name | text | YES | Min 2 chars |
| Email | email | YES | Valid email format |
| Phone | tel | YES | Valid phone (international) |

**On Submit**:
1. POST to GHL webhook (creates contact + tags: `funnel-lead`, `thegenius-club`)
2. Redirect to booking page
3. Trigger GHL automation: confirmation email + SMS

### Technical Requirements

| Requirement | Spec |
|-------------|------|
| Load time | < 3 seconds (mobile) |
| Mobile responsive | YES — mobile-first design |
| Video hosting | Self-hosted or Vimeo Pro (no YouTube — no distracting recommendations) |
| Analytics | Google Analytics 4 + Meta Pixel |
| SSL | Required (HTTPS) |
| No-JS fallback | Form should be visible if JS disabled (graceful degradation) |

---

## Page 2: Booking Page

### URL
`thegenius.club/book` or `/booking`

### Layout

```
┌─────────────────────────────────┐
│         HEADER                  │
│  Logo (left)                    │
├─────────────────────────────────┤
│      PAGE HEADER                │
│                                 │
│  H1: You're Almost There.       │
│                                 │
│  Sub: Book your free            │
│  Infrastructure Audit call.     │
├─────────────────────────────────┤
│   QUALIFICATION QUESTIONS       │
│                                 │
│  Q1: Annual revenue/profit      │
│  [Dropdown: ranges]             │
│                                 │
│  Q2: Full-time employees        │
│  [Dropdown: ranges]             │
│                                 │
│  Q3: Investor meetings (12 mo)  │
│  [Dropdown: ranges]             │
│                                 │
│  Q4: Biggest fundraising        │
│      challenge                  │
│  [Radio buttons + Other]        │
│                                 │
│  Q5: How soon raising capital   │
│  [Dropdown: urgency levels]     │
├─────────────────────────────────┤
│   PRE-CALENDAR COPY             │
│                                 │
│  "Based on your answers..."     │
│  Expectation setting bullets    │
├─────────────────────────────────┤
│      CALENDAR WIDGET            │
│                                 │
│  [Embedded booking calendar]    │
│  30-minute time slots           │
│  Timezone auto-detection        │
├─────────────────────────────────┤
│   BELOW CALENDAR                │
│                                 │
│  "What Happens After You Book"  │
│  4 numbered steps               │
├─────────────────────────────────┤
│         FOOTER                  │
└─────────────────────────────────┘
```

### Qualification Logic

| Q1 Answer | Action |
|-----------|--------|
| Under $100K | Redirect to disqualification page |
| $100K - $250K | Redirect to disqualification page |
| $250K+ | Continue to calendar |

| Q4 Answer | CRM Tag (for salesperson) |
|-----------|--------------------------|
| Can't get meetings | `avatar:unknown` |
| Getting meetings but rejected | `avatar:prisoner` |
| Don't know what investors want | `avatar:prisoner` |
| Running both is killing me | `avatar:red-liner` |
| Other | `avatar:unknown` |

**Auto-detect Bottleneck**: If Q2 = "Just me" or Q5 = "Exploring", may indicate bottleneck pattern. Tag for salesperson awareness.

### Calendar Integration

| Spec | Detail |
|------|--------|
| Platform | GHL calendar widget |
| Duration | 30-minute slots |
| Buffer | 15 min between calls |
| Availability | Mon-Fri, configurable hours |
| Meeting type | Google Meet (auto-generated link) |
| Timezone | Auto-detect from browser |
| Confirmation | Immediate email + SMS via GHL |

### Disqualification Page

**URL**: `thegenius.club/not-yet`

```
┌─────────────────────────────────┐
│  H1: We're Not the Right        │
│      Fit — Yet.                 │
│                                 │
│  Body: Honest, respectful       │
│  explanation. Recommends         │
│  focusing on $250K revenue       │
│  first. "Come back when ready." │
│                                 │
│  [Optional: email capture for   │
│   future nurture list]          │
│                                 │
│  [Back to thegenius.club]       │
└─────────────────────────────────┘
```

---

## Page 3: Thank You Page

### URL
`thegenius.club/confirmed` or `/thank-you`

### Layout

```
┌─────────────────────────────────┐
│         HEADER                  │
├─────────────────────────────────┤
│      CONFIRMATION               │
│                                 │
│  H1: You're Booked. ✓           │
│                                 │
│  Date: [Dynamic]                │
│  Time: [Dynamic, local TZ]     │
│  Platform: Google Meet          │
│  (link in confirmation email)   │
├─────────────────────────────────┤
│     WHAT HAPPENS NEXT           │
│                                 │
│  Timeline: before → during →    │
│  after the call                 │
│  4 numbered steps               │
├─────────────────────────────────┤
│      BONUS VIDEO                │
│                                 │
│  H2: Watch This Before Your     │
│      Call (2 min)               │
│                                 │
│  [VIDEO PLAYER]                 │
│  NOT gated — they already       │
│  booked                         │
├─────────────────────────────────┤
│    SHOW-UP MOTIVATION           │
│                                 │
│  "Most founders never find out  │
│   the real reason..."           │
│  Body text: why this call       │
│  matters                        │
├─────────────────────────────────┤
│    LOGISTICS REMINDER           │
│                                 │
│  Call details repeated           │
│  Reschedule link                │
├─────────────────────────────────┤
│   SOCIAL PROOF (WHEN READY)     │
│                                 │
│  [HIDDEN until testimonials     │
│   exist — no fake quotes]       │
├─────────────────────────────────┤
│         FOOTER                  │
└─────────────────────────────────┘
```

### Thank You Page Requirements

| Requirement | Detail |
|-------------|--------|
| Dynamic booking details | Pulled from GHL booking confirmation |
| Bonus video | Self-hosted or Vimeo, NOT gated |
| Reschedule link | From GHL calendar system |
| Social proof section | Hidden by default, unhide via CMS when testimonials ready |
| No additional CTA | They already booked — don't distract |

---

## Integration Map

```
                    ┌──────────────┐
                    │   META ADS   │
                    │  (Pixel fire  │
                    │  on all pages)│
                    └──────┬───────┘
                           │
                    ┌──────▼───────┐
                    │ LANDING PAGE │
                    │              │
                    │ • GA4 event  │
                    │ • Meta Pixel │
                    │ • Video play │
                    │   tracking   │
                    └──────┬───────┘
                           │ Form submit
                    ┌──────▼───────┐
                    │   GHL CRM    │
                    │              │
                    │ • Contact    │
                    │   created    │
                    │ • Tags added │
                    │ • Automation │
                    │   triggered  │
                    └──────┬───────┘
                           │
                    ┌──────▼───────┐
                    │ BOOKING PAGE │
                    │              │
                    │ • Qual Qs    │
                    │   → CRM tags │
                    │ • Calendar   │
                    │   → GHL     │
                    │ • Meet link  │
                    │   generated  │
                    └──────┬───────┘
                           │
                    ┌──────▼───────┐
                    │  THANK YOU   │
                    │              │
                    │ • Conversion │
                    │   event fire │
                    │ • Meta CAPI  │
                    │   (server)   │
                    └──────┬───────┘
                           │
                    ┌──────▼───────┐
                    │ GHL AUTOMATIONS│
                    │              │
                    │ • Confirm    │
                    │   email+SMS  │
                    │ • 24hr prep  │
                    │ • 30min      │
                    │   reminder   │
                    │ • Post-call  │
                    │   sequences  │
                    └──────────────┘
```

---

## Tracking & Pixels

| Event | Where | Platform | Details |
|-------|-------|----------|---------|
| PageView | All pages | GA4 + Meta Pixel | Standard pageview |
| VideoStart | Landing page | GA4 | Video play begins |
| VideoComplete | Landing page | GA4 | Video reaches 80% |
| FormVisible | Landing page | GA4 | Form appears (post-gate) |
| Lead | Landing page | GA4 + Meta Pixel | Form submitted |
| QualComplete | Booking page | GA4 | Qual questions answered |
| BookingComplete | Booking page | GA4 + Meta CAPI | Calendar booked — **PRIMARY CONVERSION EVENT for Meta** |
| ThankYouView | Thank you page | GA4 + Meta Pixel | Page loaded |
| BonusVideoStart | Thank you page | GA4 | Bonus video play begins |

### Meta Conversion API (CAPI)

- Server-side event for BookingComplete → ensures tracking even with ad blockers
- Deduplicate with browser pixel using event_id
- Send: email (hashed), phone (hashed), first_name, last_name

---

## Design Specifications

### Colors

| Usage | Color | Hex |
|-------|-------|-----|
| Primary background | Dark navy / near-black | `#0A0E1A` or `#111827` |
| Secondary background | Dark gray | `#1F2937` |
| Text (primary) | White | `#FFFFFF` |
| Text (secondary) | Light gray | `#9CA3AF` |
| Accent / CTA | Gold or amber | `#F59E0B` |
| CTA hover | Lighter gold | `#FBBF24` |
| Error / rejection | Red | `#EF4444` |
| Success / confirmation | Green | `#10B981` |

### Typography

| Usage | Font | Size (mobile) | Size (desktop) |
|-------|------|:-------------:|:--------------:|
| H1 | Inter Bold or equivalent sans-serif | 28px | 48px |
| H2 | Inter Bold | 22px | 36px |
| Body | Inter Regular | 16px | 18px |
| Small / micro | Inter Regular | 14px | 14px |
| CTA button | Inter Bold | 16px | 18px |

### Button Style

```css
.cta-primary {
  background: #F59E0B;
  color: #0A0E1A;
  font-weight: 700;
  padding: 16px 32px;
  border-radius: 8px;
  border: none;
  cursor: pointer;
  font-size: 18px;
  transition: background 0.2s;
}
.cta-primary:hover {
  background: #FBBF24;
}
```

### Layout

- Max width: 720px for content (centered)
- Padding: 24px mobile, 48px desktop
- Section spacing: 64px between sections
- Mobile-first: single column, no side-by-side elements under 768px

---

## Deployment Notes

| Item | Detail |
|------|--------|
| Domain | thegenius.club (already owned) |
| Hosting | Custom — we control the stack |
| SSL | Cloudflare or Let's Encrypt |
| CDN | Cloudflare (free tier sufficient at launch) |
| Video hosting | Vimeo Pro (no YT branding/recs) or self-hosted |
| DNS | Point to hosting, www redirect to apex |
| Staging | Build on staging subdomain first (staging.thegenius.club) |
| GHL integration | Webhook URL from GHL for form submission |
| Calendar embed | GHL calendar widget embed code |
