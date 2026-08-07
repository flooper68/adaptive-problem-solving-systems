---
id: apss.insight.processes-are-compiled-knowledge
type: insight
status: groomed
captured: 2026-08-06
source: APS framework maintainer
source_records:
  - ../../working-sessions/2026-08-06-grooming-consolidation.md
related_insights:
  - apss.insight.start-simple-add-only-when-needed
related_work:
  - ../../../tasks/compile-start-simple-principle.md
compiled_into: []
---

# Processes are compiled knowledge — replace them, never archive them

## Insight

### Claim

A system's processes are compiled knowledge, not records: they change over
time, only the current version is operative, and superseded versions should
be deleted rather than archived because session records and version-control
history already reconstruct them.

### Scope

Stated about Framework Operations' process files when the operator proposed
archiving four superseded grooming processes, and phrased generally enough to
apply to any APS instantiation that keeps its processes in version control.
It distinguishes compiled artifacts (processes, framework knowledge — current
version wins, history reconstructs) from records (sessions, problems,
insights, feedback — preserved as written, archived when closed). The claim
presupposes durable history; a system without version control would need
another recovery path before applying it.

### Reasoning

The maintainer's inference: archiving a superseded process creates a parallel
copy whose only job is provenance, but provenance already exists — the
sessions that changed the process record why, and git records what. A dead
copy in an `archive/` folder adds a directory concept, invites links to
non-operative procedure, and duplicates what history holds for free.

## Evidence

### Supporting

- Applied immediately: the four grooming processes and three intake processes
  were deleted, not archived; historical records keep their original links as
  citations of their time, and nothing broke operationally.
- The repository already treats records differently — closed problems and
  tasks move to `archive/` folders — so the distinction is observable in
  practice, not just asserted.

### Contradictory or limiting

- Links in retained records to deleted process files no longer resolve in a
  file browser; recovery requires git. Accepted deliberately, but it is a
  real cost for a reader without history access.
- None yet from observed use of the deleted-process recovery path; no one has
  needed to reconstruct a superseded process so far.

## Possible implications

- Candidate for compilation into framework guidance alongside
  [[start-simple-add-only-when-needed]]: the two together say "declare the
  simplest current version; let history hold the rest."
- Suggests the framework's record-vs-compiled-artifact distinction could be
  made explicit where it teaches system definition.

## Open questions

- Does the rule hold for compiled *framework* knowledge consumed by others,
  where superseded versions may need citable releases rather than only git
  history?

## Intake and clarification record

### 2026-08-06 — captured

Source wording: "I don't think we should archive processes, these can be
reconstructed from sessions/history and they change anyway over time - they
are 'compiled' knowledge." The maintainer approved capturing this as an
insight explicitly when asked during the pre-application review. No further
grill was run: the claim, reasoning, and an immediate application were all
present in the source's own words; the record-vs-compiled distinction in
Scope is operator inference from the repository's observed conventions.

## Grooming record

### 2026-08-07 — act: assessed supported; joined to the compilation task

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Assessment:** **supported within its stated scope.** The immediate
  application succeeded — seven superseded process files were deleted, not
  archived, and nothing broke operationally — and the repository observably
  maintains the records-versus-compiled-artifacts distinction the scope
  describes. The open question (whether compiled *framework* knowledge
  consumed by others needs citable releases rather than git history alone)
  remains unresolved and rides into the compilation task rather than being
  answered here.
- **Disposition:** **act** — linked into
  [`apss.compile-start-simple-principle`](../../../tasks/compile-start-simple-principle.md)
  so one brainstorming session compiles both principles together
  ("declare the simplest current version; let history hold the rest").
