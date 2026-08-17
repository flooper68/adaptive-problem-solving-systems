---
entity:
  identity:
    type: key
    value: APS-R-9
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:40:45.221Z
  dispositionNote: null
  groomed: false
  key: APS-R-9
  keyNumber: 9
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-16T19:40:45.221Z
---

# Visualization tooling is missing

## Report

### Context

The reporter was assessing the framework as an operable system definition and
wanted a useful visual representation of a declared system.

### Observed problem or outcome

APSS describes how systems should be visualized, but the repository provides no
tool that turns one or more `SYSTEM.md` declarations into a usable visual
artifact. A consumer must manually translate declarations into diagrams, which
makes the visualization guidance harder to apply and allows generated views to
drift from the source of truth.

### Desired outcome

A consumer can run a provided tool against APSS system declarations and receive
a clear, attractive visual HTML representation suitable for exploring and
communicating the system.

### Suggested response

Provide a script that reads the system declarations and generates polished
visual HTML.

### Evidence

- Maintainer report based on inspection and attempted use of the framework.
- [`framework/VISUALIZATION.md`](../../../../framework/VISUALIZATION.md)
  already defines derived views and a generation contract.
- No generator or executable visualization tool exists in the repository as of
  2026-07-09.

## Grooming record

### 2026-07-09 — actionable

- **Participants:** APSS framework maintainer and Codex operator.
- **Evidence consulted:** the report, the normative visualization contract,
  the system schema, and the repository file set.
- **Clarified experience:** the framework specifies visual projections but
  leaves consumers to implement them manually.
- **Underlying need:** make declared APSS systems inspectable and communicable
  without duplicating declaration data or designing a renderer from scratch.
- **Proposed response:** a repository-provided script that generates polished
  visual HTML. The choice of runtime, rendering library, interaction model, and
  packaging remains open.
- **Scope:** supporting tooling derived from the normative framework; this does
  not yet require changing APSS semantics.
- **Reach and impact:** directly affects any consumer who needs to orient within
  or communicate a non-trivial system hierarchy. Manual diagrams are a
  workaround, but cost effort and can drift from declarations.
- **Confidence:** high that the tool is absent and the generation contract
  exists; usability and portability requirements still need validation with a
  generated prototype.
- **Disposition:** `actionable`. A bounded investigation and implementation
  candidate is justified because the missing tool prevents consumers from
  directly exercising an already documented contract.
- **Linked work:** `apss.visual-html-generator`, captured in
  [`operations/tasks/visual-html-generator.md`](../../../tasks/visual-html-generator.md).
- **Follow-up:** report acknowledged through this retained record. Validate a
  future implementation using at least the operations system and one example,
  then obtain consumer feedback on clarity and usefulness before marking this
  report `addressed`.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/framework-feedback/archived/2026-07-09-visualization-tooling.md","legacyId":"apss.feedback.visualization-tooling"}

---

[repository-import:stream-record:apss.feedback.visualization-tooling@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/framework-feedback/archived/2026-07-09-visualization-tooling.md]
