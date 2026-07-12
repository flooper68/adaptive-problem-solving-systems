---
id: apss.feedback.problem-creation-grooming-and-storage
type: framework-feedback
status: grooming
received: 2026-07-12
reporter: APS framework maintainer
source: Maintainer-agent discussion in the current Codex task
related_feedback:
  - apss.feedback.problem-hierarchy-and-goal-ambiguity
related_work:
  - apss.review-open-problem
  - apss.review-problem-grooming
  - apss.review-problem-file
  - apss.review-task
  - apss.review-task-collection
---

# Problem creation, grooming, task handling, and storage need clearer boundaries

## Report

### Context

The maintainer was reviewing the proposed goal-free problem hierarchy and its
minimal open/closed lifecycle. Existing sources include the normative
[problem lifecycle](../../../framework/README.md#problem-lifecycle-and-verification),
the [open-problem definition](../../../framework/VOCABULARY.md#open-problem),
the Operations [problem-grooming process](../../processes/problem-grooming.md),
and the current [problem-file convention](../../problems/p1-finish-mvp-and-run-loop.md).

### Observed problem or outcome

- It is unclear how and why a possible gap becomes an actual problem.
- It is unclear whether a problem should retain an explicit change history.
- Problem grooming may need to be a heartbeat process that reviews current
  problems, prunes them, and potentially creates new ones.
- It is unclear whether the same grooming should handle tasks within problems;
  task grooming may belong to a different meeting or process.
- APS should not prescribe a problem folder or file structure. A system may use
  Jira epics, GitHub milestones, a Notion board, repository files, or another
  system of record, and the practical grooming implementation belongs to that
  system's process.

### Desired outcome

Define only the domain-independent responsibilities for problem creation,
history, review, pruning, and task relationship. Delegate cadence, meetings,
storage, fields, and tools to each system's process.

### Suggested response

Consider problem grooming as a recurring heartbeat over the current problem
set, with authority to create, revise, split, merge, retain, close, and reopen
problems. Keep task grooming separate if problem framing and executable-work
selection require different participants, cadence, or decisions. Remove
normative problem-folder and problem-file requirements.

### Evidence

Direct maintainer usability and design feedback. The suggested heartbeat and
process split are proposals, not independently validated requirements.

## Grooming record

### 2026-07-12 — grooming started

- **Participants:** APS framework maintainer and Codex operator.
- **Evidence consulted:** this report's linked framework and Operations
  sources, the active system-problem review, and the five related concept tasks.
- **Scope:** normative problem responsibilities versus system-specific process
  and storage implementation.
- **Impact:** the current file/folder language may falsely imply that APS
  requires the Framework Operations implementation and may obscure who creates
  problems and how task decisions relate to problem review.
- **Current facts:** feedback is evidence but does not automatically become a
  problem; Operations currently has separate problem-grooming and task-grooming
  processes; the normative framework currently prescribes problem files and an
  archive folder.
- **Unresolved questions:** creation authority and threshold, minimum retained
  change history, whether heartbeat is normative or implementation-specific,
  the boundary between problem and task grooming, and the storage-neutral
  minimum problem record.
- **Disposition:** grooming through existing linked concept-review work; do not
  create duplicate tasks.
- **Follow-up:** after the current hierarchy questions are resolved, ask one
  load-bearing question at a time beginning with problem creation.

### 2026-07-12 — problem-creation authority clarified

- **Maintainer decision:** any stream or process records its own observations,
  issues, results, and insights. Its relevant grooming may propose a new
  higher-level problem; problem grooming then acts on that proposal.
- **Compiled boundary:** source-specific grooming interprets and proposes but
  does not open a problem. Problem grooming decides whether to open, merge with
  or revise an existing problem, defer, or reject the proposal. A task
  candidate may be captured independently, but selection waits until it
  addresses an open problem.
- **Rationale:** broad discovery preserves evidence from every operating source
  while one authority-governed responsibility keeps the active problem set
  coherent and avoids turning every report or insight into a problem.
- **Remaining questions:** minimum problem change history, heartbeat cadence,
  separation of problem and task grooming, and storage-neutral representation.
- **Disposition:** remains `grooming`; continue one load-bearing question at a
  time.

### 2026-07-12 — material decision history required

- **Maintainer decision:** keeping a log of problem decisions is crucial.
- **Compiled boundary:** each problem's chosen system of record retains why it
  was opened, materially reframed, changed strategy or signal, closed, or
  reopened, together with supporting evidence and authority. It does not
  duplicate routine task activity, detailed discussions, or evidence retained
  in native sources.
- **Implementation boundary:** APS requires recoverable material history but
  does not prescribe a changelog file, folder, product, or field layout.
- **Remaining questions:** heartbeat cadence, separation of problem and task
  grooming, and storage-neutral representation.

### 2026-07-12 — grooming cadence delegated to the system

- **Maintainer decision:** problem-grooming cadence is an implementation detail;
  event-driven operation may fit some systems, while a scheduled approach such
  as cron may fit others.
- **Compiled boundary:** APS requires the problem-set re-evaluation
  responsibility but does not prescribe a heartbeat mechanism or cadence.
  Event-driven, scheduled, continuous, and mixed implementations are valid.
- **Framework Operations choice:** its current problem-grooming process uses
  explicit event triggers such as new proposals, material evidence, work
  selection, and maintainer request.
- **Remaining questions:** separation of problem and task grooming and
  storage-neutral representation.

### 2026-07-12 — problem and task grooming separated

- **Maintainer decision:** separate problem grooming from task grooming because
  the hierarchical problem structure is central to APS.
- **Compiled boundary:** problem grooming maintains proposed, open, and closed
  problems, their strategies, signals, relevance, and priority. Task grooming
  shapes bounded executable responses and their readiness for selection. One
  responsibility cannot silently substitute for the other.
- **Implementation boundary:** a system may still combine both responsibilities
  in one meeting, process, tool, or cadence when their distinct decisions and
  authority remain inspectable.
- **Remaining question:** storage-neutral problem representation.

### 2026-07-12 — normative problem storage removed

- **Maintainer decision:** APS should contain no problem-storage details, only
  the general concepts.
- **Compiled boundary:** APS requires recoverable current problem meaning,
  evidence, desired change, signal, strategy, lifecycle, and material decision
  history but does not prescribe identifiers, fields, files, folders, archive
  paths, views, or products.
- **Examples, not requirements:** systems may use Jira epics, GitHub milestones,
  Notion items, repository files, databases, or other systems of record.
- **Framework Operations choice:** it continues using `operations/problems/`
  and `problems/archive/` through its own processes as local implementation.
- **Disposition:** `actionable`; the reported semantic and implementation
  boundaries are compiled in uncommitted changes. Mark addressed only after
  delivery and subsequent use show the explanation is clear.
