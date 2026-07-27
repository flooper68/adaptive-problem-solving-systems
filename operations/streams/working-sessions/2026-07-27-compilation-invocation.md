---
id: apss.session.compilation-invocation
type: working-session
status: retained
recorded: 2026-07-27
accepted: 2026-07-27
closed: 2026-07-27
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: []
related_tasks: [apss.knowledge-compilation-refinement]
---

# Restrict compilation to brainstorming; tasks without problems

## Frame

Decide when knowledge compilation runs in Framework Operations and align the
declared processes with that decision. The responsible user and decision
authority is the APS framework maintainer. A useful stopping point is a
consistent set of uncommitted process changes under maintainer review.

The task-capture handoff decided mid-session exposed the task-selection rule,
and the maintainer extended the session to a third decision: dropping the
normative requirement that every selected task address a current problem.
That part changes `framework/` and was compiled under this session's own new
rule — inside brainstorming — with a changelog entry.

## Orientation

The maintainer asked how compiled knowledge is produced and when. The declared
processes named several compilation entry points: brainstorming's Compile step,
`process.md` step 6 for normative framework work and step 8 for recompilation,
insight grooming's routing of supported insights "into knowledge compilation,"
and feedback grooming's feeding of stable lessons "into validation and
knowledge compilation." The framework itself leaves compilation timing to each
instance (framework README, "Compile knowledge"), so this is an instance-level
declaration, not a framework change.

## Load-bearing question

The maintainer proposed that compilation happen only during brainstorming, and
that grooming should result in change of the knowledge. The two sentences
admit opposite readings — pulling all knowledge edits into one venue versus
pushing direct edits into every grooming process — so the operator asked which
relationship was intended before compiling.

## Decision

**Only brainstorming edits the compiled framework.** The maintainer selected
this explicitly from three offered relationships. Grooming processes update
only their own artifacts — insight dispositions, feedback records, problem and
task files — and do not invoke knowledge compilation directly.
`knowledge-compilation.md` is invoked solely from brainstorming's Compile
step, and recompilation after verification likewise happens within the
brainstorming session.

**The handoff is a captured task, not an untracked wait.** After the operator
noted that framework-worthy lessons could now surface in grooming without a
session picking them up, the maintainer directed that when another working
session or grooming invocation surfaces such a lesson, it is added as a task.
The compilation is captured through `task-intake.md` linking the source
evidence, and a brainstorming session executes the task. Pending lessons are
therefore visible in `tasks/` and flow through the normal task grooming and
selection discipline.

**A task no longer requires an addressed problem.** The operator noted that a
captured task could not be selected until problem grooming opened or linked a
problem. The maintainer decided to drop that rule: real operation produces
random one-off tasks — chores, fixes, and errands — with no long-running gap
behind them, and requiring a problem link would invent problems or leave the
work untracked. The compiled framework now says a task may or may not be in
the context of a problem: most implement or test part of a problem's
strategy, while a task addressing none may still be selected under the same
declared selection authority; it stays bounded and owned, is verified against
its own acceptance conditions rather than a problem signal, and recurring or
substantial problem-less work is evidence of an unrepresented gap for problem
grooming. The guardrails are operator-proposed compilation choices, not
maintainer wording, and are open to correction in review.

**No new vocabulary term.** The operator's first compilation named the
problem-less case a "transient task." In review the maintainer rejected the
name as official vocabulary; the framework simply states that a task may or
may not be in the context of a problem. Every "transient" the compilation
introduced was removed from the framework, changelog, and operations
processes. Occurrences of the word in retained pre-2026-07-27 stream records
are unrelated and left as written.

## Changes

- [`knowledge-compilation.md`](../../processes/knowledge-compilation.md) —
  gains an Invocation section declaring brainstorming's Compile step as the
  only entry point and stating the general rule: any other work session or
  grooming invocation captures a framework-worthy lesson as a task through
  task intake, and a brainstorming session executes it.
- [`process.md`](../../processes/process.md) — step 6 compiles normative
  framework work within a brainstorming session and names brainstorming as the
  only venue that edits the compiled framework; step 8 recompiles within the
  brainstorming session.
