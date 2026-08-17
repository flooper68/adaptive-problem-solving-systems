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

