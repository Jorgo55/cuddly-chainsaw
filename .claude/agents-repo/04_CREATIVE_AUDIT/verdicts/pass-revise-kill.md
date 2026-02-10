# Verdict Criteria

Final verdict: PASS, REVISE, or KILL

---

## Auto-Gates (Hard Rules)

These override everything else.

### AUTO-KILL Triggers

If ANY of these are true → immediate KILL:

| Condition | Why |
|-----------|-----|
| Clarity ≤ 3 | Confusing / not understood in 1 pass |
| Believability ≤ 3 | Sounds fake / claim >> proof |
| Trust Score < 45% | Will trigger skepticism at scale |

### AUTO-REVISE Triggers

If ANY of these are true → REVISE (cannot PASS):

| Condition | Why |
|-----------|-----|
| Clarity 4-6 | Fixable but risky to scale |
| Believability 4-6 | Needs proof/mechanism work |

---

## PASS (launch-ready)

Creative is ready to test with ad spend.

**ALL requirements must be met**:

| Requirement | Threshold |
|-------------|-----------|
| Hook | ≥ 7/10 |
| Clarity | ≥ 8/10 |
| Believability | ≥ 7/10 |
| Trust Score | ≥ 70% |
| Weighted Radar Average | ≥ 7.5 |
| No major compliance/trust penalty triggers | True |

---

## REVISE (testable concept, execution weak)

Core idea is strong but execution needs work before launch.

**Triggers**:
- Hook is generic (but message is right)
- Proof missing or weak
- Messaging is muddy
- Persona fit is uneven
- Clarity or Believability is 4-6
- Trust Score 45-69%
- Weighted Radar Average 5.5-7.4

**Action**: Make 1-3 targeted fixes, then re-audit.

---

## KILL (not worth spend)

Creative will waste money. Don't launch.

**Triggers**:
- Any AUTO-KILL condition met
- Confusing + generic + unproven
- Claim > proof by wide margin
- No clear audience, no clear benefit, no "reason to believe"
- Feels like "every other ad" in the feed
- Trust Score < 45%
- Weighted Radar Average < 5.5

**Action**: Start over with different angle or offer.

---

## The Single Most Important Factor: KILL vs REVISE

**Believability failure on cold traffic — specifically Claim-to-Proof mismatch.**

If the ad makes a meaningful promise but:
- Doesn't show mechanism, or
- Doesn't show proof early, or
- Feels hypey/vague

→ It typically becomes **KILL** (because scaling amplifies skepticism)

If the promise is strong but needs proof/mechanism/clarity tightening → **REVISE**

---

## Verdict Decision Tree

```
START
  │
  ├── Clarity ≤ 3? ──────────────────────────────→ KILL
  │
  ├── Believability ≤ 3? ────────────────────────→ KILL
  │
  ├── Trust Score < 45%? ────────────────────────→ KILL
  │
  ├── Weighted Radar < 5.5? ─────────────────────→ KILL
  │
  ├── Clarity OR Believability is 4-6? ──────────→ REVISE
  │
  ├── Trust Score < 70%? ────────────────────────→ REVISE
  │
  ├── Weighted Radar < 7.5? ─────────────────────→ REVISE
  │
  ├── Hook < 7? ─────────────────────────────────→ REVISE
  │
  ├── Clarity < 8? ──────────────────────────────→ REVISE
  │
  ├── Believability < 7? ────────────────────────→ REVISE
  │
  └── All gates passed? ─────────────────────────→ PASS
```

---

## Verdict Template

```
## Verdict: [PASS / REVISE / KILL]

**Reasoning**: [1-2 sentences explaining the decision]

**Primary Bottleneck**: [Single highest-leverage failure point]

**Key Scores**:
- Hook: X/10
- Clarity: X/10
- Believability: X/10
- Weighted Radar: X.X/10
- Trust Score: XX%

**Auto-Gate Status**: [Which gates passed/failed]

**If REVISE/KILL - Top Fixes**:
1. [Fix 1] → [expected lift]
2. [Fix 2] → [expected lift]
3. [Fix 3] → [expected lift]
```

---

## Special Verdicts

### REVISE (incomplete)

For partial creatives (hook only, no full script):
- Score what can be judged
- Mark missing elements
- Provide next beats to complete
- Cannot be PASS until complete

### KILL for this target

For technically good creative, wrong audience:
- Execution: strong
- Positioning: wrong
- May work for different segment
