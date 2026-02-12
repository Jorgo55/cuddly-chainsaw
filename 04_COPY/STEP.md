# STEP 4: COPY CREATION

**Write every word using the offer, avatars, and ben heath system.**

**Depends on**: Step 3 (Offer) complete → `RESULTS/03_offer/` exists, score ≥35/54
**Produces**: `RESULTS/04_copy/`
**Agent**: `copy-engine`

---

## What This Step Does

Write all copy for the funnel: landing page, booking page, thank you page, ads, outbound emails. Every piece runs through the Value Equation and uses the avatar data.

---

## Input

From `RESULTS/03_offer/`:
- Completed offer package (transformation statement, mechanism, bonuses, guarantee, CTAs)
- Offer score + avatar fit matrix

From `RESULTS/02_avatars/`:
- All 3 avatar profiles (pain points, voice lines, ad angles, objections)

From `RESULTS/01_analysis/`:
- Real audience language (vocabulary bank)
- Competitor messaging gaps

From `00_CONTEXT/07_messaging_dna.md`:
- Tone, angles, messaging rules

---

## The Copy System

**Value Equation** (apply to everything):
```
Value = (Dream Outcome × Perceived Likelihood) / (Time Delay × Effort & Sacrifice)
```

**Message Flow**:
```
Hook → Jealousy/Contrast → Problem Dig → Solution (mechanism) → Easy/Quick/Safe → Objection Handling → Social Proof → CTA
```

**Hook Frameworks** (from `templates/`):
- Outcome + Time: "Get <outcome> in <time> without <pain>"
- Before/After: "From <bad state> to <good state>"
- Specific ICP: "For <ICP>: <outcome> with <mechanism>"
- Risk Removal: "Avoid <risk> when doing <job>"
- Ben Heath: "Stop wasting X on…", "The hidden cost of…"

---

## Process (Write in This Order)

### 4a. Landing Page Copy
- Headline: 3-5 options ranked (must pass 3-second test)
- Sub-headline: hard filter ($250K+ visible)
- Video script: short — NOT full VSL, just enough to explain the funding offer
- Lead capture CTA
- Social proof section (if available)

### 4b. Booking Page Copy
- Qualification questions (filter tire-kickers, don't be hostile)
- Expectation-setting copy
- Booking CTA

### 4c. Thank You Page Copy
- Booking confirmation
- Bonus video script (what they get on the call, why it matters)
- Show-up motivation copy
- "What happens next" section

### 4d. Ad Copy (per avatar)
For EACH of the 3 avatars:
- 3-5 hook variations
- Primary text
- Headline
- Description
- Use ad angles from avatar profiles

### 4e. Outbound Email Copy (for 50K list)
- Subject line variations (3-5)
- Email body (reference outbound hook from `00_CONTEXT/01_icp.md`)
- Per-avatar variations if needed

---

## Copy Hard Rules

1. **3-second test**: reader knows EXACTLY what they're getting
2. **$250K+ filter**: visible in headline or sub-headline
3. **Sell FUNDING, not the club** — club revealed on call ONLY
4. **One promise, one ICP, one mechanism** per piece
5. **Concrete nouns + numbers** over vague adjectives
6. **Clarity > cleverness** — always
7. **No hype, no fluff** — confident and direct
8. **Claim safety**: no proof = soften language
9. Use real audience language from Step 1 research

---

## Output

Save to `RESULTS/04_copy/`:
- `landing-page-copy.md` — headlines, sub-headlines, body, CTA, video script
- `booking-page-copy.md` — questions, copy, CTA
- `thankyou-page-copy.md` — confirmation, bonus video script, motivation
- `ad-copy-red-liner.md` — hooks, primary text, headlines per avatar
- `ad-copy-pitch-deck-prisoner.md`
- `ad-copy-expert-bottleneck.md`
- `outbound-email-copy.md` — subject lines, body, variations

---

## Done When

- [ ] All funnel page copy complete (landing, booking, thank you)
- [ ] Ad copy written for all 3 avatars (3-5 hooks each)
- [ ] Outbound email copy with subject line variations
- [ ] Every piece uses avatar language + offer components
- [ ] All outputs saved to `RESULTS/04_copy/`

→ Proceed to Step 5 (Audit)
