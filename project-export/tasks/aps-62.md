---
entity:
  identity:
    type: key
    value: APS-62
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-21T07:30:51.874Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-62
  keyNumber: 62
  labels: []
  originSchedule: null
  originSession: session:key:APS-S-41
  originTask: null
  parent: null
  priority: 2
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: todo
  summary: null
  title: Revisit and nail down the system-level definitions
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-21T09:39:57.935Z
---

## Why

Grooming APS-S-41 (2026-08-21): the maintainer answered "no" to being able to explain and run the whole APS process unaided. Before more concept reviews, the maintainer wants the top-level declarations reviewed and nailed down in a dedicated session, separately from P1's own pages.

## Work

Go through the project's four declarations with the maintainer, one page at a time, in plain language:

1. **Problem** (`problem.html`) — what is the root condition this system exists for?
2. **Strategy** (`strategy.html`) — approach, grooming guidance, adaptation rule. Still right? Anything ceremonial?
3. **Verification** (`verification.html`) — is it clear what gets checked, when, and what counts as evidence?
4. **Process** (`process.html`) — the operating loop. Can the maintainer follow it step by step?

Record every meaning change as a decision. Wording-only fixes belong to APS-10 (plain-language rewording); note them there instead of doing them here.

## Done when

The maintainer can explain the system's problem, strategy, verification, and process in their own words, and the four pages say exactly that.

## Context

Created by grooming APS-S-41 (adaptation decision L3). Sibling task: APS-61 "Revisit and nail down P1's definitions" — do this one first; the system-level declarations sit above P1 in the hierarchy (grooming APS-S-50, 2026-08-21).
