# STEP 5: CREATIVE AUDIT

**Nothing goes live without passing. No exceptions.**

**Depends on**: Step 4 (Copy) complete → `RESULTS/thegenius.club/04_copy/` exists
**Produces**: `RESULTS/thegenius.club/05_audit/`
**Agent**: `creative-auditor`

---

## What This Step Does

Run EVERY piece of copy from Step 4 through the 5-persona audit system. Score it. Verdict it. Fix it. Re-audit until it PASSES.

---

## Input

From `RESULTS/thegenius.club/04_copy/`:
- All copy assets (landing page, booking, thank you, ads, outbound emails)

From `RESULTS/thegenius.club/03_offer/`:
- Offer package (for proof/claim matching)

From `RESULTS/thegenius.club/02_avatars/`:
- Avatar profiles (for relevance checking)

---

## The 5 Audit Personas (Run in This Order)

| Order | Persona | Weight | Gate | Details |
|-------|---------|--------|------|---------|
| 1st | Efficient Ezra | 25% | "I don't get it" | `personas/efficient-ezra.md` |
| 2nd | Skeptical Sophia | 30% | "I don't believe it" | `personas/skeptical-sophia.md` |
| 3rd | Protective Paula | 20% | "Feels risky" | `personas/protective-paula.md` |
| 4th | Driven Devin | 15% | "What do I gain" | `personas/driven-devin.md` |
| 5th | Aspirational Avery | 10% | "Do I want to be this" | `personas/aspirational-avery.md` |

**Genius Club adjustment**: Sophia + Devin weighted HIGHER (B2B founder audience).

**These are NOT the 3 product avatars.** These are psychological truth filters.

---

## Audit Process (Exact — for Each Creative)

1. Extract core promise (outcome + for whom + how fast + cost)
2. Cold-traffic reality check (2-5 sec muted — would you stop scrolling?)
3. Claim-to-proof check (proof louder than promise?)
4. Friction scan (vagueness, hype, missing constraints)
5. Run all 5 personas (in order above)
6. Score **Conversion Radar**:

| Dimension | Weight |
|-----------|--------|
| Hook | 20% |
| Clarity | 20% |
| Believability | 20% |
| Relevance | 15% |
| Emotion | 15% |
| Belief Break | 10% |

7. Calculate **Trust Score** (`trust-rubric.md`)
8. Pick THE bottleneck (single highest-leverage failure)
9. Rank fixes: Priority = (Severity × Leverage × Frequency) ÷ (Effort × Risk)
10. **Verdict**

---

## Verdicts

| Verdict | Condition | Action |
|---------|-----------|--------|
| **PASS** | Radar ≥ 7.5, Hook ≥ 7, Clarity ≥ 8, Believability ≥ 7, Trust ≥ 70% | → Move to Step 6 |
| **REVISE** | Radar 5.5-7.4 or Clarity/Believability 4-6 | Fix top issues → back to Step 4 → re-audit |
| **KILL** | Radar < 5.5 or Clarity ≤ 3 or Believability ≤ 3 or Trust < 45% | Rewrite from scratch → back to Step 4 → re-audit |

**#1 Kill Factor**: Believability failure — claim-to-proof mismatch.

---

## What to Audit (Checklist)

| Creative | File | Verdict |
|----------|------|---------|
| Landing page headline + copy | `RESULTS/thegenius.club/04_copy/landing-page-copy.md` | |
| Landing page video script | (within landing page file) | |
| Booking page copy | `RESULTS/thegenius.club/04_copy/booking-page-copy.md` | |
| Thank you page copy | `RESULTS/thegenius.club/04_copy/thankyou-page-copy.md` | |
| Ad copy: Red-Liner | `RESULTS/thegenius.club/04_copy/ad-copy-red-liner.md` | |
| Ad copy: Pitch-Deck Prisoner | `RESULTS/thegenius.club/04_copy/ad-copy-pitch-deck-prisoner.md` | |
| Ad copy: Expert Bottleneck | `RESULTS/thegenius.club/04_copy/ad-copy-expert-bottleneck.md` | |
| Outbound email | `RESULTS/thegenius.club/04_copy/outbound-email-copy.md` | |

---

## Output Format

Use `output-standards.md` for every audit:
- Executive Summary (verdict + bottleneck + trust + radar + top 3 fixes)
- Conversion Radar (6 dimensions, weighted scores)
- Persona Panel (all 5, in order, with voice lines)
- Fix Plan (ranked by lift)

---

## Output

Save to `RESULTS/thegenius.club/05_audit/`:
- `audit-landing-page.md`
- `audit-booking-page.md`
- `audit-thankyou-page.md`
- `audit-ads-red-liner.md`
- `audit-ads-prisoner.md`
- `audit-ads-bottleneck.md`
- `audit-outbound-email.md`
- `audit-summary.md` — master verdict table (which passed, which need work)

---

## Done When

- [ ] Every creative audited through all 5 personas
- [ ] Every creative has a verdict (PASS/REVISE/KILL)
- [ ] All REVISE items fixed and re-audited to PASS
- [ ] All KILL items rewritten and re-audited to PASS
- [ ] Master summary shows ALL PASS
- [ ] All outputs saved to `RESULTS/thegenius.club/05_audit/`

→ Proceed to Step 6 (Funnel Build)
