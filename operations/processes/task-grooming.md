# Task grooming

## Purpose

Turn a captured candidate action into an explicit, evidence-aware disposition
without silently treating it as committed work. Grooming improves decision
quality; it does not itself authorize execution or a normative framework
change. Task grooming does not open, reframe, prioritize, or close problems. If
the candidate exposes an unrepresented evidenced gap, propose it to problem
grooming; work that responds to no such gap may be selected without an
addressed problem.

## Invocation and roles

Groom an item when the maintainer requests it, new evidence makes it timely, a
dependency is resolved, or the current problem set needs another ready task.

- An operator facilitates the analysis and updates the durable item.
- The item owner supplies context or identifies who can.
- The APS framework maintainer approves the final disposition and alone
  selects a task for execution.

## Procedure

1. **Orient.** Read the item, its source, current framework and Operations
   application,
   current strategy, problem files, compiled knowledge, related task files, and
   relevant session history.
2. **Check identity.** Merge duplicate actions, split unrelated actions, and
   preserve links to their original source records and IDs.
3. **Frame the response.** State the affected consumer, the addressed open
   problem with its parent and strategy — or that the work addresses none —
   the proposed action, expected outcome, and why it belongs within this
   system's boundary. If the work responds to an evidenced gap no current
   open problem represents, propose a problem file before treating it as
   ready; work responding to no such gap may be ready without one.
4. **Classify the effect.** Identify whether it may change the normative
   framework, Framework Operations, a future application, or only current
   understanding. One item may affect several, but the distinction must remain
   explicit.
5. **Resolve load-bearing uncertainty.** Use discussion, research, or a bounded
   experiment when a missing answer could materially reverse the disposition.
   Record facts, assumptions, disagreements, and unavailable evidence
   separately.
6. **Shape candidate work.** Describe the smallest coherent change or inquiry,
   affected artifacts, dependencies, risks, validation approach, and an owner.
   Prefer work that can produce its artifact in one working session.
   Split work that has several independently reviewable results or stopping
   points, duplicates the whole open problem, or cannot be evaluated as one
   bounded result.
7. **Check readiness.** Apply the readiness questions below. Unanswered
   questions are allowed only when the task approach explicitly resolves them
   before they become dangerous or expensive.
8. **Propose and approve a disposition.** The maintainer records one disposition
   and its rationale. Do not equate desirability with current priority.
9. **Propagate the result.** Record the disposition in the item's grooming log
   and update its current state. On selection, list its problem IDs under
   `addresses` or record that it addresses none. A task stays `open` under
   `tasks/` until it is closed; a task closed by grooming — rejected, merged,
   or duplicated — moves under `tasks/archive/` with its reason. Do not erase
   the source or its rejected alternatives.

## Readiness questions

An item is ready only when the responsible operator can answer:

- Which current open problem does this address and how does that problem
  decompose its parent — or does the work address none?
- How does the work implement or test that problem's strategy, or what bounded
  need does it meet without one?
- What consumer problem or opportunity are we addressing?
- What observable outcome would make the work worthwhile?
- Can the task produce its artifact in one working session?
- Does it implement or test a bounded part of the problem strategy rather than
  duplicate the whole problem or depend on problem closure?
- Which normative artifact, application, or operating process may change?
- What evidence supports acting now, and what remains assumption?
- Which discussion, research, or experiment is still necessary?
- How will artifact correctness and consumer outcome be validated separately?
- What dependencies, compatibility risks, or migration costs exist?
- Who owns execution, validation, and approval?
- What acceptance conditions permit the work to stop or be reconsidered?

## States and dispositions

A task has two states, mirroring the problem lifecycle:

- `open` — the task is part of the current task collection. It lives directly
  under `tasks/`.
- `closed` — the system will no longer act on it. It moves under
  `tasks/archive/` with its reason.

Nothing else is a state. Readiness, deferral, selection, and progress are
*dispositions and events*, recorded in the grooming log and the task's current
state rather than in the status field, in the same way `solved` is an
assessment about a problem rather than one of its lifecycle states:

- **Ready** — sufficiently understood to be considered for selection. Not a
  commitment or priority promise.
- **Deferred** — potentially valuable but blocked, premature, or deliberately
  postponed. Record a reconsideration trigger, condition, or date. The task
  stays `open`, exactly as a problem kept open without current work does.
- **Selected** — the maintainer committed the task to execution. The working
  session record and the uncommitted working tree show which task is active;
  a status field asserting it would be a second source of truth.

Closure records its reason in the task: delivered, rejected as outside the
boundary or not worth pursuing, merged into another item (`merged_into`), or
superseded by one (`superseded_by`). A reason is not a state, and the reason
must survive in the file rather than only in the status name.

These states apply to task files. Insights and feedback records keep their own
vocabularies in their own processes. The task owns current state; session
records own material history.

## Required durable result

Append a grooming-log entry containing:

- date, participants, and evidence consulted;
- clarified problem, expected outcome, and scope;
- the current problem-file and parent-problem references;
- important facts, assumptions, and unresolved questions;
- readiness gaps or acceptance conditions;
- approved disposition and rationale; and
- reconsideration trigger or target task when applicable.

Any normative change still follows the
[Framework Operations process](process.md) and declared adaptation authority.
