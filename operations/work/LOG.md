# Work log

Durable record of material execution, decisions, deviations, failures, and
successful resolutions. Detailed file history remains in git.

## 2026-07-09 — stewardship bootstrap started

- The maintainer approved separating produced artifacts from the operations
  that produce them.
- Moved the normative framework package under `artifacts/framework/`.
- Moved the CNC part production implementation under `artifacts/examples/` and
  classified examples as supporting, non-normative artifacts.
- Moved deferred foundations research under `operations/work/backlog/`.
- Declared the root APSS Framework Stewardship System.
- Added explicit backlog intake and grooming processes.

Validation completed after the move:

- both `SYSTEM.md` declarations satisfy the required structure and constraints
  of `artifacts/framework/system.schema.json`;
- every declared local process, plan, log, knowledge, stream-consumer, and
  artifact path resolves; and
- every local Markdown link resolves.

Outcome validation is still pending. The stewardship system therefore remains
`proposed` until a later idea completes the full operating and learning cycle.

## 2026-07-09 — framework feedback stream delivered

- **Status:** pushed to `origin/main`.
- **Claim:** Codex operator claimed the maintainer-requested change to define a
  direct framework-feedback stream, its intake and grooming processes, and to
  exercise them with the reported visualization-tooling gap.
- **Acceptance:** feedback remains distinct from backlog work; reports have a
  durable capture format and explicit dispositions; actionable reports can
  create bidirectionally linked work; the first report is captured and groomed;
  declarations and repository links remain valid.
- The maintainer distinguished direct feedback about APSS from backlog work and
  requested a durable reporting and grooming path.
- Added a framework-feedback stream that preserves the reported experience,
  provenance, context, desired outcome, suggested response, and evidence.
- Added feedback-specific grooming with explicit dispositions and a rule that
  actionable feedback creates or links separate backlog work.
- Captured and groomed the first report: APSS specifies visual projections but
  provides no tool that generates useful visual HTML from system declarations.
- Dispositioned the report as actionable and captured the linked task
  `apss.visual-html-generator`; planning priority and implementation scope remain
  undecided.
- Validation parsed the stewardship declaration and new report/work
  frontmatter, checked the new stream against the schema's required stream
  shape, confirmed all local Markdown links resolve after the concurrent
  repository-layout change, and found no whitespace errors with
  `git diff --check`.
- Manual consistency review found no change to normative APSS semantics: the new
  mechanism implements stewardship evidence handling, while the visualization
  generator remains a supporting-tool candidate. Outcome validation remains
  pending until the process receives another report or the linked tool is
  tested with a consumer.
- On 2026-07-10, the maintainer reviewed and approved the complete coherent
  working tree for commit and push to `origin/main`.
- Committed the approved work as `577cbfa` and pushed it to `origin/main`.

## 2026-07-09 — minimal AI agent task process awaiting review

- Claimed a bounded task to define how AI agents perform repository work.
- Added a five-step process: claim, do, record, obtain human review, then commit
  and push.
- Connected the process to the framework loop and declared that AI agents need
  maintainer approval before committing or pushing.
- Confirmed both system declarations parse as YAML, all local Markdown links
  resolve, the declared AI process path exists, and the JSON Schema parses.
- The maintainer reviewed and approved the complete coherent working tree for
  commit and push to `origin/main`.
- Committed the approved work as `45d18a5` and pushed it to `origin/main`.
