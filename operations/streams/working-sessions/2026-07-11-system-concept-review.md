---
id: apss.session.system-concept-review
type: working-session
status: active
recorded: 2026-07-11
participants: [APS framework maintainer, Codex operator]
source: Maintainer-agent discussion in the current Codex task
related_problems: [P1]
related_tasks: [apss.review-system-concept]
---

# Review the adaptive problem-solving system concept

## Frame

Give the system concept the smallest clear meaning, boundary, ownership, and
lifecycle needed by the complete adaptive loop. Apply P1's concept review test
without separately deciding downstream system-problem, boundary, authority,
subsystem, or relationship concepts.

A useful stopping point is one maintainer-reviewed disposition—retain,
simplify, merge, demote, defer, or remove—with accepted changes propagated
through affected normative and supporting surfaces. Until that point, changes
remain uncommitted for iterative review.

## Evidence and current orientation

- P1 requires the initial framework to keep only what is needed to run one
  complete loop now and makes maintainer understanding and use the initial
  outcome signal.
- The framework currently defines an adaptive problem-solving system through
  an eleven-item ownership list covering identity, direction, operation,
  artifact and outcome, evidence, learning, and adaptation.
- The current subsystem rule says a subsystem is a complete system whose
  lifecycle is owned by exactly one parent; an entity without its own complete
  adaptive loop should instead be modeled as a process or capability.
- The system declaration schema gives a system a stable ID and lifecycle
  status, so the concept currently owns durable identity and state.

## Current stopping point

The maintainer identified the main idea as a problem statement plus an
iterative loop for solving it. A small set of general problem-solving concepts
supports that loop: strategy, work planning, input streams, information
grooming, learning and knowledge compilation, and verification of the problem
solution.

Current interpretation: the system concept should lead with this simple core
rather than an eleven-item ownership checklist. The supporting concepts still
need clear responsibilities, but they need not all appear as coequal identity
criteria in the concise definition.

The maintainer clarified that APS is the general method, while a system is one
instantiation of that method. APS defines hierarchical systems as a means of
problem decomposition. This resolves the prior ambiguity between the method
and its instances: the instance owns the problem and repeated loop.

The conclusion has been compiled as uncommitted changes to the framework
definition, vocabulary, and changelog. Next: clarify the minimum responsibility
of a child system in the hierarchy, particularly whether every child must own
its own complete adaptive loop or may implement only part of its parent's loop.

The maintainer decided that every child owns its loop. Its parent may supply
feedback, verification, or insights, but those are contributions to the
child's loop rather than ownership of it. The framework proposal now
distinguishes loop ownership from external participation.

Next: establish the system instance's lifecycle boundary—particularly whether
solving its stated problem ends the system or may lead to a revised problem and
another lifecycle stage.

The maintainer decided that this consequence belongs to the system definition
and its process. APS should not prescribe that verified solution retires the
system or causes another universal transition. The framework prose now records
that boundary; the declaration schema remains unchanged pending a decision on
whether lifecycle declaration itself is universally required.

Next: determine whether APS requires every system to declare how lifecycle
decisions are made while leaving its states and transitions system-specific, or
whether lifecycle need not be a general declaration responsibility.

The maintainer clarified the more general rule: a system has the problem,
verification, problem decomposition, and other concepts needed for its loop,
but all processes are customizable. Current interpretation: APS defines the
responsibilities and concepts that make the loop complete; the system defines
the processes that implement them. APS therefore need not prescribe a
universal lifecycle process.

Next: confirm this responsibilities-versus-processes boundary, then test the
system-concept proposal for consistency and capture process-specific schema
questions for their later concept reviews rather than expanding this task.

The maintainer identified grooming as a general concept required in some form
by every problem-solving process: information processing plus decision making
that checks verification evidence. Different problems and input streams may
need different groomings. Current interpretation: APS may require grooming as
a loop responsibility without prescribing one named grooming process or
ceremony. The framework proposal now states the general responsibility; the
current framework's specifically required work sessions remain a downstream
review question.

Next: determine whether producing an artifact is essential to every system or
whether inspectable work and direct verification of problem change can close a
system loop without a separately named artifact.

The maintainer decided that artifacts are contextual to the problem being
solved. Current interpretation: attempting a solution and verifying its effect
belong to the irreducible loop, while producing a separately named artifact
does not define system identity. The proposal now states this boundary.

