---
id: apss.feedback.visualization-tooling
type: framework-feedback
status: actionable
received: 2026-07-09
reporter: APSS framework maintainer
source: Maintainer report in Codex task
related_feedback: []
related_work:
  - apss.visual-html-generator
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
- [`framework/VISUALIZATION.md`](../../../framework/VISUALIZATION.md)
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
  [`operations/work/backlog/visual-html-generator.md`](../../work/backlog/visual-html-generator.md).
- **Follow-up:** report acknowledged through this retained record. Validate a
  future implementation using at least the stewardship system and one example,
  then obtain consumer feedback on clarity and usefulness before marking this
  report `addressed`.
