---
entity:
  identity:
    type: key
    value: APS-R-8
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:40:44.499Z
  dispositionNote: "Legacy disposition: groomed"
  groomed: true
  key: APS-R-8
  keyNumber: 8
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-16T19:41:15.987Z
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
- The former `operations/work/backlog/README.md` contained an `Items` section
  linking every retained backlog item; the task collection has since replaced
  that index.
- [`operations/streams/framework-feedback/README.md`](../README.md) currently
  contains a `Reports` section, suggesting the same scaling concern may apply
  here; the broader reach has not yet been assessed.

## Grooming record

### 2026-08-07 — act: remove the last residual index

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Evidence consulted:** the three stream READMEs and the archived-folders
  convention.
- **Assessment:** the reported concern is already largely adopted — the
  insights and working-sessions READMEs explicitly keep no exhaustive index
  and direct discovery by frontmatter and filenames, and the `archived/`
  convention bounds each stream root to records still awaiting grooming. The
  one surviving instance was the feedback stream README's own one-item
  `Reports` section.
- **Disposition:** **act** — remove that residual `Reports` section, aligning
  the feedback README with the insights README's no-index statement. Executed
  with this entry.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/framework-feedback/archived/2026-07-10-unbounded-stream-indexes.md","legacyId":"apss.feedback.unbounded-stream-indexes"}

---

[repository-import:stream-record:apss.feedback.unbounded-stream-indexes@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/framework-feedback/archived/2026-07-10-unbounded-stream-indexes.md]
