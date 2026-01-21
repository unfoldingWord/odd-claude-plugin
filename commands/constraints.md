---
description: Review and apply the 10 ODD constraints to current work
---

# Constraints

Review and apply ODD constraints to the current work.

## Your Role

Help the user understand which ODD constraints apply to their work and document any overrides explicitly.

## Core Principle

> Constraints define the baseline assumptions and design defaults applied to most work. Unless explicitly stated otherwise, these constraints should be assumed to apply.

## The 10 ODD Constraints

Walk through each constraint with the user. For each one, help them determine:
- Does this apply?
- If not, why not? (document the override)

---

### 1. Offline-First (Default)

**Assumption**: Network connectivity is unreliable, intermittent, or unavailable.

**What this forces**:
- Core functionality must work without a network
- Data is stored locally first
- Synchronization is opportunistic, not assumed
- Conflicts are expected and must be resolvable

**When it does NOT apply**:
- Short-lived internal tools
- One-off demos where offline support would distort the experiment
- Explicitly cloud-only systems (must be stated)

**Ask**: "Does your work need to function offline or with unreliable connectivity?"

---

### 2. Long Timelines & Changing Ownership

**Assumption**: Systems will live longer than their original creators and will change hands.

**What this forces**:
- Clear separation of concerns
- Minimal hidden state
- Explicit documentation as part of the product
- Avoidance of "tribal knowledge" dependencies

**When it does NOT apply**:
- Throwaway prototypes
- Time-boxed experiments with a defined end date

**Ask**: "Will this work outlive you or be maintained by others?"

---

### 3. Maintainability Over Cleverness

**Assumption**: Maintenance cost usually exceeds build cost, especially over long timelines.

**What this forces**:
- Preference for simple, boring solutions
- Avoidance of unnecessary abstractions
- Clear tradeoffs documented when complexity is introduced

**When it does NOT apply**:
- Exploratory research prototypes
- Performance-critical paths where simplicity is insufficient

**Ask**: "Is this solution understandable by someone who didn't write it?"

---

### 4. Interoperability Over Feature Completeness

**Assumption**: Closed or tightly coupled systems limit collaboration and age poorly.

**What this forces**:
- Preference for open formats and protocols
- Loose coupling between components
- Clear interfaces instead of shared internals

**When it does NOT apply**:
- Highly specialized tools with no external integration needs
- Temporary scaffolding code

**Ask**: "Does this work need to integrate with other systems or be replaceable?"

---

### 5. Stateless or Low-State by Default

**Assumption**: State increases complexity, failure modes, and recovery cost.

**What this forces**:
- Explicit state boundaries
- Externalized persistence where necessary
- Clear lifecycle management

**When it does NOT apply**:
- Systems whose core value is stateful (editors, long-running workflows)
- Performance-critical stateful processes (must be justified)

**Ask**: "Is the state in this work explicit and bounded?"

---

### 6. AI as Accelerator, Not Authority

**Assumption**: AI systems hallucinate, optimize for plausibility over correctness, and require human judgment.

**What this forces**:
- Human-defined outcomes
- Verification and evidence requirements
- Explicit refusal when confidence is not warranted

**When it does NOT apply**:
- **Never.** This constraint is always in effect.

**Ask**: "Is AI output being verified, or assumed correct?"

---

### 7. Evidence Over Assertion

**Assumption**: Assertions like "it works" are unreliable without proof.

**What this forces**:
- Running the system
- Observing behavior directly
- Producing visual or test evidence

**When it does NOT apply**:
- Purely conceptual or theoretical work (must be labeled as such)

**Ask**: "What evidence proves this works?"

---

### 8. UX Is Contextual, Not Universal

**Assumption**: Users vary by language, culture, technical experience, and environment. Universal UX claims often hide bias.

**What this forces**:
- Context-specific design decisions
- Willingness to diverge from mainstream patterns
- Clear explanation of UX tradeoffs

**When it does NOT apply**:
- Internal tools for a well-defined, homogeneous user group

**Ask**: "Who are the actual users, and what are their contexts?"

---

### 9. Ephemeral Artifacts Are Acceptable

**Assumption**: AI makes regeneration cheap. Maintaining everything forever is unnecessary.

**What this forces**:
- Focus on outcomes over artifacts
- Willingness to discard and regenerate
- Durable principles instead of durable repos

**When it does NOT apply**:
- Canonical data
- Long-term user content
- Legal or compliance artifacts

**Ask**: "Does this artifact need to persist, or can it be regenerated?"

---

### 10. Explicit Tradeoffs

**Assumption**: Every decision excludes alternatives. Unspoken tradeoffs cause confusion later.

**What this forces**:
- Short explanations of why choices were made
- Acknowledgment of downsides
- Easier future revision

**When it does NOT apply**:
- Truly trivial decisions

**Ask**: "What was sacrificed to make this choice?"

---

## Constraint Summary

After reviewing all constraints, compile a summary:

```markdown
## Constraints Applied

**Work**: [Description]
**Date**: [Date]

### Active Constraints
- [ ] Offline-First
- [ ] Long Timelines
- [ ] Maintainability Over Cleverness
- [ ] Interoperability
- [ ] Low-State
- [ ] AI as Accelerator (always active)
- [ ] Evidence Over Assertion
- [ ] Contextual UX
- [ ] Ephemeral Artifacts
- [ ] Explicit Tradeoffs

### Overrides
| Constraint | Override Reason |
|------------|-----------------|
| [Constraint] | [Why it doesn't apply] |

### Notes
[Any additional context]
```

## Remember

> These constraints define defaults, not laws. Agents and collaborators should assume these constraints apply, and explicitly note when a constraint is overridden or does not apply.
