# Trust Score Rubric

Trust Score is a weighted calculation (0-100%) based on observable trust signals minus penalties.

---

## Trust Score Formula

### Step 1: Calculate Sub-Scores (0-10 each)

| Code | Sub-Score | What It Measures |
|------|-----------|------------------|
| C2P | Claim-to-Proof Fit | Is proof proportional to claim? |
| MECH | Mechanism Clarity | Does it explain WHY it works? |
| SPEC | Specificity | Numbers, constraints, who it's for/not for |
| RISK | Risk Reversal / Safety | Guarantee, transparency, effort/time realism |
| LEGIT | Legitimacy Cues | Tone, professionalism, consistency, compliance-safe phrasing |
| FRIC | Friction Honesty | Acknowledges tradeoffs, avoids "too perfect" |

### Step 2: Apply Weights

```
Base Trust% = 10 × (0.30×C2P + 0.20×MECH + 0.15×SPEC + 0.15×RISK + 0.10×LEGIT + 0.10×FRIC)
```

| Sub-Score | Weight |
|-----------|--------|
| C2P (Claim-to-Proof) | 30% |
| MECH (Mechanism) | 20% |
| SPEC (Specificity) | 15% |
| RISK (Risk Reversal) | 15% |
| LEGIT (Legitimacy) | 10% |
| FRIC (Friction Honesty) | 10% |

### Step 3: Apply Penalties

Subtract from Base Trust after calculation:

| Penalty | Range | Trigger |
|---------|-------|---------|
| Hype penalty | -5 to -25 | Language exaggerated relative to proof ("miracle," "instant," "guaranteed results") |
| Vagueness penalty | -5 to -20 | Benefits are generic ("better," "amazing," "transform" with no specifics) |
| Compliance-risk penalty | -10 to -40 | Implies disallowed/unsafe claims (category-dependent) |
| Mismatch penalty | -5 to -30 | Headline/body/CTA don't align (message inconsistency) |

### Step 4: Clamp Result

```
Final Trust% = clamp(Base Trust% - Penalties, 0, 100)
```

---

## Trust Sub-Score Anchors

### C2P: Claim-to-Proof Fit (30% weight)

| Score | Criteria |
|-------|----------|
| 0 | Big claims, zero proof |
| 5 | Claims made, some proof but not proportional |
| 10 | Every claim backed by evidence of equal weight |

### MECH: Mechanism Clarity (20% weight)

| Score | Criteria |
|-------|----------|
| 0 | No explanation of how/why |
| 5 | Light mention of mechanism |
| 10 | Clear "here's why this works" that makes logical sense |

### SPEC: Specificity (15% weight)

| Score | Criteria |
|-------|----------|
| 0 | Completely generic |
| 5 | Some numbers or constraints |
| 10 | Precise numbers, timeframes, who it's for/not for |

### RISK: Risk Reversal / Safety (15% weight)

| Score | Criteria |
|-------|----------|
| 0 | No guarantee, high perceived risk |
| 5 | Basic guarantee mentioned |
| 10 | Strong guarantee + realistic expectations + transparent effort |

### LEGIT: Legitimacy Cues (10% weight)

| Score | Criteria |
|-------|----------|
| 0 | Scammy tone, poor production, inconsistent |
| 5 | Professional but unremarkable |
| 10 | High-quality, consistent, compliance-safe, trustworthy feel |

### FRIC: Friction Honesty (10% weight)

| Score | Criteria |
|-------|----------|
| 0 | "Too good to be true" / no downsides mentioned |
| 5 | Mild acknowledgment of effort |
| 10 | Honest about tradeoffs, effort required, who it's NOT for |

---

## Trust Score Thresholds

| Score | Meaning | Verdict Impact |
|-------|---------|----------------|
| ≥ 70% | Grounded, specific, proof-backed | Eligible for PASS |
| 45-69% | Plausible but needs strengthening | REVISE territory |
| < 45% | Will trigger skepticism at scale | AUTO-KILL |

**Critical**: Trust Score < 45% triggers AUTO-KILL regardless of other scores.

---

## Quick Trust Audit Checklist

| Check | Impact |
|-------|--------|
| Is there a specific number or timeframe? | +trust |
| Is the mechanism explained? | +trust |
| Is there proof proportional to the claim? | +trust |
| Are limitations acknowledged? | +trust |
| Does anything feel "too good to be true"? | -trust |
| Are there contradictions? | -trust |
| Is important info missing (price, effort, risk)? | -trust |

---

## Trust Calculation Example

**Creative claims**: "Get 10 clients in 30 days"
**Proof shown**: 2 testimonials (no specifics), no mechanism

| Sub-Score | Rating | Weighted |
|-----------|--------|----------|
| C2P | 4 | 4 × 0.30 = 1.2 |
| MECH | 2 | 2 × 0.20 = 0.4 |
| SPEC | 6 | 6 × 0.15 = 0.9 |
| RISK | 3 | 3 × 0.15 = 0.45 |
| LEGIT | 5 | 5 × 0.10 = 0.5 |
| FRIC | 2 | 2 × 0.10 = 0.2 |

Base Trust = 10 × (1.2 + 0.4 + 0.9 + 0.45 + 0.5 + 0.2) = **36.5%**

Penalties: Hype (-10 for "guaranteed" language implied)

Final Trust = 36.5 - 10 = **26.5%** → AUTO-KILL