The current declaration schema still requires an `artifact` block. Whether
that requirement should become contextual belongs to the later artifact and
schema reviews; it is captured here rather than expanded into this task.

Next: clarify whether verification is universally verification of change in
the system problem, with artifact checks added only when contextual artifacts
exist.

The maintainer characterized verification as the value function for the
optimization process. Current interpretation: verification evaluates each
solution attempt against the system problem and supplies the signal that guides
the next iteration. The function may be qualitative or quantitative and need
not reduce the problem to a numeric score. Artifact checks are contextual
inputs to that evaluation when the solution produces an artifact.

Next: clarify whether owning the loop requires adaptation authority to reside
inside the child system, or whether a parent or other external approver may
authorize changes while the child remains responsible for the loop.

The maintainer decided that performance and approval authority are
implementation details defined by the system's processes. Current
interpretation: ownership means accountability for closing the loop, not that
every actor or decision authority must reside inside the system boundary. The
framework proposal now states this distinction.

## Proposed disposition

**Simplify.** Define APS as the general method and a system as one
instantiation organized around a problem statement and an iterative optimizing
loop. The loop uses customizable processes for strategy, planning, information
inputs and grooming, solution attempts, verification, knowledge compilation,
and adaptation. Verification is its value function. Hierarchical child systems
own loops for decomposed problems even when parents contribute evidence or
approval. Artifacts and lifecycle behavior remain contextual rather than
system-identity criteria.

Direct system-identity statements have been propagated through the framework
definition and vocabulary. The review also exposed downstream requirements
that must be reconsidered in their existing concept tasks: the schema's
mandatory artifact block and fixed fields; two specifically required work
sessions; mandatory artifact validation; and fixed role declarations. Changing
those contracts here would expand this bounded task.

The maintainer renamed the general method from Adaptive Problem-Solving
Systems (APSS) to **Adaptive Problem Solving (APS)** because it is simpler to
read and say and distinguishes the method from its system instances. The rename
is propagated through current human-facing framework, operations, examples,
tasks, and contributor guidance. The current declaration contract now uses
`aps_version` and `urn:aps:system:0.1`. Stable historical record and task IDs
retain their existing `apss.*` namespace so provenance links do not change.

## Current stopping point

The proposed simplified and renamed definition is compiled as uncommitted
framework changes. Manual consistency review found the downstream contract
questions recorded above; no system-concept question remains open. Next:
validate the renamed declarations and references, present the proposal for
maintainer review, and incorporate any corrections.

Rename validation found no stale human-facing `APSS` in current framework,
operations, examples, tasks, or contributor guidance except the changelog
sentence that explains the rename. The schema JSON and current declaration YAML
parse successfully, all live declarations use `aps_version`, current relative
Markdown links resolve, and `git diff --check` passes. A JSON Schema validation
library is not installed locally, so complete schema evaluation remains for
final artifact validation after maintainer review.

The maintainer then simplified declaration identity: remove `aps_version`,
system `id`, `status`, and `parent`; the system name is sufficient. When a
problem is decomposed to another system, the originating problem definition,
strategy, or process owns the link. The schema, template, live declarations,
framework hierarchy guidance, visualization contract, and CNC example now use
this model. Existing `apss.*` task and evidence IDs are records rather than
system-declaration fields and remain stable.

Next: validate the simplified schema and live declarations and review the full
uncommitted proposal.

Validation confirms that both live declarations satisfy every remaining
top-level and nested required field, contain none of the four removed fields,
and retain the required work-session and stream structures. Schema JSON and
declaration YAML parse, current relative Markdown links resolve, stale
parent-tree language is absent from current normative and example surfaces,
and `git diff --check` passes.

Current stopping point: the simplified system concept, APS rename, and reduced
declaration identity contract are ready for maintainer review as one
uncommitted proposal.

## Constraint-concept discussion

The maintainer opened a related discussion about whether constraints make
sense as an APS concept. A retained but ungroomed insight already claims that
the concept adds no operational value and should be removed framework-wide.
Current inspection supports the narrower observation that representation is
inconsistent: Framework Operations declares a top-level `constraints` field;
the template folds a constraint into `inputs`; the schema has no constraint
property; and framework prose also uses the word for direction, process
context, and health conditions.

