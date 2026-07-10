---
id: apss.feedback.unbounded-stream-indexes
type: framework-feedback
status: received
received: 2026-07-10
reporter: APSS framework maintainer
source: Maintainer report in Codex task
related_feedback: []
related_work: []
---

# Exhaustive README indexes do not scale with unbounded streams

## Report

### Context

The reporter was reviewing the stewardship backlog README and its role as the
entry point to a collection that may continue growing without a fixed bound.

### Observed problem or outcome

The backlog README links every backlog item. This makes the README progressively
less useful as navigation and creates an indefinitely growing, manually
maintained index. The same pattern may affect other stream READMEs whose
collections are also potentially unbounded.

### Desired outcome

Stream documentation remains useful and maintainable as its collection grows,
without requiring an exhaustive list of every retained item in the README.

### Suggested response

No specific response was proposed. Any response should consider the backlog and
other potentially unbounded streams consistently rather than treating the
current backlog list as an isolated case.

### Evidence

- Maintainer report based on reviewing the backlog README.
- [`operations/work/backlog/README.md`](../../work/backlog/README.md) currently
  contains an `Items` section linking every retained backlog item.
- [`operations/streams/framework-feedback/README.md`](README.md) currently
  contains a `Reports` section, suggesting the same scaling concern may apply
  here; the broader reach has not yet been assessed.

## Grooming record

Not yet groomed. See
[`framework-feedback-grooming.md`](../../processes/framework-feedback-grooming.md).
