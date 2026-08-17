---
entity:
  identity:
    type: key
    value: APS-6
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:34.670Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-6
  keyNumber: 6
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
  title: Define reusable processes for producing good evidence
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T17:36:34.670Z
---

# Define reusable processes for producing good evidence

## Idea

Define a small set of general process patterns that can be reused across APS
implementations, including guidance for conducting good research and good
experiments.

## Motivation

The framework names research, experimentation, and discussion as general
evidence-producing capabilities but leaves their protocols to each system.
Reusable guidance could help implementers produce credible evidence without
requiring every system to design basic quality practices from scratch.

## Evidence

- The normative framework identifies research and experimentation as general
  capabilities while explicitly allowing domain-specific protocols.
- The operations-specific
  [`brainstorming process`](../processes/sessions/brainstorming.md) now defines a
  lightweight discussion protocol. No artifact yet establishes reusable,
  cross-domain quality guidance for all three capabilities.
- No evidence yet establishes which process patterns are sufficiently general
  across APS domains.

## Open questions

- Which processes are genuinely cross-domain, and which require specialized
  variants?
- Should the result be normative minimum requirements, non-normative playbooks,
  templates, or examples?
- What does “good” mean for research, experimentation, discussion, observation,
  and knowledge compilation?
- How can rigor, proportionality, reproducibility, ethics, and stopping
  conditions be expressed without imposing excessive ceremony?
- Which external standards or scientific sources should inform the guidance?

## Grooming log

### 2026-07-09 — captured

Captured from the APS framework maintainer's proposal for generally useful
processes such as good research and good experimentation. The scope and
normative status remain intentionally unresolved for grooming.

### 2026-08-07 — keep; reconsideration trigger recorded

Groomed in the
[first cadenced grooming invocation](../streams/working-sessions/2026-08-06-first-cadenced-grooming.md);
approved by the maintainer. Kept open without current work — out of P1's MVP
scope. Reconsider when: an evidence-quality gap is observed in an invocation, or P1 closes.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/general-evidence-processes.md","legacyId":"apss.general-evidence-processes"}

---

[repository-import:task:apss.general-evidence-processes@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/general-evidence-processes.md]
