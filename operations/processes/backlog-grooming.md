# Backlog grooming

## Purpose

Turn a captured idea into an explicit, evidence-aware disposition without
silently treating it as committed work. Grooming improves decision quality; it
does not itself authorize a normative framework change.

## Invocation and roles

Groom an item when the maintainer requests it, new evidence makes it timely, a
dependency is resolved, or planning needs another ready candidate.

- An operator facilitates the analysis and updates the durable item.
- The item owner supplies context or identifies who can.
- The APSS framework maintainer approves the final disposition and alone
  selects ready work into `operations/work/PLAN.md`.

Set `status: grooming` while analysis is materially underway.

## Procedure

1. **Orient.** Read the item, its source, current framework and examples,
   current plan, compiled knowledge, related backlog items, and relevant work
   history.
2. **Check identity.** Merge duplicates, split unrelated ideas, and preserve
   links to their original sources and IDs.
3. **Frame the need.** State the affected consumer, current problem or
   opportunity, expected outcome, and why it belongs within this system's
   boundary.
4. **Classify the effect.** Identify whether it may change the normative
   framework, a supporting example, stewardship operations, or only current
   understanding. One item may affect several, but the distinction must remain
   explicit.
5. **Resolve load-bearing uncertainty.** Use discussion, research, or a bounded
   experiment when a missing answer could materially reverse the disposition.
   Record facts, assumptions, disagreements, and unavailable evidence
   separately.
6. **Shape candidate work.** Describe the smallest coherent change or inquiry,
   affected artifacts, dependencies, risks, validation approach, and an owner.
   Split work that cannot be evaluated or completed as one bounded result.
7. **Check readiness.** Apply the readiness questions below. Unanswered
   questions are allowed only when the plan explicitly resolves them before
   they become dangerous or expensive.
8. **Propose and approve a disposition.** The maintainer records one disposition
   and its rationale. Do not equate desirability with current priority.
9. **Propagate the result.** Update the item's frontmatter and grooming log.
   If selected, reference it from the current plan; do not erase the source
   item or its rejected alternatives.

## Readiness questions

An item is ready only when a planner can answer:

- What consumer problem or opportunity are we addressing?
- What observable outcome would make the work worthwhile?
- Is the proposed scope bounded enough for one plan item?
- Which normative artifact, example, or operating process may change?
- What evidence supports acting now, and what remains assumption?
- Which discussion, research, or experiment is still necessary?
- How will artifact correctness and consumer outcome be validated separately?
- What dependencies, compatibility risks, or migration costs exist?
- Who owns execution, validation, and approval?
- What acceptance conditions permit the work to stop or be reconsidered?

## Dispositions and states

- `ready` — sufficiently understood to be considered during planning. This is
  not a commitment or priority promise.
- `deferred` — potentially valuable but blocked, premature, or deliberately
  postponed. Record a reconsideration trigger, condition, or date.
- `rejected` — outside the boundary, unsupported, harmful, or not worth
  pursuing. Preserve the rationale and evidence.
- `merged` — represented by another durable item. Record the target ID.

`captured` and `grooming` describe work before disposition. When the maintainer
selects a `ready` item into the durable plan, set it to `planned`; execution may
then use `in-progress`, `completed`, or `cancelled`. These execution states do
not replace the work log.

## Required durable result

Append a grooming-log entry containing:

- date, participants, and evidence consulted;
- clarified problem, expected outcome, and scope;
- important facts, assumptions, and unresolved questions;
- readiness gaps or acceptance conditions;
- approved disposition and rationale; and
- reconsideration trigger, target item, or plan reference when applicable.

Any normative change still follows the
[framework operating loop](framework-loop.md) and declared adaptation authority.
