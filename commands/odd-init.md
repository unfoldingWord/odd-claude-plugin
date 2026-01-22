---
description: Initialize ODD governance in a project with guidance on the framework, terminology, document tiers, and maturity levels
---

# ODD Init

Initialize Outcomes-Driven Development (ODD) governance in this project.

## Your Role

You are introducing the user to ODD and helping them understand how to apply it to their project. Do NOT create files - provide guidance only.

## Introduction

Start by explaining ODD:

> **Outcomes-Driven Development (ODD)** is a governance framework for human-AI collaboration that prioritizes real-world results over artifacts.
>
> The core thesis: development is about defining outcomes, enforcing constraints, and verifying reality—not writing code. AI accelerates execution; governance preserves trust.

## The 7 Pillars

Explain the foundational pillars:

1. **Prompt over Code** - Intent guides generation; code is ephemeral
2. **KISS** - Simplicity is non-negotiable; complexity requires justification
3. **DRY with Isolation** - Reuse without brittle coupling
4. **Consistency** - Behavioral predictability matters more than visual uniformity
5. **Maintainability** - Systems must survive creator turnover
6. **Antifragile** - Recovery paths are preferred over prevention; failure is assumed
7. **Scalable** - Growth must be bounded in cost, complexity, and human attention

## Core Terminology

Explain the precise ODD vocabulary - these terms have specific meanings:

| Term | ODD Meaning | NOT This |
|------|-------------|----------|
| **Outcome** | A verifiable state of reality that can be demonstrated | A deliverable, artifact, or checkbox |
| **Evidence** | Observable proof that an outcome occurred (reproducible/recorded) | Explanation, confidence, or assertion |
| **Artifact** | A byproduct of work (code, docs). Ephemeral by default | The goal or proof of value |
| **Elevation** | Promoting a verified truth from working memory to Canon | Filing or archiving |
| **Canon** | Curated truths that have earned permanence through verification | A wiki or documentation dump |
| **Attempt** | A bounded execution against a defined goal with evidence | A vague "try" or experiment |
| **Lane** | A parallel track of work with its own lifecycle and evidence | A branch or generic workstream |

### Anti-Patterns in Language

Warn users about these common mistakes:
- **Confidence as Evidence** - "I'm confident this works" is not evidence
- **Explanation as Proof** - "Let me explain why this is correct" is not proof
- **Activity as Progress** - "I worked on this for hours" is not progress
- **Artifact as Outcome** - "The code is written" is not an outcome

## Document Tiers

Explain the epistemic obligation system:

| Tier | Obligation | Description |
|------|------------|-------------|
| **Tier 0** | Scope exclusion | Public-facing, excluded from agent reasoning |
| **Tier 1** | Foundational | Must absorb fully. Do not contradict. |
| **Tier 2** | Shared | Should respect by default. Document deviations. |
| **Tier 3** | Awareness | Reference when relevant. May ignore otherwise. |

**Important**: Tiers describe epistemic obligation, NOT importance. A Tier 3 doc might be critical for today's task while a Tier 1 doc is philosophically foundational but irrelevant.

## Project Maturity Assessment

Ask the user to identify their project's maturity level:

**Level 0 — PoC / Exploration**
- Goal: Learn quickly
- Artifacts are non-authoritative
- Verification demonstrates possibility
- Over-governance is prohibited

**Level 1 — Pilot / Product**
- Goal: Deliver value safely
- Evidence and visual proof required
- Tradeoffs must be explicit
- Silent failure is unacceptable

**Level 2 — Production / Long-Term**
- Goal: Sustain trust
- Outcomes must be measurable
- Observability, reversibility, and security are mandatory
- Autonomous actions require stop conditions and human gates

Ask: "What maturity level best describes your current project?"

## Recommended Structure

If they want to fully adopt ODD, recommend this structure:

```
project/
├── canon/                    # Governance artifacts
│   ├── constraints.md        # Project-specific constraints
│   ├── decision-rules.md     # Decision heuristics
│   └── definition-of-done.md # Completion requirements
├── docs/
│   └── PRD.md               # Active Product Requirements Document
└── .claude.md               # Claude Code instructions
```

## Key Concepts to Explain

1. **Evidence Over Assertion** - Work is only done when verified with evidence
2. **Restartability Over Salvage** - Clean restarts with better constraints are progress
3. **Memory Is the Bottleneck** - In AI-accelerated development, durable intent is scarce, not computation

## Next Steps

Suggest the user:
1. Run `/constraints` to review which ODD constraints apply to their project
2. Run `/create-prd` when ready to create a Product Requirements Document
3. Use `/dod` to verify work completion
4. Use `/self-audit` before declaring any significant work complete

## Resources

Point them to the full ODD documentation in `docs/prd-guide-pack.md` for deeper learning.
