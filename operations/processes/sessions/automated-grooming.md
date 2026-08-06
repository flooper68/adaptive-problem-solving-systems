# Automated grooming

## Purpose

Groom captured inputs autonomously up to — but never past — the maintainer's
decision: the agent orients, clarifies, and assesses each item in scope and
drafts one proposed disposition with its rationale, an independent reviewer
agent checks the proposals, and the maintainer then approves, adjusts, or
rejects each disposition before anything is recorded as approved or delivered.
This specializes [`grooming`](grooming.md), whose rules, dispositions, and
propagation apply unchanged; only the preparation is autonomous.

This session type is an experiment. Retain evidence from its first invocations
in the working-session records so grooming can decide whether to keep, revise,
or remove it.

## Preconditions

- The maintainer names the scope when invoking the session — specific items or
  a bounded set such as all ungroomed records of one stream.
- The maintainer approves every disposition; the agent only proposes. An item
  is not `groomed` until its approved entry is recorded.
- Grooming never edits the compiled framework; that invariant applies here
  unchanged.

## Procedure

1. **Assess autonomously.** For each item, follow the orient, clarify, and
   assess steps of [`grooming.md`](grooming.md) without maintainer
   interaction. Where clarification would need the reporter or maintainer,
   record the open question instead of assuming an answer; when a missing
   answer could materially reverse the disposition, propose `keep` with an
   evidence request rather than a stronger disposition. Draft exactly one
   proposed disposition per item with its rationale. Do not rewrite source
   records.
2. **Agent review.** Launch an independent reviewer agent that did not draft
   the proposals. It checks each proposal against the source records, the
   evidence consulted, and the rules in [`grooming.md`](grooming.md). Record
   its findings; revise the proposals where findings are confirmed and record
   rejected findings with reasons.
3. **Maintainer decision.** Present per item: the clarified claim, evidence
   consulted, the proposed disposition with rationale, open questions, and the
   reviewer findings with their resolutions. The maintainer approves, adjusts,
   or rejects each disposition; items left undecided stay ungroomed with the
   assessment retained as a proposal in the working-session record.
4. **Record and propagate.** For each approved disposition, append the dated
   grooming entry to the item's authoritative file and execute the approved
   propagation per [`grooming.md`](grooming.md), including intake captures and
   bidirectional links.
5. **Deliver.** The maintainer's per-item disposition approvals are the
   approval signal for delivering exactly those recorded entries and their
   propagation. Stage the session scope, commit, push, and record the delivery
   per [`ai-agent-tasks.md`](../ai-agent-tasks.md); no separate delivery
   confirmation is required, and nothing beyond the approved scope rides on
   the signal.

## Evidence and retention

The item's file remains authoritative for its approved grooming history; the
working-session record retains the proposals as drafted, reviewer findings and
resolutions, per-item decisions, undecided items with their open questions,
and, when delivered, the commit. Raw agent transcripts stay in their native
recoverable sources, linked when material.
