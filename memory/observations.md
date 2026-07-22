# Research Protocol Observations & Process Log

> **PURPOSE**: Backlog for capturing process improvements, recurring edge cases, model execution misses, or protocol adjustments based on real research runs.

---

## Observation Log Template

### Observation [N]: [Short Title]
- **Status**: [ OPEN | ACTIONED | DECLINED ]
- **Date**: YYYY-MM-DD
- **Target Component**: [ Core Protocol | Claude Adapter | OpenAI Adapter | Gemini Adapter | NotebookLM Guide | Workflows ]
- **Observed Failure / Edge Case**: [What process failure or ambiguity occurred?]
- **Suggested Protocol Fix**: [What small rule change or guardrail prevents it next time?]

---

## Active Observations

### Observation 001: Explicit Restricted Mode Turn Counter
- **Status**: ACTIONED
- **Date**: 2026-07-22
- **Target Component**: Claude Adapter (`adapters/claude/SKILL.md`)
- **Observed Failure / Edge Case**: Restricted Mode counter `[1/2]` was lost when context summarization occurred during long chats.
- **Suggested Protocol Fix**: Explicitly format turn counters as `[Restricted Mode 1/2]` and `[Restricted Mode 2/2]` in every response body.
