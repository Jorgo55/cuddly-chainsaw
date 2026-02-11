# STEP 3: OFFER ARCHITECTURE

**Structure what you sell before you write a word of copy.**

**Depends on**: Step 2 (Avatars) complete → `RESULTS/02_avatars/` exists
**Produces**: `RESULTS/03_offer/`
**Agent**: `offer-builder`

---

## What This Step Does

Build the complete offer package using the avatar data. Every component follows a template. Score it. Audit it against all 3 avatars. Don't proceed until it scores ≥35/54.

---

## Input

From `RESULTS/02_avatars/`:
- All 3 completed avatar profiles
- Pain points, objections, false solutions, goals per avatar

From `RESULTS/01_analysis/`:
- Competitor pricing and offer structures
- Positioning canvas (our unique angle)

From `00_CONTEXT/`:
- Business overview (pricing: $5K membership, $10K accelerator)
- Sales mechanism (bait-and-switch flow)

---

## Process (Templates in Order)

| Order | Component | Template | Output |
|-------|-----------|----------|--------|
| 3a | Value Equation | `templates/01_offer_value_equation_and_message_flow.md` | All 4 variables optimized |
| 3b | Transformation Statement | `templates/09_transformation_statement.md` | Core promise in 1 sentence |
| 3c | Unique Mechanism | `templates/10_unique_mechanism.md` | Named method + why it works |
| 3d | Offer Name | `templates/05_offer_naming_magic.md` | M-A-G-I-C applied (3 of 5 min) |
| 3e | Pricing | `templates/02_strategic_pricing.md` | Anchored + stacked strategy |
| 3f | Bonuses | `templates/06_bonuses_playbook.md` | Named bonuses solving objections |
| 3g | Guarantee | `templates/07_power_guarantee.md` | Risk reversal with clear terms |
| 3h | Urgency/Scarcity | `templates/04_urgency_and_scarcity.md` | Real action triggers |
| 3i | Credibility | `templates/11_credibility_checklist.md` | Proof assets + claim matching |
| 3j | CTAs | `templates/ben-heath-cta-swipefile.md` | Action-oriented, desire-aligned |

### Then Score

Use `templates/12_offer_score_rubric.md` (54-point rubric):

| Score | Verdict | Action |
|-------|---------|--------|
| 45-54 | Strong | → Proceed to Step 4 |
| 35-44 | Good | Fix minor gaps → proceed |
| 25-34 | Needs Work | Fix gaps → re-score |
| <25 | Weak | Rebuild → re-score |

### Then Audit Against Avatars

For EACH of the 3 avatars, check:
1. Does the offer address their specific pain points?
2. Does the messaging hit their emotional triggers?
3. Are their objections handled?
4. Does the proof match what THEY need?
5. Would they actually buy? Why/why not?

Output: avatar fit matrix (score /10 per avatar + gaps + fixes)

---

## Genius Club Hard Rules

- Sell FUNDING on the page — the club is revealed on the call ONLY
- "Great team" and "years of experience" are NOT differentiators
- The irresistible part = unique mechanism + urgency + clear reason to act NOW
- Bonuses presented AFTER price (unexpected = higher value)
- Tools > training for perceived immediacy

---

## Output

Save to `RESULTS/03_offer/`:
- `offer-package.md` — all components filled
- `offer-score.md` — rubric score + gap analysis
- `avatar-fit-matrix.md` — fit score per avatar + fixes
- `transformation-statement.md` — the one-liner
- `unique-mechanism.md` — the named method

---

## Done When

- [ ] All 10 offer components completed
- [ ] Offer scored ≥35/54
- [ ] Avatar fit audit done for all 3 avatars
- [ ] Weak fits (<5) addressed with specific fixes
- [ ] All outputs saved to `RESULTS/03_offer/`

→ Proceed to Step 4 (Copy)
