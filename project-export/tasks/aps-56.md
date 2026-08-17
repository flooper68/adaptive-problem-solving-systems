---
entity:
  identity:
    type: key
    value: APS-56
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:37:17.284Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:56.027Z
  key: APS-56
  keyNumber: 56
  labels:
    - repository-import
    - aps-legacy
  originSchedule: null
  originSession: null
  originTask: null
  parent: null
  priority: 3
  problem: null
  queuePosition: null
  startedAt: null
  status: done
  summary: Imported terminal state from repository source.
  title: Define a grilling protocol for task candidates
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:56.029Z
---

# Define a grilling protocol for task candidates

## Idea

Create a structured discussion protocol that helps a person turn an initial
observation into a well-understood task candidate and distinguish ideas,
insights, issues, problems, and proposed solutions.

## Motivation

Early ideas often arrive with missing context or a proposed solution embedded
in an unclear need. A reusable grill could elicit the affected consumer,
observed condition, evidence, impact, assumptions, uncertainty, urgency, and
possible next step while preserving the source's original meaning.

## Evidence

- At capture,
  [`operations/processes/task-intake.md`](../../processes/task-intake.md)
  defined minimum capture but no interactive elicitation protocol. It now
  includes a short adaptive clarification conversation.
- [`operations/processes/task-grooming.md`](../../processes/task-grooming.md)
  defines framing and readiness questions after capture.
- The normative framework recognizes discussion or grilling as an
  evidence-producing capability and allows source-specific protocols.
- The later
  [`brainstorming process`](../../processes/sessions/brainstorming.md) provides a
  general discussion/grilling protocol. Grooming must determine whether any
  task-specific protocol remains necessary beyond intake clarification.

## Open questions

- Is the grill part of intake, grooming, or a reusable protocol invoked by
  both?
- Which distinctions among observation, insight, issue, problem, opportunity,
  hypothesis, and solution are operationally useful?
- Which questions are always required, and which should adapt to the candidate
  type and available evidence?
- How should the grill avoid leading the source or forcing premature scope,
  priority, or solution decisions?
- What durable output should it create, and how should unanswered questions be
  represented?
- How will usefulness be validated without making low-cost capture burdensome?

## Grooming log

### 2026-07-10 — captured

Captured from the APS framework maintainer's proposal for a grilling process
that helps derive and clarify executable candidate actions from ideas,
insights, issues, and problems. Its relationship to the existing intake and
grooming processes remains open.

### 2026-08-07 — closed: superseded

Groomed in the
[first cadenced grooming invocation](../../streams/working-sessions/2026-08-06-first-cadenced-grooming.md);
approved by the maintainer. The need this task named is covered: intake now
runs a short adaptive clarification conversation (one load-bearing question
at a time), the brainstorming process carries the general discussion/grilling
protocol, and the per-kind intake and grooming processes this task referenced
were deleted in the consolidation. No task-specific protocol remains
necessary beyond what those processes state. **Closed as superseded** by
`processes/intake.md` and `processes/sessions/brainstorming.md`.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/task-candidate-grilling.md","legacyId":"apss.task-candidate-grilling"}

---

[repository-import:task:apss.task-candidate-grilling@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/task-candidate-grilling.md]
