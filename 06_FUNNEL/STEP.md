# STEP 6: FUNNEL BUILD

**Implement the pages. Copy is locked — just build.**

**Depends on**: Step 5 (Audit) complete → ALL creatives PASS in `RESULTS/05_audit/`
**Produces**: `RESULTS/06_funnel/`
**Agent**: `funnel-architect` (structure) + `page-builder` (implementation)

---

## What This Step Does

Build the actual funnel pages using the audited copy from Step 5. No copy changes here — if copy needs changing, go back to Step 4.

---

## Input

From `RESULTS/04_copy/` (audited + passed):
- Landing page copy
- Booking page copy
- Thank you page copy

From `00_CONTEXT/05_tech_and_automation.md`:
- Tech stack specs

---

## Funnel Architecture

```
Landing Page → Gated Video → Lead Capture → Booking + Qual Qs → Thank You Page
```

**NOT a VSL funnel.** The qualification call is the selling point.

---

## Page Specs

### 6a. Landing Page

| Element | Spec |
|---------|------|
| Hero | Headline + sub-headline + video player |
| Video | Gated — form hidden until video is watched |
| Form | First name, last name, email, phone |
| Social proof | Section below form (if available) |
| Design | Mobile-first, <3 sec load, clean, professional |
| Integration | Form submits to GHL CRM |

### 6b. Booking Page

| Element | Spec |
|---------|------|
| Calendar | Widget integration (Google Meet links, NOT Zoom) |
| Questions | Qualification questions at booking |
| Logic | Auto-cancel if answers disqualify |
| Confirmation | Clear confirmation step |
| Integration | Booking syncs to GHL + auto-generates Meet link |

### 6c. Thank You Page

| Element | Spec |
|---------|------|
| Confirmation | Booking details displayed |
| Bonus video | Player with "what to expect on the call" |
| Next steps | "What happens next" section |
| Meet link | Displayed or "link will be sent via email" |

---

## Tech Stack

- **CRM**: Go High Level (GHL)
- **Video calls**: Google Meet (free, no download)
- **Funnel pages**: Custom HTML/CSS (we're the dev team)
- **Video player**: Gated — completion triggers form visibility
- **Booking**: Calendar widget + GHL integration
- **Mobile-first**: Most traffic from Meta = mobile devices

---

## Design Rules

- Professional but not corporate (targeting founders, not enterprises)
- Clean whitespace, readable typography
- No stock photos, no fake testimonials
- Fast: under 3 seconds load time
- No design gimmicks — let the copy do the work
- No unnecessary JS frameworks — keep it lean

---

## Output

Save to `RESULTS/06_funnel/`:
- `landing-page/` — HTML, CSS, JS files
- `booking-page/` — HTML, CSS, integration config
- `thankyou-page/` — HTML, CSS, JS files
- `funnel-specs.md` — technical specs, integration points, deployment notes
- `screenshots/` — screenshots of each page (desktop + mobile)

---

## Done When

- [ ] All 3 pages built and functional
- [ ] Video gating works (form appears after video completion)
- [ ] Lead capture form submits to GHL
- [ ] Booking calendar integrated with Google Meet
- [ ] Qualification questions functional with auto-cancel logic
- [ ] Mobile responsive on all pages
- [ ] Load time under 3 seconds
- [ ] Screenshots captured
- [ ] All outputs saved to `RESULTS/06_funnel/`

→ Proceed to Step 7 (Automations)