Current operator interpretation: problem solving must account for real limits,
but APS may not need a first-class constraint concept. A hard limit can instead
be part of the problem statement, verification/value function, strategy,
process, authority, or contextual input according to what role it actually
plays. The remaining decision is whether to remove only the distinct field and
concept while allowing ordinary contextual use of the word, or eliminate the
term throughout APS guidance.

The maintainer directed complete removal from current APS surfaces. The
retained insight was groomed as supported: representation was inconsistent,
and no distinct operation or information was lost when each concrete limit was
rewritten by its actual role. The top-level Framework Operations field was
removed; all current normative, operational, process, problem, task, and
example occurrences were removed or replaced with role-specific language.
Historical evidence retains the original discussion and wording.

Next: validate the full proposal and present the updated diff for maintainer
review.

Validation confirms zero occurrences of the removed term across current
framework, examples, system declaration, strategy, processes, problems, and
tasks. Both live declarations satisfy the reduced schema and contain none of
the removed fields; JSON, YAML, current relative links, and diff whitespace
checks pass.

## Role-concept discussion

The maintainer opened a review of the system-level `roles` concept. The current
schema requires `owner`, `operators`, `consumers`, `validators`, and
`adaptation_approvers` for every system, while the framework also says each
system's processes define who performs and authorizes each step.

Current operator interpretation: the universal role block duplicates more
specific sources. Lifecycle accountability belongs to the relevant lifecycle
process; operators vary by process; validators belong to verification;
adaptation approvers belong to adaptation; and affected people or artifact
consumers belong to the problem context or contextual artifact. APS still needs
processes to make participation and decision authority explicit, but may not
need five system-wide role lists.

The load-bearing question is whether any actor must remain accountable for the
system as a whole independently of all its processes. If not, the `roles`
field can be removed and each process can state its required participants and
authority.

The maintainer decided to remove the system-wide field: participant
responsibilities are not assigned by the framework and belong in `process.md`
definitions. The schema, template, live declarations, framework explanation,
system-creation guidance, and assessment questions now use process-specific
participation and responsibility. Process-specific role language remains valid
inside process definitions.

Next: validate the reduced declaration contract and current references.

Validation confirms that neither live declaration contains `roles`, both
satisfy every remaining schema requirement, and no system-level role checklist
remains in the current schema, template, examples, or framework guidance. JSON,
YAML, current relative links, and diff whitespace checks pass.

## Remaining SYSTEM.md field audit

On 2026-07-12 the maintainer requested a field-by-field pruning review of the
current Framework Operations declaration. The audit distinguishes durable
system direction from process indexing and process implementation detail.

Strong pruning candidates:

- `purpose` restates the problem, vision, name, and prose purpose.
- `inputs` duplicates declared streams and process-specific intake.
- `artifact` is contextual by the already accepted system-concept decision and
  should not be universally required.
- `planning.process`, `execution.process`, and `execution.invocation` describe
  process implementation; problem and task locations may also be conventions
  owned by those processes rather than system identity.
- `work_sessions` prescribes two named processes and duplicates their own
  definitions.
- `uncertainty` prescribes three implementation modes that can be selected by
  the relevant process.
- `authority` duplicates the decision authority now assigned to each process.
- `health` is a contextual verification or operating concern, not a universal
  declaration concept.
- `relations` is an empty universal structure in both live declarations;
  problem decomposition already links systems from problem definitions,
  strategies, or processes, and other relations can be contextual.

Concepts worth retaining but simplifying before deciding their representation:

- `streams` represents the input-stream concept the maintainer considers part
  of the general method, but its required `id`, `purpose`, `source`, `access`,
  `consumed_by`, and `grill` fields may over-specify implementation.
- verification is a core value function, but the fixed `artifact`/`outcome`
  split conflicts with contextual artifacts and may be better represented by a
  link to the system's verification process.
- learning and knowledge compilation are core loop responsibilities, but four
  fixed paths may be replaceable by one process link.

Likely durable core: system `name`, `problem`, and strategy link. `vision`
remains a separate concept-review question because it may add durable direction
or merely restate the desired inverse of the problem. A minimal declaration
could then link the few system-level processes or sources needed to find the
loop without encoding their implementation.

