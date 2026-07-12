---
id: apss.feedback.problem-hierarchy-and-goal-ambiguity
type: framework-feedback
status: actionable
received: 2026-07-12
reporter: APS framework maintainer
source: Maintainer-agent discussion in the current Codex task
related_feedback: []
related_work:
  - apss.review-system-problem
  - apss.review-goal
  - apss.review-open-problem
  - apss.review-problem-strategy
  - apss.review-system-strategy
---

# Problem hierarchy and goal relationships are unclear

## Report

### Context

The maintainer was orienting to the current system-problem definition before
executing its concept review. The sources consulted were the normative
[definition](../../../framework/VOCABULARY.md#system-problem), the framework's
[relationship explanation](../../../framework/README.md#problem-hierarchy-and-strategy),
the [declaration contract](../../../framework/SCHEMA.md), and the concrete
[Framework Operations problem](../../SYSTEM.md).

### Observed problem or outcome

- The framework provides no example showing the shape of a useful problem
  statement.
- It lacks a clear general explanation of problem and strategy and does not
  make the problem hierarchy understandable: one main system problem is
  decomposed during problem solving into smaller problems, each with its own
  strategy.
- The relationship among problem, goal, and strategy is unclear; goal appears
  redundant.

The result is that the maintainer cannot yet form a coherent top-down mental
model from the current definitions.

### Desired outcome

Explain the model with at least one concrete problem statement, a general
problem–strategy relationship, and a clear account of decomposition from the
system problem to smaller problems. Retain `goal` only if it has a distinct,
demonstrable role.

### Suggested response

Test a smaller model in which the system problem is the root problem, the loop
decomposes it into smaller problems, every problem has a strategy, and tasks
iterate on problem solutions. Remove or demote goal if examples cannot show
information it contributes beyond the problem's desired change and strategy.

### Evidence

Direct maintainer usability report while attempting to understand and prepare
the system-problem concept review. The current
[Framework Operations declaration](../../SYSTEM.md) supplies a real system
problem but the normative explanation does not present it as a worked example
or trace its decomposition into [P1](../../problems/p1-finish-mvp-and-run-loop.md).

## Grooming record

### 2026-07-12 — grooming started

- **Participants:** APS framework maintainer and Codex operator.
- **Evidence consulted:** this report's linked normative definitions,
  declaration contract, Framework Operations statement, P1, the prior
  [goal-decomposition insight](../insights/2026-07-10-goals-decompose-into-open-problems.md),
  and the five linked concept-review tasks.
- **Clarified experience:** the existing pieces do not produce an understandable
  hierarchy or distinct roles for problem, goal, and strategy.
- **Scope:** normative semantics and explanation, with Framework Operations as
  the first worked example.
- **Reach and impact:** directly blocks the maintainer's P1 understanding
  signal and the system-problem review. Broader consumer reach is not yet
  observed.
- **Current hypothesis:** one root system problem → smaller problems with their
  own strategies → bounded tasks → evidence and learning may be simpler and
  clearer than the current goal-mediated model.
- **Unresolved question:** whether a separate goal contributes any necessary
  information or should be removed from the first APS model.
- **Disposition:** grooming; link to existing concept-review work rather than
  create duplicate tasks.
- **Follow-up:** ask one load-bearing question about testing a goal-free model.

### 2026-07-12 — actionable; goal removal authorized

- **Clarification:** the maintainer decided to remove goal completely rather
  than retain it provisionally.
- **Disposition:** actionable through the already selected
  [`apss.review-system-problem`](../../tasks/review-system-problem.md); the
  separate goal review is superseded rather than duplicated.
- **Compiled response:** define problem and strategy generally; make the system
  problem the root of an evolving hierarchy; give every smaller problem its
  own desired change, signal, and strategy; connect tasks and learning to that
  hierarchy; add Framework Operations and P1 as a worked example; and remove
  current goal semantics from normative and operational surfaces.
- **Confidence and reach:** the direct maintainer report is sufficient to
  justify a small reversible MVP simplification. Broader consumer effectiveness
  remains unverified until the revised explanation is reviewed and used.
- **Follow-up owed:** present the uncommitted compiled model for maintainer
  review. Mark this feedback addressed only after delivered changes improve a
  subsequent use.
