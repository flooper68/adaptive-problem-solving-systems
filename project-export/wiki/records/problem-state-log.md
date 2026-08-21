# Problem state log

This is the project-owned append-only history of problem signal readings and health assessments. Signal definitions remain in Verification; Current state carries the latest meaning. Evidence recorded here does not create work without a separate grooming decision, and this path has no product-level semantics.

Migration cutoff: `2026-08-17T09:16:27.161Z`. Source rows are preserved verbatim as canonical JSON; paired timeline events preserve actor and session-key attribution. Future entries are appended with `append_wiki_file` against the complete current page SHA.

<a id="aps-p-2"></a>
## APS-P-2 — The APS MVP is unfinished and has not run its complete loop

Problem slug: `p1`.

### 2026-08-17T07:00:45.682Z — signal reading — `88899283-dbff-4c53-b34c-5e58ca1afd41`

Legacy source row:

```json
{
  "id": "88899283-dbff-4c53-b34c-5e58ca1afd41",
  "readAt": "2026-08-07",
  "components": [
    {
      "name": "Concept review inventory",
      "value": "12 reviewed; 18 review tasks remain"
    },
    {
      "name": "Loop responsibilities",
      "value": "Grooming, compilation, adaptation, and delivery have run; teach-back and adversarial verification have not"
    },
    {
      "name": "Maintainer understand-and-run check",
      "value": "Untested since consolidation"
    }
  ],
  "notes": "Imported structured reading from P1 current state at source commit 43b9f691.",
  "readByType": "user",
  "readByAgentName": null,
  "sessionId": "90e6f517-752a-4170-9385-02bf8c87461d",
  "createdAt": "2026-08-17T07:00:45.682Z"
}
```

Paired append-only timeline event:

```json
{
  "id": "7689ba8f-7f4e-473a-ae98-8d51ce17da9d",
  "type": "reading_recorded",
  "actorType": "user",
  "actorAgentId": null,
  "actorAgentName": null,
  "taskId": null,
  "taskKey": null,
  "taskTitle": null,
  "agentId": null,
  "agentName": null,
  "artifactSlug": null,
  "artifactTitle": null,
  "problemKey": "APS-P-2",
  "problemSlug": "p1",
  "problemTitle": "The APS MVP is unfinished and has not run its complete loop",
  "recordId": null,
  "recordKey": null,
  "recordStream": null,
  "relatedTaskId": null,
  "relatedTaskKey": null,
  "relatedTaskTitle": null,
  "project": "aps-framework-operations",
  "sessionId": "90e6f517-752a-4170-9385-02bf8c87461d",
  "sessionKey": "APS-S-34",
  "message": "Signal read for \"p1\" on 2026-08-07: Concept review inventory 12 reviewed; 18 review tasks remain; Loop responsibilities Grooming, compilation, adaptation, and delivery have run; teach-back and adversarial verification have not; Maintainer understand-and-run check Untested since consolidation",
  "createdAt": "2026-08-17T07:00:45.686Z"
}
```

### 2026-08-17T09:56:43Z — verification reading — `APS-S-36`

- **Concept review inventory:** 12 reviewed; 18 review tasks remain. APS-1
  revised the declaration contract but was not one of the remaining concept
  review tasks.
- **Loop responsibilities:** grooming, compilation, adaptation, and delivery
  have run; teach-back and adversarial verification have not.
- **Maintainer understand-and-run check:** the migration exposed that APS was
  confusing a declaration responsibility with one repository representation.
  The maintainer understood and approved the representation-neutral
  distinction and the repository/structured-project profiles. A full unaided
  explanation and end-to-end run remains untested.

**Comparison with 2026-08-07:** improved in the understandability dimension:
one file-shaped rule that contradicted observed use is removed, and the
maintainer approved the replacement model. Inventory and never-run validation
responsibilities are unchanged, so P1 remains open.

**Immediate verification:** exact canonical content was read back; remaining
`SYSTEM.md` and `STRATEGY.md` references are confined to the explicit
repository profile or historical changelog context; the APS project reports no
declaration warnings; and the repository projection converged successfully at
commit `6134bd321ec43f2e20d2963bc1f7a196d8c2c4c5`.

### 2026-08-17T17:15:00Z — verification reading — `APS-S-39`

