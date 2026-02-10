# OfferOps Agent

Codex-compatible agent for building high-converting offers and auditing creatives.

## What This Agent Does

1. **Builds Offers** - Using proven frameworks (Value Equation, M-A-G-I-C naming, bonuses, guarantees, urgency)
2. **Audits Creatives** - Predicts conversion performance before ad spend
3. **Forces Quality** - Adversarial review that makes creatives earn belief

## Quick Start

1. Connect this repo to ChatGPT Codex
2. Codex reads `AGENTS.md` for behavioral instructions
3. Say "audit this creative" or "help me build an offer"

## Modes

| Mode | Trigger | What Happens |
|------|---------|--------------|
| `audit` | Submit creative | 5-persona scorecard + verdict + fixes |
| `offer-build` | "Help me build..." | Walk through offer templates |
| `full-pipeline` | "New product" or unclear | Product → Avatar → Offer → Audit |

## Structure

```
├── AGENTS.md                 # Agent instructions (the brain)
├── 00_CONSTITUTION/          # Rules, modes, output formats
├── 01_PRODUCT/               # Product configs (plug-and-play)
├── 02_AVATARS/               # 9 target customer profiles
├── 03_OFFER_FRAMEWORK/       # Offer building templates + rubrics
├── 04_CREATIVE_AUDIT/        # 5 audit personas + scoring system
├── 05_WORKFLOWS/             # Step-by-step process guides
├── 06_CONFIG/                # Mode switches
└── 90_GOVERNANCE/            # Principles + changelog
```

## Two Persona Systems

| Type | Location | Purpose |
|------|----------|---------|
| **5 Audit Personas** | `04_CREATIVE_AUDIT/personas/` | Evaluate creatives (Paula, Sophia, Devin, Ezra, Avery) |
| **9 Product Avatars** | `02_AVATARS/standard/` | Build offers (Marcus, Sarah, David, etc.) |

## Current Product

**Store + App Launch Kit** - Ready-made ecommerce website + apps for non-technical founders.

Config: `01_PRODUCT/store-app-launch-kit.md`

## Methodology Sources

- **Offer Framework**: Jack Rogers' Offer Creation SOP
- **Creative Audit**: Ben Heath / Heath Media GPT
- **Value Equation**: (Dream Outcome × PLA) / (Time Delay × E&S)
