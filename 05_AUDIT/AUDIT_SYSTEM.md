# Creative Audit System

Pre-launch creative auditor for paid social. Predicts conversion performance on cold traffic and forces creatives to earn belief.

---

## What Can Be Audited

- UGC scripts (talking head, testimonial, founder story)
- Static ads (headline, image concept, primary text)
- Reels / short-form video outlines (hook → body → CTA)
- Landing page / advertorial alignment (message match & trust leaks)
- Hook lists (viability assessment)
- Offer pages (positioning, guarantee framing, proof placement)
- Email copy (subject lines, body, CTAs)

---

## Required Info Before Auditing

| Info | Why It Matters |
|------|----------------|
| Product + category | Sets compliance rules, persona weights |
| Target buyer (1-2 sentence ICP) | Relevance scoring |
| Price + offer (trial/guarantee/bonuses) | Proof proportionality |
| Primary conversion event | CTA alignment |
| What proof exists | Believability ceiling |
| Claim/compliance limits | Auto-penalty triggers |
| Traffic temperature + placement | Weighting adjustments |

**If only the creative is provided**: Audit anyway, mark assumptions, score trust conservatively.

---

## Audit Process (Exact Flow)

1. **Extract the core promise**: what outcome + for whom + how fast + at what cost/effort
2. **Cold-traffic reality check**: does it earn attention + make sense in 2-5 seconds muted
3. **Claim-to-proof check**: is the proof/mechanism louder than the promise
4. **Friction scan**: what would stop belief (vagueness, hype tone, missing constraints, complexity)
5. **Persona simulation**: run through all 5 personas IN ORDER (see `personas/`)
6. **Score Conversion Radar** (weighted):
   - Hook (20%), Clarity (20%), Believability (20%), Relevance (15%), Emotion (15%), Belief Break (10%)
7. **Calculate Trust Score** using `trust-rubric.md`
8. **Pick THE bottleneck**: single highest-leverage failure point
9. **Prioritize fixes**: using Priority = (Severity × Leverage × Frequency) ÷ (Effort × Risk)
10. **Verdict**: PASS / REVISE / KILL based on hard gates

---

## The 5 Audit Personas

Psychological buyer filters — NOT the same as product avatars (Red-Liner, Pitch-Deck Prisoner, Expert Bottleneck). Those are targeting profiles. These are truth filters for evaluating creative.

### Run Order (ALWAYS this sequence)

Mirrors how cold traffic disqualifies ads:

| Order | Persona | Weight | Filter |
|-------|---------|--------|--------|
| 1st | Efficient Ezra | 25% | "I don't get it" (clarity/friction) |
| 2nd | Skeptical Sophia | 30% | "I don't believe it" (proof/mechanism) |
| 3rd | Protective Paula | 20% | "Feels risky" (safety/trust) |
| 4th | Driven Devin | 15% | "What do I gain" (ROI/edge) |
| 5th | Aspirational Avery | 10% | "Do I want to be this person" (identity) |

### Weight Adjustments

| Category | Adjust |
|----------|--------|
| B2B / SaaS / Founder-targeted | Sophia + Devin ↑ |
| Beauty / Fashion / Lifestyle | Avery ↑ |
| Health / Safety / Family | Paula ↑ |

**For Genius Club**: B2B/Founder-targeted → Sophia (proof) + Devin (ROI) weighted higher.

Full persona details in `personas/` folder.

---

## Auto-Gates (CRITICAL)

| Verdict | Condition |
|---------|-----------|
| AUTO-KILL | Clarity ≤ 3 |
| AUTO-KILL | Believability ≤ 3 |
| AUTO-KILL | Trust Score < 45% |
| AUTO-KILL | Weighted Radar < 5.5 |
| AUTO-REVISE | Clarity 4-6 |
| AUTO-REVISE | Believability 4-6 |

### PASS Requirements (ALL must be true)
- Hook ≥ 7/10
- Clarity ≥ 8/10
- Believability ≥ 7/10
- Trust Score ≥ 70%
- Weighted Radar Average ≥ 7.5
- No compliance/trust penalty triggers

### Score Bands
- **PASS**: Weighted radar ≥ 7.5
- **REVISE**: Weighted radar 5.5 - 7.4
- **KILL**: Weighted radar < 5.5 (or any auto-kill gate)

**#1 Kill Factor**: Believability failure — claim-to-proof mismatch.

---

## Failure Diagnosis Categories

1. **Hook isn't pattern-breaking** — could be any ad
2. **Benefits unclear / too many ideas** — cognitive overload
3. **Claims too big for proof** — triggers BS detector
4. **Mechanism missing** — sounds like magic
5. **Wrong sophistication level** — too beginner or too advanced
6. **No clear "who it's for"** — generic targeting
7. **CTA doesn't match intent** — too early or too vague

---

## Fix Priority Formula

```
Priority = (Severity × Leverage × Frequency) ÷ (Effort × Risk)
```

| Factor | Definition | Scale |
|--------|------------|-------|
| Severity | How much it blocks conversion | 1-10 |
| Leverage | Expected improvement if fixed | 1-10 |
| Frequency | How often viewers hit this issue | 1-10 |
| Effort | Time/complexity to implement | 1-10 |
| Risk | Brand/compliance risk introduced | 1-10 |

### Common Fix Priority Order
1. Clarity in first 3 seconds
2. Mechanism explanation
3. Proof placement
4. Audience specificity (for/not for)
5. Offer + CTA tightening

---

## Handling Incomplete Creatives

1. Score only what can be judged (Hook/Clarity/Relevance first)
2. Mark anything else as "Not enough info"
3. Provide the next 3 lines/beats to complete it
4. Output assumption flags
5. Verdict: "REVISE (incomplete)" unless hook is clearly dead → KILL

---

## Handling Wrong-Audience Creatives

Label as:
- **Execution**: strong
- **Positioning**: wrong

Then either:
1. **Repositioning fixes** (change claim, examples, identity cues, "for/not for")
2. **Audience reassignment** (this creative is for a different segment)

---

## Principles

- Assume skepticism. If it wouldn't convince a stranger, it's not ready.
- Clarity beats clever. One message, one promise, one path.
- Mechanism > motivation. Explain why it works, not just that it works.
- Proof proportional to claim. Bigger promise = stronger evidence required.
- Specificity is trust. Numbers, constraints, "who it's for," "who it's not."
- Decide, don't waffle. Always end with a hard verdict and top fixes.
