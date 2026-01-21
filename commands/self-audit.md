---
description: Run the ODD self-audit checklist to verify work is complete before declaring done
---

# Self-Audit

Walk through the ODD self-audit checklist to verify work completion.

## Your Role

You are helping the user audit their own work against ODD standards. Guide them through each section, asking probing questions. Be thorough but not bureaucratic.

## Core Principle

> Builders—human or AI—must audit their own work against stated outcomes, constraints, and evidence. If an item cannot be answered, that is a signal—not a failure.

## Checklist Process

Walk through these 9 areas one at a time. For each area, ask the user to provide their answer before moving to the next.

### 1. Intended Outcome

Ask:
- "What outcome was this work intended to achieve?"
- "How will someone know if that outcome was achieved?"

**Red flags**: Vague outcomes, feature lists instead of outcomes, unmeasurable goals.

### 2. Constraints Applied

Ask:
- "Which constraints were relevant to this task?" (e.g., offline-first, maintainability, interoperability)
- "Were any default constraints intentionally overridden? If yes, why?"

**Red flags**: No constraints considered, implicit overrides without documentation.

### 3. Decision Rules Followed

Ask:
- "Which decision rules guided your approach?" (e.g., Borrow→Bend→Break→Build, KISS, explicit tradeoffs)
- "Were there moments where a different rule could have been applied? Why wasn't it?"

**Red flags**: No conscious decision-making process, unexplained choices.

### 4. Verification Performed

Ask:
- "What was run or exercised to verify the work?"
- "What behavior was directly observed?"

**Red flags**: "It should work", "I reviewed the code", no actual execution.

### 5. Evidence Produced

Ask:
- "What evidence proves the behavior occurred?" (screenshots, recordings, logs, rendered output)
- "Where can this evidence be found?"

**Red flags**: No evidence, evidence predates the change, vague references.

### 6. UX & Behavior Check (If Applicable)

If the work affects UI or user interaction, ask:
- "Does the UI or interaction behave as expected?"
- "Is the behavior understandable without explanation?"
- "If explanation is required, is that a UX smell?"

**Red flags**: Long explanations compensating for confusing UX.

### 7. Tradeoffs & Risks

Ask:
- "What tradeoffs were made?"
- "What risks remain?"
- "What assumptions could be wrong?"

**Red flags**: No acknowledged tradeoffs (every decision has them), hidden assumptions.

### 8. Maintainability Check

Ask:
- "Would someone else understand this in six months?"
- "What would be the hardest part to maintain or change?"

**Red flags**: Tribal knowledge dependencies, clever but opaque solutions.

### 9. Confidence Level

Ask:
- "How confident are you that this works as intended?" (Low / Medium / High)
- "What would increase confidence further?"

**Red flags**: High confidence without evidence, no path to higher confidence.

## Completion Report

After going through all 9 areas, compile a summary:

```markdown
## Self-Audit Report

**Work**: [Description of work audited]
**Date**: [Date]
**Audited by**: [Name]

### Outcome
[What was achieved]

### Constraints Applied
- [List constraints]

### Verification
- [What was run/tested]

### Evidence
- [Links/descriptions of evidence]

### Tradeoffs
- [List acknowledged tradeoffs]

### Risks
- [Remaining risks]

### Confidence
[Low/Medium/High] - [Reasoning]

### Status
[ ] Ready to declare done
[ ] Needs additional work: [What]
```

## Minimum Acceptable Completion

Remind the user that at minimum, completed work must include:
- A stated outcome
- At least one verification step
- At least one piece of evidence
- Acknowledgment of tradeoffs or unknowns

If these are missing, the task is not complete.
