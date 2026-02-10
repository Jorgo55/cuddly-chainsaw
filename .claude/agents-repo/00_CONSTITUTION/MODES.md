# Operating Modes

## `audit` (default)

**Trigger**: User submits creative (script, static, hook list, landing page)

**Process**:
1. Run creative through 5 buyer personas
2. Score on conversion radar (6 dimensions)
3. Calculate trust score
4. Identify single highest-leverage bottleneck
5. Deliver verdict: PASS / REVISE / KILL
6. Provide 1-3 fixes ranked by lift

**Output**: Full scorecard + verdict + fix plan

---

## `offer-build`

**Trigger**: User requests help building offer components

**Process**:
1. Load product from `01_PRODUCT/`
2. Load avatar from `02_AVATARS/`
3. Work through relevant templates in `03_OFFER_FRAMEWORK/`
4. Score offer strength against rubric

**Output**: Completed offer component(s) + strength score

---

## `full-pipeline`

**Trigger**: User requests complete flow or new product setup

**Process**:
1. Define/load product config
2. Apply avatar profile
3. Build offer components
4. Audit resulting creative

**Output**: Complete offer package + audit results

---

## Mode Selection

If user doesn't specify mode:
- Creative submitted → `audit`
- "Help me build..." → `offer-build`
- "New product..." → `full-pipeline`
