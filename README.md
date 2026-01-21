# ODD - Outcomes-Driven Development Plugin for Claude Code

A Claude Code plugin that provides governance tools for human-AI collaboration based on the **Outcomes-Driven Development (ODD)** framework.

## What is ODD?

Outcomes-Driven Development is a governance framework that prioritizes real-world results over artifacts. The core thesis:

> Development is about defining outcomes, enforcing constraints, and verifying reality—not writing code. AI accelerates execution; governance preserves trust.

### The 7 Pillars

1. **Prompt over Code** - Intent guides generation; code is ephemeral
2. **KISS** - Simplicity is non-negotiable
3. **DRY with Isolation** - Reuse without brittle coupling
4. **Consistency** - Behavioral predictability matters
5. **Maintainability** - Systems must survive creator turnover
6. **Antifragile** - Recovery paths preferred over prevention
7. **Scalable** - Growth bounded in cost, complexity, and attention

## Installation

### Prerequisites

- Claude Code version **1.0.33 or later**

### From GitHub

```bash
# Step 1: Add the marketplace
/plugin marketplace add unfoldingWord/odd-claude-plugin

# Step 2: Install the plugin
/plugin install odd-claude-plugin@unfoldingWord
```

For project-wide installation (shared with collaborators via `.claude/settings.json`):

```bash
/plugin install odd-claude-plugin@unfoldingWord --scope project
```

### Local Development

```bash
# Clone the repo
git clone https://github.com/unfoldingWord/odd-claude-plugin.git

# Add as local marketplace
/plugin marketplace add ./odd-claude-plugin

# Install (use the plugin name from plugin.json)
/plugin install odd@odd-claude-plugin
```

### Verify Installation

Run `/plugin` and check the "Installed" tab to confirm the plugin is active.

## Available Commands

### `/odd-init`
Initialize ODD governance in your project. Provides guidance on:
- The ODD framework and 7 pillars
- Project maturity levels (PoC → Pilot → Production)
- Recommended folder structure
- Next steps

### `/self-audit`
Run through the 9-area self-audit checklist before declaring work complete:
1. Intended Outcome
2. Constraints Applied
3. Decision Rules Followed
4. Verification Performed
5. Evidence Produced
6. UX & Behavior Check
7. Tradeoffs & Risks
8. Maintainability Check
9. Confidence Level

### `/dod`
Check if work meets the ODD Definition of Done requirements:
1. Change Description - What changed, where, and why
2. Verification Performed - What was run or checked
3. Observed Behavior - What actually happened
4. Evidence Produced - Proof of behavior
5. Self-Audit Completed - Reflection against constraints

### `/create-prd`
Interactive PRD (Product Requirements Document) creation through 7 stages:
1. Outcome Discovery
2. Success Criteria
3. Non-Goals and Scope
4. Constraints
5. Definition of Done
6. Risks and Tradeoffs
7. Draft Assembly

### `/constraints`
Review and apply the 10 ODD constraints:
1. Offline-First (Default)
2. Long Timelines & Changing Ownership
3. Maintainability Over Cleverness
4. Interoperability Over Feature Completeness
5. Stateless or Low-State by Default
6. AI as Accelerator, Not Authority
7. Evidence Over Assertion
8. UX Is Contextual, Not Universal
9. Ephemeral Artifacts Are Acceptable
10. Explicit Tradeoffs

### `/decision-rules`
Get guidance from the 14 ODD decision heuristics when facing choices:
- Outcomes Before Implementation
- Borrow → Bend → Break → Build
- Simplicity Wins (KISS)
- DRY with Isolation
- And 10 more...

## Agents

### PRD Guide Agent
A dedicated agent for thorough, multi-turn PRD creation. More in-depth than the `/create-prd` command, with:
- Probing questions at each stage
- Push-back on vague or untestable statements
- Comprehensive PRD assembly

## Progressive Governance

ODD applies different levels of rigor based on project maturity:

| Level | Stage | Governance |
|-------|-------|------------|
| 0 | PoC / Exploration | Bias toward speed; over-governance prohibited |
| 1 | Pilot / Product | Evidence required; tradeoffs explicit |
| 2 | Production | Outcomes measurable; security mandatory |

## Key Concepts

### Evidence Over Assertion
> Work is not complete unless it is verified with evidence. Assertions like "this should work" do not count.

### Restartability Over Salvage
> Clean restarts with better constraints are progress. Restarting is not failure.

### Memory Is the Bottleneck
> In AI-accelerated development, durable intent is scarce—not computation.

## Documentation

Full ODD documentation is available in `docs/prd-guide-pack.md`, including:
- Complete constraints definitions
- All 14 decision rules with examples
- Definition of Done requirements
- Self-audit checklist details
- PRD template and creation guide

## Future Ideas

See `docs/future-ideas.md` for planned enhancements including:
- File creation in `/odd-init`
- Evidence capture helpers
- Maturity level tracking
- Code review integration

## Contributing

Contributions welcome! When contributing, please:
1. Follow ODD principles (evidence over assertion)
2. Include verification of changes
3. Document tradeoffs explicitly

## License

MIT

---

> ODD is about preserving intent without freezing execution. The measure of success is not how elegant the artifact is, but whether the outcome holds up in the real world.
