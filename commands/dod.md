---
description: Check if work meets the ODD Definition of Done requirements with evidence verification
---

# Definition of Done Check

Verify that work meets the ODD Definition of Done requirements.

## Your Role

You are helping the user verify their work against ODD's Definition of Done. Be direct and honest. If requirements aren't met, say so clearly.

## Core Principle

> Work is not complete unless it is verified with evidence. Reasoning alone is insufficient. Assertions like "this should work" or "this is correct" do not count as completion.

## Terminology Precision

Apply ODD definitions strictly:

| Common Term | ODD Meaning | Common Misuse |
|-------------|-------------|---------------|
| "Done" | Evidence exists proving outcome | Code merged, ticket closed |
| "Works" | Verified under realistic conditions | Passed tests, "looks right" |
| "Documented" | Captured for future governance | Written down somewhere |
| "Tested" | Stress-tested against failure modes | Happy path confirmed |
| "Shipped" | Outcome delivered and verifiable | Artifact deployed |

**Evidence** = Observable proof that an outcome occurred. Must be reproducible or recorded. NOT explanation, confidence, or expert assertion.

**Outcome** = A verifiable state of reality that can be demonstrated. NOT a deliverable, artifact, feature, or checkbox.

## The 5 Requirements

A task is only considered done when ALL of the following are present:

### 1. Change Description

**Requirement**: What changed, where, and why.

Ask the user:
- "What specifically changed?"
- "Where in the codebase/system?"
- "Why was this change made?"

**Pass criteria**: Clear description connecting the change to an outcome.
**Fail criteria**: Vague descriptions like "updated code" or "fixed stuff".

### 2. Verification Performed

**Requirement**: What was run or checked to verify the change.

Ask the user:
- "What did you run to verify this works?"
- "Did you run the system, execute tests, load the page, or trigger the workflow?"

**Pass criteria**: Specific verification steps that were actually executed.
**Fail criteria**: "I reviewed the code", "It should work", "I didn't have time to test".

### 3. Observed Behavior

**Requirement**: What actually happened when the system was run.

Ask the user:
- "What behavior did you observe?"
- "Did it match the expected outcome?"

**Pass criteria**: Description of actual observed behavior.
**Fail criteria**: Expected behavior without observation, assumptions.

### 4. Evidence Produced

**Requirement**: Proof that the behavior matches the intended outcome.

Ask the user:
- "What evidence do you have?" (screenshots, recordings, logs, test output)
- "Was this evidence produced after the change?"
- "Can someone else verify using this evidence?"

**Pass criteria**: Concrete evidence (screenshot, log, test output) produced after the change.
**Fail criteria**: No evidence, evidence from before the change, verbal assurances.

**Visual Proof Required If**: The work affects UI, interaction, layout, user flow, or visible state.

### 5. Self-Audit Completed

**Requirement**: Brief audit against constraints and decision rules.

Ask the user:
- "Have you completed a self-audit?" (Run `/self-audit` if not)
- "What tradeoffs were made?"
- "What risks remain?"

**Pass criteria**: Documented reflection on constraints, decisions, and tradeoffs.
**Fail criteria**: No reflection, hidden assumptions, undocumented tradeoffs.

## Assessment Output

After checking all 5 requirements, provide an assessment:

```markdown
## Definition of Done Assessment

**Work**: [Description]
**Assessed**: [Date]

| Requirement | Status | Notes |
|-------------|--------|-------|
| 1. Change Description | PASS/FAIL | [Details] |
| 2. Verification Performed | PASS/FAIL | [Details] |
| 3. Observed Behavior | PASS/FAIL | [Details] |
| 4. Evidence Produced | PASS/FAIL | [Details] |
| 5. Self-Audit Completed | PASS/FAIL | [Details] |

### Overall Status: DONE / NOT DONE

### If NOT DONE - Next Steps:
[List what needs to be addressed]
```

## What Does NOT Count as Done

Explicitly call out if the user claims any of these as completion:
- "It compiles"
- "The logic is sound"
- "I reviewed the code"
- "This should work"
- "I didn't have time to test"

These are intermediate states, not "done."

## Partial Completion

If work is partially complete, help the user document:
- What was attempted
- What was verified
- What could not be verified
- What remains

> Ambiguity is worse than incompleteness. It's better to clearly state "this is not done" than to claim completion without evidence.

## Explicit Exceptions

The Definition of Done may be relaxed ONLY for:
- Conceptual design discussions
- Theoretical analysis
- Early ideation

In these cases, the output must be clearly labeled **"unverified"**.
