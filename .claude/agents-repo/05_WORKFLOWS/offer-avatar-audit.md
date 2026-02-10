# Offer-Avatar Audit Workflow

Systematically check the offer against ALL 9 product avatars to find gaps and maximize buyer coverage.

**Goal**: Turn every avatar into a potential buyer. Identify exactly what's missing for each.

---

## Input Required

- Product config from `01_PRODUCT/`
- Current offer (landing page, sales page, or offer description)
- OR: Ask agent to fetch from provided URL

---

## Process

### 1. Load All 9 Avatars

Read each avatar file from `02_AVATARS/standard/`:
1. `01-marcus-stuck-starter.md`
2. `02-sarah-side-hustle-parent.md`
3. `03-david-shopify-refugee.md`
4. `04-priya-platform-prisoner.md`
5. `05-tony-brick-to-click.md`
6. `06-jasmine-creator-commerce.md`
7. `07-mike-outgrown-diyer.md`
8. `08-rachel-burned-by-devs.md`
9. `09-carlos-marketplace-builder.md`

### 2. For Each Avatar, Analyze

| Check | Question |
|-------|----------|
| **Pain Points** | Does the offer address their specific pains? |
| **Emotional Triggers** | Does messaging hit their primary emotion? |
| **Objections** | Are their specific objections handled? |
| **Proof Needs** | Does the credibility match what they need to believe? |
| **Language** | Does copy use words that resonate with them? |
| **Value Perception** | Would they see this as worth the price? |
| **Urgency Fit** | Does the urgency/scarcity appeal to them? |
| **Conversion Likelihood** | Would they actually buy? Why/why not? |

### 3. Score Each Avatar

Rate fit from 0-10:
- **8-10**: Strong fit, likely to convert
- **5-7**: Partial fit, needs adjustments
- **0-4**: Weak fit, major gaps

### 4. Identify Gaps

For each avatar scoring <8, identify:
- THE primary gap (one thing)
- Specific fix to close that gap

### 5. Prioritize Fixes

Rank fixes by:
1. How many avatars it helps
2. Ease of implementation
3. Expected conversion lift

---

## Output Format

```
# Offer-Avatar Audit Results

## Avatar Fit Matrix

| Avatar | Score | Primary Gap | Fix |
|--------|-------|-------------|-----|
| Marcus (Stuck Starter) | /10 | | |
| Sarah (Side Hustle Parent) | /10 | | |
| David (Shopify Refugee) | /10 | | |
| Priya (Platform Prisoner) | /10 | | |
| Tony (Brick to Click) | /10 | | |
| Jasmine (Creator Commerce) | /10 | | |
| Mike (Outgrown DIYer) | /10 | | |
| Rachel (Burned by Devs) | /10 | | |
| Carlos (Marketplace Builder) | /10 | | |

**Average Fit Score**: /10

---

## Strongest Fits (8+)
[List avatars and why they're well-served]

## Weakest Fits (<5)
[List avatars and the core problem]

---

## Priority Fixes

### Fix 1: [Title]
**Helps**: [Which avatars]
**What to change**: [Specific action]
**Expected impact**: [What improves]

### Fix 2: [Title]
**Helps**: [Which avatars]
**What to change**: [Specific action]
**Expected impact**: [What improves]

### Fix 3: [Title]
**Helps**: [Which avatars]
**What to change**: [Specific action]
**Expected impact**: [What improves]

---

## Missing Elements

[Things the offer needs that aren't there at all]

## Underutilized Strengths

[Product strengths not being leveraged in the offer]
```

---

## Trigger Phrases

User says any of these → Run this workflow:
- "Audit my offer"
- "Check against avatars"
- "Find gaps in my offer"
- "Who am I missing?"
- "Product-market fit check"
- "Which avatars aren't served?"
