# Changelog

## [0.7.0] - Audit Mechanics Refined

### Added
- Exact Trust Score formula with 6 weighted sub-scores + penalties
- Conversion Radar dimension weights (Hook/Clarity/Believability 20% each, Relevance/Emotion 15%, Belief Break 10%)
- Auto-gate decision tree for PASS/REVISE/KILL
- Fix Priority formula: (Severity × Leverage × Frequency) ÷ (Effort × Risk)
- Persona evaluation order (Ezra → Sophia → Paula → Devin → Avery)
- Persona weights (Sophia 30%, Ezra 25%, Paula 20%, Devin 15%, Avery 10%)
- Required info checklist before auditing
- Incomplete creative handling (REVISE incomplete)
- Wrong-audience creative handling
- Trust calculation example in trust-rubric.md
- Verdict decision tree flowchart

### Changed
- **AGENTS.md**: Added exact scoring mechanics, auto-gates, persona order/weights
- **AUDIT_SYSTEM.md**: Complete rewrite with full process, fix formula, edge cases
- **scoring-anchors.md**: Added dimension weights, auto-kill thresholds
- **trust-rubric.md**: Added exact formula with sub-scores and penalties
- **pass-revise-kill.md**: Added auto-gates, decision tree, detailed thresholds
- **OUTPUT_STANDARDS.md**: Updated with exact output structure (A-E sections)
- All 5 persona files: Added weight and evaluation order info

---

## [0.6.0] - All-Avatar Audit

### Added
- `05_WORKFLOWS/offer-avatar-audit.md` - systematic check against ALL 9 avatars
- Avatar Fit Matrix output format in AGENTS.md

### Changed
- **AGENTS.md**: Default behavior now checks ALL 9 avatars when auditing offers (not 1-2)
- Clear trigger: "audit offer" → full 9-avatar systematic analysis
- Output includes fit matrix, gaps per avatar, priority fixes

---

## [0.1.0] - Initial Structure

### Added
- Directory structure
- AGENTS.md main entry point
- 00_CONSTITUTION (SYSTEM, MODES, OUTPUT_STANDARDS)
- 01_PRODUCT template
- 02_AVATARS template (content coming)
- 03_OFFER_FRAMEWORK templates + rubric
- 04_CREATIVE_AUDIT (full Ben Heath system)
  - 5 buyer personas
  - Conversion radar scoring
  - Trust rubric
  - Verdict criteria
- 05_WORKFLOWS (full-pipeline, offer-only, audit-only)
- 90_GOVERNANCE (principles, changelog)

## [0.6.0] - All-Avatar Audit

### Added
- `05_WORKFLOWS/offer-avatar-audit.md` - systematic check against ALL 9 avatars
- Avatar Fit Matrix output format in AGENTS.md

### Changed
- **AGENTS.md**: Default behavior now checks ALL 9 avatars when auditing offers (not 1-2)
- Clear trigger: "audit offer" → full 9-avatar systematic analysis
- Output includes fit matrix, gaps per avatar, priority fixes

---

## [0.5.0] - Agent Refinement

### Added
- Complete rewrite of `AGENTS.md` - proper agent instructions for Codex
- Clear distinction between 5 Audit Personas vs 9 Product Avatars

### Fixed
- Score thresholds in workflows (was /18, now /54)
- Workflow templates now reference all new offer components
- Persona/avatar confusion clarified across all relevant files

### Updated
- `README.md` - reflects current state
- `05_WORKFLOWS/offer-only.md` - includes all templates
- `05_WORKFLOWS/full-pipeline.md` - correct thresholds
- `04_CREATIVE_AUDIT/AUDIT_SYSTEM.md` - persona clarification
- `02_AVATARS/AVATAR_INDEX.md` - avatar vs persona distinction

---

## [0.4.0] - Offer Framework Complete

### Added
Full offer methodology integrated into `03_OFFER_FRAMEWORK/`:
- `OFFER_SYSTEM.md` - Complete system with Value Equation + Message Flow
- `templates/value-equation.md` - 4-variable value optimization
- `templates/offer-naming-magic.md` - M-A-G-I-C naming formula
- `templates/pricing-strategy.md` - Strategic pricing SOP
- `templates/bonuses-playbook.md` - 8 rules for bonuses
- `templates/urgency-scarcity.md` - Urgency/scarcity types + swipe
- `templates/guarantee-framework.md` - Power guarantee types
- `templates/message-flow.md` - 8-step persuasion sequence
- `templates/cta-swipefile.md` - Copy-paste CTAs by type
- `templates/what-offer-is-not.md` - Anti-patterns (expected basics)
- `rubrics/offer-score.md` - Comprehensive 54-point rubric

### Updated
- Existing templates enriched with new methodology

---

## [0.3.0] - Avatars Complete

### Added
- 9 detailed buyer avatars in `02_AVATARS/standard/`:
  - 01-marcus-stuck-starter.md
  - 02-sarah-side-hustle-parent.md
  - 03-david-shopify-refugee.md
  - 04-priya-platform-prisoner.md
  - 05-tony-brick-to-click.md
  - 06-jasmine-creator-commerce.md
  - 07-mike-outgrown-diyer.md
  - 08-rachel-burned-by-devs.md
  - 09-carlos-marketplace-builder.md
- `02_AVATARS/AVATAR_INDEX.md` - Quick reference and segmentation
- Expanded `02_AVATARS/AVATAR_TEMPLATE.md` with full 14-section structure

### Pending
- Full offer methodology content (awaiting 10 detailed files)
- Example outputs
- Config presets

---

## [0.2.0] - Product Data

### Added
- `01_PRODUCT/store-app-launch-kit.md` - Full product config for Store + App Launch Kit
- Updated AGENTS.md to reference active product
