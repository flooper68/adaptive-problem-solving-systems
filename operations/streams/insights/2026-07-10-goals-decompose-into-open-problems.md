---
id: apss.insight.goals-decompose-into-open-problems
type: insight
status: captured
captured: 2026-07-10
source: APSS framework maintainer
source_records: []
related_insights:
  - apss.insight.evidence-deliberation-action-learning
related_work: []
compiled_into: []
---

# Goals evolve into open problems before becoming tasks

## Insight

### Claim

APSS is missing an explicit concept between a system's current goal and its
executable work: the **open problem**. A goal should be decomposed over time
into smaller open problems as input streams provide new evidence and learning
changes the system's understanding. Tasks, research, experiments, and other
work should be selected to resolve, reduce, test, or reframe those problems
rather than being treated as a static decomposition of the goal.

### Scope

This is a candidate framework-level planning concept within an adaptive
problem-solving system. It concerns the changing problem structure that
connects the system's durable problem and current goals to bounded executable
work. An open problem belongs to the system that is pursuing the goal; it is
not itself a child APSS merely because the goal was decomposed. It remains
unclear whether every open problem must be a durable record or whether every
work item must map to exactly one open problem.

### Reasoning

A goal describes a bounded result, but it rarely provides enough information
to determine all necessary work in advance. Evidence arriving through input
streams can reveal obstacles, unknowns, opportunities, and incorrect
assumptions. Learning from completed work can close one problem while exposing,
splitting, combining, or reframing others.

If planning moves directly from goals to tasks, that evolving interpretation
is implicit. The system can retain what it intends to do without retaining why
that work is currently relevant or how its view of the problem space changed.
Making open problems explicit would let planning adapt the decomposition while
keeping executable work bounded and traceable to the problem it is intended to
advance.

## Evidence

### Supporting

- The maintainer observed that the current framework misses an “opened” or
  open-problem concept and proposed that a main goal be progressively
  decomposed into smaller problems from input streams and learning, with tasks
  solving those problems.
- The framework already expects planning to consume the current problem,
  goals, evidence, constraints, and learning, but its guidance moves from that
  context to executable work without naming a durable intermediate problem
  model.
- The related evidence-deliberation-action-learning insight proposes a
  recurring flow from streams and interpretation into selected responses. Open
  problems may explain what that interpretation produces before responses are
  selected.

### Contradictory or limiting

- “Problem” already names the system-level condition APSS exists to change;
  using the same term for planning-level units could blur system boundaries.
- Some necessary work maintains capability, satisfies a constraint, or
  responds to routine operation without obviously solving one discrete open
  problem.
- No observed APSS application has yet compared planning with and without an
  explicit open-problem layer.
- A heavy problem-record lifecycle could add administrative cost without
  improving decisions for small or synchronous systems.

## Possible implications

- APSS may need a first-class open-problem model between direction and work,
  including provenance, current framing, relationship to goals, status, and
  links to evidence, learning, and attempted responses.
- Planning may be better described as maintaining an adaptive problem
  decomposition or problem portfolio, not merely selecting and ordering tasks.
- Work intake may need to ask which open problem a task, research inquiry, or
  experiment is intended to resolve, reduce, test, or reframe.
- Validation and learning may update both the goal or strategy and the current
  problem decomposition: problems can be resolved, invalidated, reframed,
  split, merged, or newly discovered.
- Open problems remain planning entities owned within a system rather than
  recursively creating a child APSS for every decomposition step.

## Open questions

- Is an open problem always a first-class durable record with an explicit
  lifecycle, or may it remain a transient part of a plan in simple systems?
- What distinguishes an open problem from the system's root problem, a goal,
  an issue, an unresolved question, and an executable work item?
- Can one work item address several open problems, and can several work items
  represent competing attempts to address one problem?
- Which evidence is sufficient to close a problem, and who has authority to
  close, reframe, split, or merge it?
- Can an open problem ever motivate a separately designed child system, while
  remaining distinct from that system and its independently declared problem?

## Intake and clarification record

### 2026-07-10 — captured

Captured from the APSS framework maintainer's observation that the current
system lacks an “opened” problem concept: the main goal needs to be decomposed
over time into smaller problems based on input streams and learning, and tasks
should solve those problems. The operator normalized “opened problem” to “open
problem” while preserving the proposed relationship among goals, evidence,
learning, problems, and tasks.

The first load-bearing clarification is whether open problems are intended as
planning entities within a system or as recursively nested adaptive systems.
That choice affects the concept's boundary, lifecycle, and relationship to
existing APSS system declarations.

### 2026-07-10 — first clarification

The maintainer answered that an open problem exists **within a system**. The
scope and implications were updated so goal decomposition does not recursively
create child APSS declarations. Whether an open problem must be durable, and
how it differs from existing issues and unresolved questions, remain open.

The next load-bearing clarification asks what kind of statement qualifies as an
open problem. Its answer will determine whether issues and questions are
specialized views of problems or remain separate inputs that may reveal them.

### 2026-07-10 — clarification stopped

The maintainer was not yet sure whether an open problem should specifically be
an unresolved gap or obstacle while issues and questions remain evidence or
investigative forms. The uncertainty is retained rather than resolved by
operator assumption. A concrete planning example may make the useful boundary
clearer during grooming or later framework design.

The insight remains `captured`: it preserves the proposed goal → open problems
→ work relationship and the confirmed within-system boundary without claiming
that the problem taxonomy, record shape, or lifecycle has been established.

## Grooming record

Not yet groomed. See
[`insight-grooming.md`](../../processes/insight-grooming.md).