### Work-session types

The maintainer asked specifically whether work-session types should remain.
Current interpretation: a work session is a bounded invocation of a process,
not a separate universal system concept. `brainstorming` and
`problem-grooming` are useful Framework Operations processes, but requiring
those two names in every APS system prescribes an implementation and conflicts
with contextual grooming. Continuous or automated processes may not have a
natural session boundary at all.

Recommended disposition: remove `work_sessions` and its required types from the
system schema. A process defines its own invocation, participants, decisions,
outputs, stopping or observation boundary, and retention. When history is
material, a system may keep a record of that process invocation in an
appropriate stream; APS need not call every invocation a work session.

The maintainer challenged complete removal because a system still needs an
authoritative place to define which working-session types it offers. Revised
interpretation: retain `work_sessions` in `SYSTEM.md` as the system-specific
catalog, with each entry naming and describing a type and linking its defining
`process.md`. Remove only the framework mandate that every system implement the
specific `brainstorming` and `problem-grooming` types. Those remain Framework
Operations choices. Continuous processes that are not working-session types do
not need catalog entries.

The remaining design question is whether every system must declare at least one
working-session type or whether `work_sessions` may be empty when the system has
no bounded interactive sessions.

### 2026-07-12 — minimal declaration compiled

The maintainer authorized pruning the full declaration based on the audit and
work-session clarification. The normative schema now requires only `name`,
`problem`, `vision`, `strategy`, `process`, `work_sessions`, `verification`,
and `streams`. The work-session catalog remains required as the authoritative
answer to which bounded session types a system offers, but may be empty; APS no
longer mandates particular types.

Framework Operations and the CNC example now use the minimal shape. Their main
processes own planning, execution, learning, participation, authority,
uncertainty handling, contextual artifacts, operating conditions, problem
decomposition, and other relationships. The framework schema guide, template,
definition, visualization contract, root orientation, and artifact-validation
process have been aligned with that source-of-truth boundary.

Next: validate schema conformance, all referenced paths, terminology, and
cross-surface consistency, then present the uncommitted proposal for review.

Validation passed for both live declarations: all eight required fields have
the expected types; working-session and stream IDs are valid and unique; every
declared strategy, loop, verification, work-session, and stream-consumer path
resolves; current Markdown links resolve; schema JSON parses; no stale universal
requirement for the removed blocks was found; and `git diff --check` passes.

Current stopping point: the complete session proposal is uncommitted and
awaiting maintainer review.

## Problem, vision, and verification overlap

The maintainer reopened the review to ask whether all three minimal fields are
worth retaining. They currently answer different questions: the problem names
the condition to change; vision describes the durable desired future; and
verification evaluates whether an attempt improved the condition.

Current operator interpretation: verification remains operationally distinct
as the optimization loop's value function. The strongest overlap is between
problem and vision. A sufficiently directional problem statement can imply its
desired inverse, while a useful longer-horizon vision could instead live in the
strategy when the system needs one. The load-bearing decision is whether APS
needs every system to declare an aspirational future independently of its
problem.

The maintainer decided it does not. The aspirational-future field and concept
were removed from the schema, template, both live declarations, framework
definition, normative vocabulary, root guidance, and current concept
dependencies. Goal is now defined relative to reducing the system problem.
Longer-horizon direction may be stated in strategy when it adds value. The
separate ready review task was superseded and archived by this decision.

Next: validate the final seven-field declaration and scan all current
framework surfaces for stale semantics before returning to review.

Validation passed: both live systems satisfy the seven-field contract; all
field types and local IDs are valid and unique; every declared strategy, loop,
verification, work-session, and stream-consumer path resolves; no current
normative, example, system, strategy, process, or problem surface retains the
removed concept; current Markdown links resolve; schema JSON parses; and
`git diff --check` passes.

Current stopping point: the final session proposal is uncommitted and awaiting
maintainer review.

## Root README simplification

The maintainer observed that the root README duplicated operational navigation
by linking individual processes. It was reduced to the repository's purpose,
the high-level responsibilities of `framework/`, `operations/`, and
`examples/`, and the boundary between normative, operational, and
example-specific choices. Process discovery remains inside the Operations
system. All retained root README links resolve and `git diff --check` passes.

