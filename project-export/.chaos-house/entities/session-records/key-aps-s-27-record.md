---
entity:
  identity:
    type: slug
    value: key-aps-s-27-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-06T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-27
---

# Subsystem and system-relationship concept review

## Frame

The eleventh concept review and the last at Direction level, executed as the
first invocation of the
[automated brainstorming](../../processes/sessions/automated-brainstorming.md)
session type: the operator worked brainstorming's steps autonomously, decided
where an interactive session would have asked the maintainer, and recorded
each decision with its rationale and the strongest case against it. Every
disposition below is a proposal until maintainer review. Intended result per
the task: the smallest clear model of subsystem ownership and relationships
needed for nested APS systems, with unsupported relationship machinery
removed.

## Orientation

- The vocabulary has no `Subsystem` entry. The concept lives in the framework
  definition's "System and subsystem" section as a bold-defined term, while
  the vocabulary's `System problem` entry, the Problem decomposition section,
  and most of `VISUALIZATION.md` call the same thing a "child system."
- Earlier reviews already removed the machinery this task anticipated:
  normative parent fields and cardinality (system-problem review), the
  universal relation registry ("APS does not require a universal relation
  registry"), and system ID/status/parent declaration fields. The remaining
  model is: the originating problem definition, strategy, or process links to
  the child; the child declares no parent.
- `VISUALIZATION.md`'s visual discipline still distinguished "governance
  relationships" — wording predating the authority review, but left without
  a referent once authority was removed from the framework.

## Concept review test

- **Meaning and purpose.** A child system is a system whose root problem was
  decomposed from another system's problem. Its purpose in the loop is
  delegation: a decomposed problem with an independent boundary and complete
  loop becomes the child's system problem.
- **Distinctness and dependencies.** Depends on system, problem, and
  decomposition. Distinct from process and capability (the definition already
  draws that line). Not distinct from "child system" — the two terms name one
  relationship.
- **Dependents.** System strategy ("coordinates its subsystems"), the Adapt
  step ("subsystem structure"), the assessment checklist, and the
  visualization views.
- **Durable identity or state.** None of its own. The child is an ordinary
  system with its own identity; "subsystem" names only the decomposition
  origin. No lifecycle machinery exists, and none is needed — correct per the
  strategy's rule for relationships.
- **Authoritative state.** The delegation link lives on the parent side, in
  the originating problem, strategy, or process; the child declares nothing.
- **Can the first loop operate without it?** Framework Operations has no
  child systems, but nesting is constitutive of the APS entry itself
  ("permits systems to form a hierarchy for problem decomposition") and of
  the System problem entry. What the first loop can operate without is a
  *separate concept* for it.

## Decisions (proposals until maintainer review)

1. **Merge "subsystem" into "child system."** All seven normative uses now
   say "child system"; the definition paragraph leads with the retained term
   and states that being a child names only the decomposition origin — the
   child is an ordinary system in every other way, and APS defines no
   separate subsystem concept. Rationale: one concept had two names, the
   same duplication pattern pruned in the `Strategy`/`Problem strategy` and
   task-family reviews; "child system" was already the majority spelling and
   says plainly what the relationship is, per the plain-language constraint.
   Strongest case against: "subsystem" is the widely recognized engineering
   word, and readers may reach for it. Answer: that recognition is the
   hazard — engineering subsystems are components of how a system operates,
   exactly what the definition warns must be modeled as a process or
   capability instead; "child system" cannot be misread that way.
2. **Add a concise `Child system` vocabulary entry** (revised in agent
   review; the session initially chose no entry). The initial rationale
   leaned on the missing-analogue heuristic — problem decomposition needs no
   "subproblem" entry — and on a citation the reviewer showed to be false:
   the relationship is carried by the `System problem` and `Adaptive
   problem-solving system` entries, not the `Problem` entry. The reviewer's
   stronger case: the concept's meaning and boundary had no single
   vocabulary home — the becoming-a-child condition sat in `System problem`,
   the link rule in `Adaptive problem-solving system`, and the
   process/capability boundary only in the framework definition — and the
   compilation principle from the task-family review places a concept's
   exact meaning and boundary in the vocabulary. The analogue answer also
   fails in reverse — a decomposed problem is just a problem, while a child
   system carries a boundary worth one consolidated statement. Resolution:
   entry added under Direction. The second review pass then caught that this
   first resolution restated the full definition in both files — the exact
   duplication the principle forbids and the open
   `apss.deduplicate-readme-against-vocabulary` task exists to remove — so
   the definition paragraph was trimmed to its operational explanation with
   a vocabulary reference, following the dedup worked example.
3. **Confirm the relationship model as already minimal; remove nothing
   further.** Parent-side links, no parent declaration, no registry, other
   cross-system interactions living where they affect operation — each piece
   was placed by an earlier reviewed decision, and this review found no
   unsupported machinery left. Strongest case against (added in agent
   review): the link may live in "the originating problem definition,
   strategy, or process" — three sanctioned homes — so enumerating a
   system's children means scanning all three, brushing against the
   adversarial check for multiple sources of truth. Answer: the three homes
   mirror where a decomposition decision can legitimately be recorded;
   naming one required home would be new machinery with no demonstrated
   need, and no system with child systems exists yet to demonstrate it.
   Recorded for the adversarial validation pass instead. Like the
   system-strategy review, this is a confirming disposition, further
   evidence the model is near its useful minimum.
4. **Remove the orphaned "governance relationships" wording** (rationale
   corrected in agent review; the session initially called it
   authority-removal residue). Git history shows the wording predates the
   authority review, which never targeted the word "governance" — so nothing
   was "missed," and the missed-sibling-pattern claim is withdrawn. The
   correct rationale: the authority removal left the distinction without a
   referent — the framework no longer defines governance relationships to
   keep visually distinct — so the visual discipline now contrasts
   decomposition edges with "artifact and evidence relationships" only.

## Validation

- Grep over `framework/`, `AGENTS.md`, and `README.md` confirms "subsystem"
  and "governance" no longer appear as terms in live framework surfaces; the
  remaining mentions are the deliberate "no separate subsystem concept"
  statements in the vocabulary entry and the definition, and the changelog's
  historical narrative.
- Link check over changed files confirms all markdown links resolve.
- Changelog updated per the compilation process; the P1 grooming history and
  Current state and the task file updated with the proposed dispositions.
- Known breakage, recorded rather than repaired per the established
  leave-historical-records-as-written precedent: the section rename breaks
  the `#system-and-subsystem` anchor linked from the retained 2026-07-12
  system-boundary-review record.

## Reviewer findings

The independent reviewer agent examined the uncommitted diff, re-ran the
validation greps, and traced git history for the claims. It found the diff
faithful to the task's scope and stop condition and the merge disposition
well-argued, and raised ten findings. Resolutions:

- **Confirmed and fixed (blocking/material):** the P1 grooming entry claimed
  its dispositions were "ratified at maintainer review" before that review
  happened (rewritten as pending); the no-entry rationale cited the `Problem`
  vocabulary entry for a relationship it does not carry (citation corrected
  in all four places, and the decision itself overturned — see decision 2);
  the "governance" deletion was misattributed to authority-review residue
  when git history shows the wording predates that review (rationale
  rewritten, missed-sibling claim withdrawn — see decision 4); decision 3
  lacked its required strongest case against (added — see decision 3).
- **Confirmed and fixed (minor/nit):** P1's Current state still listed this
  review as next while the grooming entry recorded it executed (Current
  state updated); the record's reviewer-findings placeholder and overstated
  no-residue validation claim (both rewritten); a newly introduced
  over-length line in the vocabulary (reflowed); a circular
  "problem-decomposed-into-a-problem" phrasing in the definition (now "split
  off from its parent's problem").
- **Confirmed, recorded rather than repaired:** the broken inbound anchor
  from the 2026-07-12 system-boundary-review record, per the
  leave-historical-records-as-written precedent the reviewer's own
  suggestion acknowledged as an option.

No findings were rejected. Revisions were material, so the reviewer was
rerun.

**Second pass.** The reviewer verified all ten resolutions as genuinely
implemented, re-ran the greps and history checks, and found the diff still
not ready: the vocabulary-entry fix had restated the full definition in both
the vocabulary and the framework definition — the duplication the compilation
principle forbids and the open `apss.deduplicate-readme-against-vocabulary`
task exists to remove — and the rewritten rationale overstated what "lived
only in the framework definition" (the link rule was already in the
`Adaptive problem-solving system` entry), a claim propagated to the
changelog and P1. Resolutions: the definition paragraph was trimmed to its
operational explanation with a vocabulary reference per the dedup worked
example; the entry's first sentence now carries the
independent-boundary-and-complete-loop condition, matching `System problem`;
the rationale was corrected in all three files to consolidation of scattered
rules; the orientation's leftover "residue" framing, the validation claim's
missing vocabulary mention, and one over-length changed line were fixed.
No findings were rejected in either pass.

## Lessons and friction

- First run of automated brainstorming: the deferred-decision model reached
  dispositions without maintainer input by applying the recorded strategy,
  prior review precedents, and the challenge step — but the independent agent
  review earned its place in the process on the first invocation. It caught
  a premature ratification claim, a false citation used as load-bearing
  rationale, a false history claim, and a missing required
  counter-argument, and it overturned one disposition (the vocabulary
  entry). Evidence for the experiment: autonomous execution drafts
  plausibly but self-certifies poorly; the reviewer stage is not ceremony.
- Whether the dispositions survive maintainer review unchanged is the
  experiment's real reading.
- Two consecutive reviews (system strategy, this one) now confirm rather
  than prune, strengthening the evidence that the Direction-level model has
  reached its useful minimum.

## Stopping point

Review executed; two agent-review passes completed with all findings
resolved and none rejected; the maintainer accepted the presented changes
and asked to finish the session.

## Acceptance and delivery

The maintainer reviewed the compiled scope with the reviewer findings and
explicitly asked to finish the session; per the session process that
approval authorizes delivery. Delivery ran amid concurrent sessions: three
had delivered upstream during this one (current-state concept `dfc62a4` and
two feedback captures), and the maintainer resolved the resulting
stash-pop conflicts in the changelog, `STATE.md`, and P1 by hand before
delivery resumed. Per the exclusion precedent, the accepted-but-undelivered
grooming-cadence session scope (its `grooming.md` change, session record,
and P1 grooming entry) stays uncommitted for its own delivery; `STATE.md`
lists it as the next step. Delivered as commit ca6a082; this delivery
reference was recorded in a follow-up commit per the established pattern.

---

Legacy participants: Claude Code operator (executing agent), independent reviewer agent, APS framework maintainer (review)

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-08-06-subsystem-and-relationships-review.md","legacyId":"apss.session.subsystem-and-relationships-review"}

---

[repository-import:session:apss.session.subsystem-and-relationships-review@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-08-06-subsystem-and-relationships-review.md]