- **Concept review inventory:** 12 reviewed; 18 concept-review tasks remain
  (APS-21 selected, not yet started). APS-60 revised the grooming process and
  is not a concept review.
- **Loop responsibilities:** grooming, compilation, adaptation, and delivery
  have run; teach-back and adversarial verification have not. The first root
  grooming (APS-S-38) ran but skipped its verification, strategy, and
  adaptation substance — maintainer feedback APS-R-27.
- **Maintainer understand-and-run check:** the maintainer judged the revised
  grooming process "reasonable" on review and chose to run the next
  invocation as the experiment that validates it. A full unaided
  understand-and-run remains untested.

**Comparison with 2026-08-17T09:56:43Z (APS-S-36):** unchanged on inventory
and never-run responsibilities; unresolved on understandability — the
process revision is approved but its effect on grooming quality is unverified
until the next invocation runs under it. P1 remains open.

**Immediate verification:** the revised `processes/sessions/grooming.md` was
read back after the write; the `grooming` session type still resolves to that
path; no declaration warnings; the revision keeps the single process, the
item/branch/root scopes, and the deep-grooming mechanics from APS-59.

### 2026-08-21T07:20:00Z — grooming reading — `APS-S-41`

- **Concept review inventory:** 12 reviewed; 18 concept-review tasks remain
  (APS-21 todo, 17 backlog), confirmed against the live board. No concept
  review has run since the migration.
- **Loop responsibilities:** grooming (APS-S-35, S-38, S-40, S-41),
  verification (readings S-36, S-39), compilation (legacy), adaptation
  (APS-60 approved and applied), and delivery have each run at least once;
  teach-back and adversarial review never. New: the APS-R-27 → APS-60 →
  S-40/S-41 chain is the first real need carried through the loop into an
  approved adaptation that changed a subsequent run.
- **Maintainer understand-and-run check:** asked directly this session.
  Answer: **no**, the maintainer cannot explain and run the whole process
  unaided today. Last stumble: deferred by the maintainer to the end of this
  session (recorded there if given).

**Comparison with 2026-08-17T17:15:00Z (APS-S-39):** unchanged on inventory;
slightly improved on loop responsibilities (first need-to-changed-run chain
exists); understandability now read as a plain "no" where S-39 recorded
"untested" — a clearer, not a worse, reading. P1 remains open. Root health:
unset — APS declares no health scale and the maintainer stated no verdict.

**Addendum at close of APS-S-41:** the maintainer did not name a single
"last stumble"; the session showed two — the grooming vocabulary ("revise" as
a disposition name) and the sense that the grooming run skipped or compressed
steps (inputs not shown, no health proposal, no problem-tree review, tasks
created without challenge). Health stays unset: a yellow verdict was proposed
but the maintainer chose to close and review the process first. Root health
and the problem-tree review are carried to the next grooming run.

### 2026-08-21T08:30:00Z — verification reading — `APS-S-43`

- **Concept review inventory:** 12 reviewed; 7 clustered concept-review tasks
  remain after the APS-S-41 merge (APS-21, 23, 14, 19, 22, 15, 32). APS-S-43
  added a process, not a concept review.
- **Loop responsibilities:** unchanged set of run responsibilities; teach-back
  and adversarial review still never. New: the system now declares a way to
  verify and adapt its processes (retrospective), which closes the gap that
  process adaptation had no reading. No retrospective has run yet, so this is
  declared, not proven.
- **Maintainer understand-and-run check:** not re-asked this session; the
  APS-S-41 answer ("no") stands.

**Comparison with 2026-08-21T07:20:00Z (APS-S-41):** inventory figure restated
in cluster terms (18 tasks → 7 clusters, same 12 reviewed); loop
responsibilities unchanged in what has run, with one new declared process;
understandability carried, not re-read. P1 remains open.

**Immediate verification:** `retrospective` session type resolves to
`processes/sessions/retrospective.md` with no process warnings; `process.md`,
`processes/README.md`, and the four session pages were read back after the
writes; no declaration warnings. Delayed evidence: whether the retrospective
works is unreadable until it has run twice on one process (its own Signal
section); next trigger is APS-63 run as a retrospective on grooming, or five
grooming runs.

