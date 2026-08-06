---
id: apss.feedback.current-state-first-class
type: framework-feedback
status: received
received: 2026-08-06
reporter: APS framework maintainer
source: Maintainer direction opening the current-state concept brainstorming session
related_feedback: []
related_work: [apss.current-state-reporting, apss.session.current-state-concept]
---

# Current state should be a first-class framework concept

## Report

### Context

On 2026-08-06 the [learning-loop application
session](../../working-sessions/2026-08-06-learning-loop-application.md) closed
the [current-state-reporting
task](../../../tasks/archive/current-state-reporting.md) as delivered: a thin
root [`STATE.md`](../../../STATE.md) plus a `Current state` section in each
problem file, date-stamped, refreshed at session delivery, and subordinate to
the authoritative problem, task, and session files. That was an Operations
implementation choice; the framework itself used the phrase "current state"
in its recoverability, working-session, and archive definitions without
defining it.

### Observed problem or outcome

The maintainer reports the pattern is very useful in operation, and that the
framework does not carry it as a defined concept.

### Desired outcome

Current state is a first-class concept in the framework.

### Suggested response

Promote the concept into the normative package. (Maintainer direction: "current
state should be a first class concept in the framework, it is very useful.")

### Evidence

- Operations use: `STATE.md` and P1's `Current state` section, delivered
  2026-08-06 and consulted for orientation since.
- Undefined prior use in the framework: task recoverability
  (`framework/README.md`), `Working-session record` and `Archive` vocabulary
  entries, and a visualization reference all leaned on the term.

## Grooming record

### 2026-08-06 — acted on directly by maintainer direction

The report arrived as the framing direction of the [current-state concept
brainstorming session](../../working-sessions/2026-08-06-current-state-concept.md),
which compiled the response in the same session: a `Current state` vocabulary
entry (owned state plus the optional derived current-state view), README
references, and a changelog entry. Clarification questions were not needed —
the delivered Operations implementation already answered the design questions
the closed task had left open. Delivery rides with the session scope rather
than intake's automatic path because the same session compiles the response.
