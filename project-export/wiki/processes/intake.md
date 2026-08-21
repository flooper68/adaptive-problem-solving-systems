# Intake

Intake preserves an input faithfully before anyone decides what it means or what work follows. It first identifies **which kind of input** it is, then applies that kind's capture rules and destination. Interpretation and disposition belong to [grooming](sessions/grooming.md); capture never silently creates a problem, decision, or compiled knowledge.

Run intake inside an [intake session](sessions/intake.md), or session-bound inside another session when an input appears mid-work (announce the switch before extracting).

## Input kinds and where they go

| Kind | Test | Destination |
|---|---|---|
| **Framework feedback** | Someone reports that APS or this operation is unclear, incomplete, incorrect, burdensome, hard to apply, or missing a capability — or describes a useful outcome worth keeping. | `capture_record`, stream `framework-feedback` |
| **Insight** | A coherent conclusion drawn from evidence that may need corroboration, challenge, compilation, or reuse beyond its source. | `capture_record`, stream `insights` |
| **Usage observation** | An observed application, trial, or review of APS — what was attempted, by whom, with what result. | `capture_record`, stream `framework-usage` |
| **External foundation** | An authoritative external reference (research, standard, domain practice) compared with an APS choice. | `capture_record`, stream `external-foundations` |
| **Task candidate** | A bounded action (inquiry, experiment, review, remediation) that may improve the framework, this operation, or a future application and is not already represented. | `create_task` in `backlog`, label `task-candidate`, problem linked when known |

One input may yield more than one record: a report stays a report; the response it suggests becomes a separate, linked task candidate. A passing interpretation that needs no life of its own stays inside its source record. When the kind is unclear, ask the source one question; if still unclear, capture as framework feedback and say so in the record.

## Steps

1. **Announce.** Say that this is intake, name the kind you believe it is, and link this page. This is orientation, not a permission request when the source already asked for capture.
2. **Search first.** Look for an existing record, task, or problem on the same point (`list_records`, `list_tasks`, `search_wiki`). Link new evidence to an existing item rather than duplicating it, without erasing its own provenance.
3. **Preserve the initial statement** in the source's words before clarifying.
4. **Clarify proportionately.** Ask one load-bearing question at a time — two to four in total, fewer for a clear input — and adapt the next to the answer. Do not repeat what the source already said, steer toward a response, or demand grooming-level proof. Useful directions: what was observed and what prompted it; what follows and why; where it applies and where it may not; what better would look like and for whom; what contradicts it; what it could inform. "Unknown" is a valid answer. If clarification stops, record the next open question.
5. **Draft the record in the kind's shape** (below). Keep source words distinct from operator inference. Keep only the personal detail needed to follow up; reference access-controlled evidence, do not copy it.
6. **Present the exact record and destination** and wait for the source's approval. Silence is not approval.
7. **Capture session-bound.** Call the destination action with the session id. Link the originating task, session, or problem when the action supports it; otherwise keep the reference in the content.
8. **Stop.** Confirm what was captured and where. Do not offer grooming, propose tasks, or start work; the next possible action is grooming.

The record is durable when Chaos House accepts it. Repository backup follows on its own and is not a second intake destination.

## Capture shapes

Every record starts with a one-line title, then the sections for its kind. Empty sections stay present and say "none" or "unknown".

**Framework feedback** — Context · Observed problem or outcome · Desired outcome · Suggested response · Evidence. Keep observed, desired, and suggested apart: a proposed solution is evidence about expectations, not a requirement.

**Insight** — Claim · Scope · Reasoning · Supporting evidence · Contradicting or limiting evidence · Possible implications · Open questions. Record direct observations, external claims, and the operator's interpretation separately.

**Usage observation** — Who applied APS and to what · What was attempted · What happened · Where it was easy or hard · Recoverable reference.

**External foundation** — Source (citation or link) · What it says, in brief · Which APS choice it bears on · Agreement or tension, stated without deciding.

**Task candidate** — Proposed action · Intended result · Motivation · Evidence · Open questions. Use the closest declared session type. Capture must not invent evidence, imply approval, or rewrite the source as a settled response.

## Result

A captured input has a stable id, a recoverable source, content another operator can understand, its clarification recorded or the open question noted, and no promise of priority, adoption, or implementation. An input revealing an urgent safety, security, legal, or data-loss concern is escalated to the maintainer at once instead of waiting for grooming.

## Signal

Read by the retrospective from records and session notes: records whose kind grooming changed ÷ records captured; records grooming marked unfaithful to the source; `process:` corrections per intake session.
