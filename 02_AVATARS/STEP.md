# STEP 2: AVATAR CONSTRUCTION

**Build the customer before you build anything for them.**

**Depends on**: Step 1 (Analysis) complete → `RESULTS/thegenius.club/01_analysis/` exists
**Produces**: `RESULTS/thegenius.club/02_avatars/`
**Agent**: `icp-filter`
**Template**: `templates/AVATAR_TEMPLATE.md`

---

## What This Step Does

Build full 14-section avatar profiles for each target customer. Uses analysis data from Step 1 (real language, real pain points, real objections) — not guesses.

---

## Input

From `RESULTS/thegenius.club/01_analysis/`:
- Audience language (exact quotes from real communities)
- Competitor messaging gaps (what's NOT being addressed)
- Pain points ranked by frequency
- Failed solutions ranked by frequency
- Objections ranked by frequency

From `00_CONTEXT/01_icp.md`:
- The 3 avatar sketches (Red-Liner, Pitch-Deck Prisoner, Expert Bottleneck)
- Firmographics, behavioral signals, scraping targets

---

## Process

For EACH avatar (Red-Liner, Pitch-Deck Prisoner, Expert Bottleneck):

1. Open `templates/AVATAR_TEMPLATE.md`
2. Fill ALL 14 sections — no blanks
3. Use real language from Step 1 audience research for voice lines, pain points, objections
4. Map competitor data to "false solutions" and "expensive alternatives"
5. Write 3 relatable stories per avatar using real community examples
6. Define 5 ad angles per avatar

### The 14 Sections

| # | Section | Key Question |
|---|---------|-------------|
| 1 | Demographics | Who ARE they? (age, income, title, location) |
| 2 | Psychographics | What do they consume? (media, communities, influences) |
| 3 | Competitor Exposure | Who've they already tried? What happened? |
| 4 | Emotion Analysis | What emotions drive them? Can we trigger these? |
| 5 | Pain Points | What hurts? (money, time, ops, psychology) |
| 6 | False Solutions | What have they been sold that didn't work? |
| 7 | Goals | What do they really want? (primary, secondary, hidden) |
| 8 | Values | What do they care about beyond the transaction? |
| 9 | Objections | What stops them from buying? Root fear behind each? |
| 10 | Expensive Alternatives | What else did they consider? Why didn't they go with it? |
| 11 | Relatable Stories | 3 stories they'd see themselves in |
| 12 | Voice Line | What they'd literally say about their situation |
| 13 | Product-Pain Match | Their pain → our specific solution |
| 14 | Ad Angles | 5 hooks/angles that resonate with THIS avatar |

---

## Output

Save to `RESULTS/thegenius.club/02_avatars/`:
- `red-liner.md` — full 14-section avatar
- `pitch-deck-prisoner.md` — full 14-section avatar
- `expert-bottleneck.md` — full 14-section avatar
- `avatar-summary.md` — quick-reference matrix of all 3

---

## Done When

- [ ] All 3 avatars fully built out (zero blank sections)
- [ ] Voice lines use real language from audience research
- [ ] Pain points and objections cross-referenced with Step 1 data
- [ ] 3 relatable stories per avatar written
- [ ] 5 ad angles per avatar defined
- [ ] All outputs saved to `RESULTS/thegenius.club/02_avatars/`

→ Proceed to Step 3 (Offer)
