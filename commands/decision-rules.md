---
description: Get guidance from the 14 ODD decision heuristics when making choices
---

# Decision Rules

Get guidance from ODD decision heuristics when making choices.

## Your Role

Help the user apply ODD decision rules to their current situation. Understand their context, identify relevant rules, and provide actionable guidance.

## Core Principle

> These rules describe how decisions tend to be made when designing systems. They are defaults applied unless there is a clear reason not to. If a rule is overridden, the reason should be stated explicitly.

## How to Use This Command

Ask the user: "What decision are you facing?" Then identify which rules are most relevant and walk through them.

---

## The 14 Decision Rules

### 1. Outcomes Before Implementation

> Define the outcome before choosing tools, architectures, or code.

**How to apply**:
- Ask what problem is actually being solved
- Avoid committing to implementation details too early
- Delete work that doesn't move the outcome forward

**Signals this rule was violated**:
- The solution is impressive but unclear in purpose
- Success criteria are vague or missing
- The system "works" but doesn't help anyone

---

### 2. Borrow → Bend → Break → Build

> Follow a progression when deciding how much to create from scratch.

**The order**:
1. **Borrow** — Use an existing tool as-is
2. **Bend** — Extend or configure an existing tool
3. **Break** — Fork or partially replace an existing tool
4. **Build** — Create something new from components

**How to apply**:
- Start at Borrow and justify moving down the list
- Building from scratch requires explicit justification

**Signals this rule was violated**:
- Reinventing something stable and well-understood
- Forking without a clear maintenance plan

---

### 3. Simplicity Wins by Default (KISS)

> Choose the simplest solution that plausibly works.

**How to apply**:
- Reject unnecessary abstraction
- Prefer readable code over clever code
- Add complexity only when simplicity demonstrably fails

**Signals this rule was violated**:
- Explanations are longer than the code
- Only the original author understands the system

---

### 4. DRY, But Not at the Cost of Isolation

> Avoid duplication, but not if it creates brittle coupling.

**How to apply**:
- Allow duplication across bounded contexts
- Extract shared logic only when reuse is proven
- Avoid "god modules" shared by everything

**Signals this rule was violated**:
- Small changes cause widespread breakage
- Teams are blocked waiting on shared components

---

### 5. Prefer Explicit State Over Implicit State

> Choose designs where state is visible, named, and bounded.

**How to apply**:
- Avoid hidden global state
- Make lifecycle and ownership explicit
- Prefer passing state over reaching for it

**Signals this rule was violated**:
- Bugs depend on execution order
- Restarting the system produces surprising behavior

---

### 6. Favor Recoverability Over Perfection

> Prefer systems that fail safely and recover easily over systems that try to prevent all failure.

**How to apply**:
- Design for partial failure
- Assume components will break
- Prefer restartable, replayable processes

**Signals this rule was violated**:
- A single failure takes everything down
- Recovery requires deep expertise or manual intervention

---

### 7. Make Tradeoffs Visible Early

> Name tradeoffs as part of the design, not as a postmortem.

**How to apply**:
- Document why a choice was made
- Acknowledge what the choice sacrifices
- Leave breadcrumbs for future maintainers

**Signals this rule was violated**:
- Future changes require archaeology
- Decisions feel arbitrary in hindsight

---

### 8. Optimize for the Next Maintainer

> Assume the next person to touch the system is not you.

**How to apply**:
- Favor clarity over personal preference
- Document non-obvious decisions
- Avoid designs that require constant explanation

**Signals this rule was violated**:
- The system works but no one wants to touch it
- Knowledge exists only in conversations or chat logs

---

### 9. UI Should Carry the Explanation

> Prefer showing over telling, especially in user-facing systems.

**How to apply**:
- Let interfaces demonstrate behavior
- Keep explanatory text short
- Ask permission before going deep

**Signals this rule was violated**:
- Long explanations compensate for confusing UX
- Users need documentation to complete basic tasks

---

### 10. If It Can't Be Verified, It Isn't Done

> Do not consider work complete unless it is verified.

**How to apply**:
- Run the system
- Observe behavior directly
- Require visual or test evidence

**Signals this rule was violated**:
- Confidence is based on reasoning alone
- Bugs are discovered by users instead of builders

---

### 11. Escalate Only When Defaults Fail

> Start with defaults and escalate only when necessary.

**How to apply**:
- Try the obvious solution first
- Gather evidence before increasing complexity
- Treat escalation as a signal, not a failure

**Signals this rule was violated**:
- Overengineering early
- Complex solutions to simple problems

---

### 12. Say "I Don't Know" Early

> Prefer admitting uncertainty to pretending confidence.

**How to apply**:
- Name unknowns explicitly
- Design experiments to reduce uncertainty
- Avoid locking in assumptions prematurely

**Signals this rule was violated**:
- Decisions are justified with vague confidence
- Surprises appear late and expensively

---

### 13. Prefer One-Shot Builds; Don't Steer a Miss

> Fix the asset (PRD, constraints, inputs) and re-run clean over steering a multi-turn miss.

**How to apply**:
- Treat a failed execution path as signal, not a trajectory to nurse
- If context decays, restart with corrected inputs rather than accumulating patches
- Preserve the attempt as evidence, then begin a new attempt independently

**Signals this rule was violated**:
- "Just one more tweak" turns into extended steering
- The system only works if the same person keeps nudging it
- The final outcome cannot be reproduced from a clean start

---

### 14. Don't Hard-Code Domain Tables; Hard-Code Protocol Contracts

> Avoid hard-coding domain lookups that can be derived or updated. Do hard-code protocol contracts that define interoperability.

**How to apply**:
- If it's "data," prefer it to live in content, configuration, or a source of truth
- If it's "interface," prefer it to be explicit and enforced in code

**Signals this rule was violated**:
- Large in-code tables that drift from reality
- Domain updates require redeploys without justification
- Integrations fail because the "contract" was implicit or inconsistent

---

## Applying Rules to Your Decision

After identifying the user's decision context:

1. **List relevant rules** (usually 2-4 are most applicable)
2. **Explain how each applies** to their specific situation
3. **Identify potential conflicts** between rules
4. **Recommend an approach** with explicit tradeoffs

## Decision Summary Template

```markdown
## Decision: [Description]

### Relevant Rules
1. [Rule name] - [How it applies]
2. [Rule name] - [How it applies]

### Recommendation
[Recommended approach]

### Tradeoffs
- [What this choice sacrifices]
- [What could go wrong]

### Override Justification (if any)
[If overriding a default rule, explain why]
```

## Remember

> These rules describe how decisions tend to be made, not how decisions must always be made. State clearly when a rule is overridden and why.