## Example-directory pruning proposal

The maintainer proposed removing `examples/` until the normative framework has
been polished, treating Framework Operations as the first concrete APS
application. This follows P1's rule to keep only what is needed for the first
complete loop and add supporting complexity after observed need.

Current operator assessment supports removal: the CNC example was created
before the current simplification, has no real consumer-outcome evidence, and
creates repeated synchronization work as declaration concepts change. Keeping
it may make provisional cross-domain choices appear more validated than they
are. The cost is losing an immediate physical-domain consistency check, but Git
retains the example and a later task can recreate examples from a more stable
framework and actual validation needs.

No files have been removed pending explicit maintainer confirmation.

The maintainer confirmed removal. The entire provisional `examples/` tree was
deleted, Framework Operations is now identified as the first concrete APS
application, and the root README, Operations declaration and processes,
framework definition and schema guide, validation and release processes, P1,
and current backlog evidence were aligned. The future software/research example
task is deferred until the framework is polished and the first complete
Operations loop produces validated learning. Historical records and Git retain
the removed example's provenance.

Validation found no current links or live dependencies on the deleted tree;
all remaining current Markdown links resolve, Framework Operations satisfies
the seven-field schema, schema JSON parses, and `git diff --check` passes.

## Problem and verification ordering

The maintainer requested that verification appear immediately below the
problem. Because `STRATEGY.md` intentionally does not duplicate the system
problem, this was applied to the `SYSTEM.md` declaration order. The schema,
template, Framework Operations declaration, schema guide, changelog field list,
and system-creation sequence now order `problem` followed by `verification`,
then `strategy` and `process`.

Validation confirms the schema and Framework Operations use the exact order
`name` → `problem` → `verification` → `strategy` → `process` →
`work_sessions` → `streams`; current links resolve and `git diff --check`
passes.

## Verification process consolidation

The maintainer required `verification` to contain only a process link and asked
to rename the implementation to `verification.md`. Framework Operations now
declares `verification: processes/verification.md`. The former artifact- and
outcome-validation processes were consolidated into that single value-function
process, which handles immediate correctness evidence, problem-signal
evaluation, and delayed improvement observations.

The framework template, schema guide, creation guidance, operating loop,
strategy, adaptation, release, knowledge compilation, P1, and current research
and future-application tasks were aligned. The two pending validation-concept
review tasks were superseded and archived.

Validation confirms that `verification` is exactly the direct process path,
all declared Framework Operations paths resolve, both former files are absent,
no current Markdown source references the old process names, current links
resolve, schema JSON parses, and `git diff --check` passes.

## Declaration contract consolidation

The maintainer removed the machine-readable `system.schema.json` and merged the
separate `SYSTEM.template.md` into `SCHEMA.md`. `SCHEMA.md` is now the single
human-readable declaration contract and contains the authoring template,
field semantics, work-session and stream shape, and review checks. Framework
guidance, visualization, verification, root orientation, current task evidence,
and the merged schema-removal task were updated to use that single source.

Validation confirms both deleted files are absent, the seven-field template in
`SCHEMA.md` matches Framework Operations, all declared process paths resolve,
no current link targets either removed file, current Markdown links resolve,
and `git diff --check` passes. Historical evidence retains the former filenames
where they describe the state observed at the time.

## Task handoff cleanup

The final scope audit found that the task's current-state section had become a
duplicate chronological log with stale intermediate claims. That history is
already retained in this session record. The task file was condensed to the
final simplify disposition, seven-field contract, removed or superseded
machinery, validation result, downstream concept reviews, and acceptance next
step.

## Acceptance and delivery

On 2026-07-12 the maintainer accepted the reviewed result and explicitly asked
to finish the session. Final verification passed for the declaration contract
and order, declared process paths, active task-to-problem references, current
Markdown links, removed-file and terminology scans, and diff whitespace.

Delivery is in progress. After the reviewed commit is pushed to `origin/main`,
record its reference, retain this session, and close and archive the task.

## Main process filename

The maintainer renamed the Framework Operations loop implementation from
`processes/framework-loop.md` to the canonical `processes/process.md`. The
system declaration, three stream consumers, task-grooming reference, and
changelog were updated. No current reference uses the old filename; all
declared paths and Markdown links resolve, and `git diff --check` passes.
