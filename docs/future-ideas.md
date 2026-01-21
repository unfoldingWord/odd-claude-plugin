# Future Ideas for ODD Plugin

This document tracks enhancement ideas for future versions of the ODD Claude Code plugin.

## v2.0 Ideas

### Enhanced `/odd-init` - File Creation

**Current**: `/odd-init` provides guidance only, no file creation.

**Future**: Add option to create actual project structure:

```
project/
├── canon/
│   ├── constraints.md        # Project-specific constraints
│   ├── decision-rules.md     # Decision heuristics
│   └── definition-of-done.md # Completion requirements
├── docs/
│   └── PRD.md               # Active PRD template
└── .claude.md               # ODD-aware Claude instructions
```

**Rationale**: Some teams want a one-command setup to bootstrap ODD governance in new projects.

---

### Evidence Capture Helpers

**Idea**: Commands or hooks that help capture evidence:
- Screenshot capture integration
- Screen recording helpers
- Test output collection
- Deployment verification

**Rationale**: Evidence production is a key ODD requirement, but capturing it can be friction-heavy.

---

### Maturity Level Tracking

**Idea**: Track and enforce project maturity level:
- Store maturity level in project config
- Adjust command behavior based on level (PoC vs Production)
- Warn when actions don't match maturity governance

**Rationale**: ODD applies progressive governance based on maturity. Automated tracking would help teams stay consistent.

---

### ODD-Aligned Code Review Skill

**Idea**: A skill that reviews code changes against ODD principles:
- Check for evidence of verification
- Validate constraints are respected
- Flag missing tradeoff documentation
- Ensure Definition of Done is met before merge

**Rationale**: Code review is a natural checkpoint for ODD compliance.

---

### Project Management Integration

**Idea**: Hooks or commands that sync with project management tools:
- Create PRDs that sync with issue trackers
- Update attempt status in external tools
- Track Definition of Done completion

**Rationale**: Teams using ODD often have existing workflows that could benefit from integration.

---

### Attempt Lifecycle Management

**Idea**: Commands to manage PRD attempts:
- `/attempt-start` - Begin a new attempt against active PRD
- `/attempt-seal` - Close or abandon an attempt with evidence
- `/attempt-review` - Compare attempts against PRD criteria

**Rationale**: ODD treats attempts as first-class concepts. Tooling would help teams follow the attempt lifecycle.

---

### Canon Drift Detection

**Idea**: Periodic checks for drift between stated constraints and actual practice:
- Analyze recent commits against documented constraints
- Surface potential constraint violations
- Recommend canon updates when drift is detected

**Rationale**: Canon documents can become stale. Automated drift detection would help maintain alignment.

---

## Contributing Ideas

If you have ideas for future versions, consider:
1. Does this align with ODD principles?
2. Does it reduce friction without adding bureaucracy?
3. Can the value be verified with evidence?

Add ideas to this document with:
- Clear description
- Rationale explaining the value
- Any known tradeoffs