- [`brainstorming.md`](../../processes/brainstorming.md) — the Compile step
  states that brainstorming is the only work session that edits the compiled
  framework and that other sessions capture framework-worthy lessons as tasks
  it executes.
- [`insight-grooming.md`](../../processes/insight-grooming.md) — step 7
  captures the compilation of a supported or provisional framework-worthy
  insight as a task through task intake instead of linking it directly into
  knowledge compilation.
- [`framework-feedback-grooming.md`](../../processes/framework-feedback-grooming.md)
  — step 8 feeds outcome evidence into validation and captures a stable
  framework-worthy lesson as a compilation task.
- [`problem-grooming.md`](../../processes/problem-grooming.md) — step 6
  captures a framework-worthy lesson surfaced during grooming as a compilation
  task; grooming does not edit the compiled framework.

For the task-without-problem decision:

- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — `Task` leads with the
  inspectable-change definition and states a task may or may not be in the
  context of a problem; `Task candidate` resolves the problem relationship at
  selection by linking a problem or accepting that the work addresses none;
  `Task grooming` produces a readiness disposition without being scoped "for
  open problems" and may select problem-less work while still proposing
  evidenced gaps to problem grooming.
- [`README.md`](../../../framework/README.md) — the task definition and
  selection paragraphs carry the same change; the task system of record needs
  the addressed problem and strategy only when the task has one; recurring or
  substantial problem-less work is named as evidence of an unrepresented gap.
- [`CHANGELOG.md`](../../../framework/CHANGELOG.md) — material change recorded,
  including that no new task kind is named.
- [`process.md`](../../processes/process.md) — steps 3, 4, and 7 admit tasks
  that address no problem; verification for them compares against the task's
  own acceptance conditions.
- [`task-grooming.md`](../../processes/task-grooming.md) — purpose, framing
  step, readiness questions, and propagation admit a task with no `addresses`
  entry while keeping the problem-proposal path for evidenced gaps.
- [`insight-grooming.md`](../../processes/insight-grooming.md) — step 7
  scopes the selection restriction to work responding to an evidenced gap.
- [`problem-grooming.md`](../../processes/problem-grooming.md) — step 5 asks
  tasks selected for a problem to list its ID rather than asserting all
  selected tasks do.
- [`verification.md`](../../processes/verification.md) — a task with no
  addressed problem is verified against its acceptance conditions; the
  completion criterion reads the problem signal when the work addresses a
  problem.

No `framework/` file changed; the framework already delegates compilation
timing to the instance. The `compiled_into` relationship on insights is
unchanged — it records that a brainstorming compilation used the insight, not
that grooming performed one.

## Validation

Immediate checks: `git diff --check` is clean; the working tree contains only
this session's edits; remaining compilation references in `verification.md`
and `framework-adaptation.md` were reviewed and are consistent with the new
invocation rule; a repository-wide search for the old selection rule ("must
not be selected", "until it addresses", "for open problems") found no
surviving normative statement, and `framework/SCHEMA.md` carries no task
requirement. The framework definition, vocabulary, and changelog agree that
selection either links a problem or accepts that the work addresses none,
and after the naming correction the word "transient" appears nowhere in the
framework or the operations processes.

The task-capture handoff addresses the pile-up risk the first decision
created, at the cost of one task file per pending lesson; whether the single
entry point and task handoff reduce confusion or add overhead is delayed
outcome evidence for the
[knowledge-compilation-refinement](../../tasks/knowledge-compilation-refinement.md)
task. The task-without-problem rule removes selection friction at the risk of
untracked drift; the named counter-signal is recurring or substantial
problem-less work, which problem grooming should treat as evidence of an
unrepresented gap.

## Acceptance and delivery

The maintainer reviewed the changes iteratively during the session — the
task-capture handoff and the naming correction were both review outcomes —
and accepted the full scope on 2026-07-27 ("let's ship it"). The reviewed
scope was committed and pushed to `origin/main` per brainstorming delivery;
the delivery commit is referenced in this record's frontmatter follow-up.
