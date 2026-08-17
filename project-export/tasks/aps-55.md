---
entity:
  identity:
    type: key
    value: APS-55
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:37:16.127Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-55
  keyNumber: 55
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
  status: backlog
  summary: null
  title: Create a practical guide for defining a system
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T17:37:16.127Z
---

# Create a practical guide for defining a system

## Idea

Develop an approachable, step-by-step workflow that helps people move from an
unclear situation to an explicit, reviewable APS system definition.

## Motivation

The declaration contract describes the required result, while a practical guide
could help a new user discover the problem, boundary, outcome, participants,
artifact, components, relationships, evidence routes, operating context, validation,
learning loop, and current versus desired state in a useful order.

## Evidence

- [`framework/README.md`](../../framework/README.md) contains a concise
  ten-step “Creating a system” checklist.
- [`framework/SCHEMA.md`](../../framework/SCHEMA.md) defines the declaration
  shape, contract, and authoring template.
- Framework Operations is the first concrete APS application, but no guided
  walkthrough currently takes a person from an ambiguous starting point to a
  validated definition.
- No consumer trial yet shows where the existing checklist is insufficient.

## Open questions

- Should this extend the normative framework, become a non-normative playbook,
  or be an interactive tool or grill?
- Which starting contexts should it support: defining a new system, extracting
  one from existing work, or diagnosing an incomplete system?
- How should it help users test system boundaries and distinguish a system from
  a process, capability, project, or artifact?
- Which diagrams, examples, prompts, and intermediate worksheets would add
  value?
- How should the guide handle iteration when later steps invalidate earlier
  assumptions?
- What user exercise would demonstrate that the guide improves definition
  quality and usability?

## Grooming log

### 2026-07-10 — captured

Captured from the APS framework maintainer's proposal for a step-by-step guide
to defining a system. The existing concise checklist is treated as a starting
point rather than duplicated.

### 2026-08-07 — keep; reconsideration trigger recorded

Groomed in the
[first cadenced grooming invocation](../streams/working-sessions/2026-08-06-first-cadenced-grooming.md);
approved by the maintainer. Kept open without current work — out of P1's MVP
scope. Reconsider when: sharing or adoption work begins, or the linked [onboarding insight](../streams/insights/archived/2026-07-11-incremental-onboarding-can-teach-system-definition.md) trigger fires.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/system-definition-guide.md","legacyId":"apss.system-definition-guide"}

---

[repository-import:task:apss.system-definition-guide@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/system-definition-guide.md]
