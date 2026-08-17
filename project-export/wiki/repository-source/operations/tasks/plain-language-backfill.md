---
id: apss.plain-language-backfill
type: task
status: open
owner: APS framework maintainer
created: 2026-08-06
source: Maintainer question during the plain-language grooming session
source_records:
  [operations/streams/working-sessions/2026-08-06-plain-language-constraint-grooming.md]
---

# Reword existing surfaces in plain language

## Proposed action

Pass over the surfaces written before the plain-language constraint entered
P1's strategy and reword them in everyday language: replace specialist
vocabulary with plain words, define any term the framework must keep, and cut
sentences a reader has to reread. The maintainer scoped the pass to everything:
the framework package (`framework/`), Operations processes
(`operations/processes/`), problem files (`operations/problems/`), and stream
documentation. Meaning must not change — this is rewording, not redefinition;
anything that turns out to need a meaning change goes back through the
relevant review or grooming instead.

## Intended result

A reader without the sessions' context can read any retained surface without
stumbling over terms like "normative package," "lifecycle machinery," or
"disposition," or can find a plain definition where a term is kept. The
teach-back validation pass in P1 has fewer wording flags to raise.

## Motivation

The maintainer asked on 2026-08-06 whether the strategy makes the system simple
in language as well as structure, "so a normal person can easily understand."
Grooming set the audience as the existing one (maintainer and reviewers) with
plain wording as the quality bar. The concept reviews now carry that constraint
forward; this task is the backfill for what was already written.

## Evidence

- The grooming decision and its rationale in
  [P1's grooming history](../problems/p1-finish-mvp-and-run-loop.md).
- P1's own evidence that the maintainer's usability judgment is the relevant
  outcome evidence for understandability.
- No reviewer teach-back has run yet, so no independent list of stumbling
  points exists; the first teach-back could seed one.

## Open questions

- The scope is almost certainly larger than one working session. How should it
  split — by surface (framework first), or by waiting for teach-back evidence
  of the worst offenders?
- Should the pass wait until the concept reviews finish, so surfaces are not
  reworded twice?
- What is the concrete test for "plain enough" — a reviewer read-through, a
  wordlist, or maintainer judgment per surface?

## Grooming log

### 2026-08-06 — captured

Captured by the Claude Code operator from the maintainer's direct question in
the plain-language grooming session. Clarified with the maintainer one
question at a time: the audience stays the maintainer and capable reviewers
(plain wording is a quality bar, not a new consumer group); a backfill task is
wanted rather than forward-only application; and the scope is all surfaces,
not just the framework package. Splitting and sequencing are left to task
grooming.
