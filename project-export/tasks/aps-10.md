---
entity:
  identity:
    type: key
    value: APS-10
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:37.599Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-10
  keyNumber: 10
  labels:
    - repository-import
    - aps-legacy
  originSchedule: null
  originSession: null
  originTask: null
  parent: null
  priority: 3
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: backlog
  summary: null
  title: Reword all framework and process surfaces in plain language
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-21T07:31:09.898Z
---

# Reword all framework and process surfaces in plain language

## Scope (widened by grooming APS-S-41, 2026-08-21)

Everything a maintainer or reviewer reads: the framework package (wiki `framework/`), all process pages (`processes/…`, including `processes/sessions/grooming.md` and `brainstorming.md`), the project and problem declarations, and stream descriptions. Meaning must not change — this is rewording, not redefinition; anything that needs a meaning change goes back through the relevant review or grooming.

Trigger for the widening: in APS-S-41 the maintainer stumbled on grooming-process jargon ("revise", "disposition", "act/keep/merge/close") and asked for a bigger effort across the whole framework rather than a patch to one page.

## Intended result

A reader without the sessions' context can read any retained surface without stumbling over terms like "normative package", "lifecycle machinery", or "disposition", or finds a plain definition where a term must be kept. The teach-back validation in P1 has fewer wording flags to raise.

## Motivation

The maintainer asked on 2026-08-06 whether the strategy makes the system simple in language as well as structure, "so a normal person can easily understand." Grooming set the audience as the existing one (maintainer and reviewers) with plain wording as the quality bar. The concept reviews carry that constraint forward; this task is the backfill for what was already written.

## Open questions

- Larger than one session. Split by surface (processes first, since they are read every session; then framework; then declarations)?
- Wait for the concept-review clusters to finish so surfaces are not reworded twice, or do processes now and the rest after?
- Test for "plain enough": maintainer read-through per surface, plus a short list of banned words with their plain replacements.

## History

Captured 2026-08-06 from the maintainer's question in the plain-language grooming session. Widened to processes and attached to P1 by grooming APS-S-41.

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/plain-language-backfill.md","legacyId":"apss.plain-language-backfill"}
