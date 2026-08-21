# Retrospective

Check whether one process works as written and as run, and change the page from evidence. The object is one process page under `processes/`. Problems, tasks, strategy, and the framework are out of scope here; anything learned about them is handed to grooming or brainstorming.

## When to run it

Run on one named process when any of these is true:

- grooming step 8 scheduled it;
- the process has run five times since its last retrospective;
- the maintainer asks for it;
- the previous retrospective could not read the process signal.

One process per session. The retrospective process itself is reviewed the same way.

## Steps

1. **Set the boundary.** Name the process, its current page SHA, the last retrospective on it (from the [process state log](../../records/process-state-log.md)) with its expected effects and parked items, and the sessions since then. Promote any parked item whose trigger has fired.

2. **Ask what didn't work.** Before reading any session, ask the maintainer in plain words, about this process and the system around it:
   - What didn't work since the last retrospective?
   - What cost more than it was worth?
   - What did you avoid doing, and why?
   - What did you expect after the last change that didn't happen?

   Write each answer down in the maintainer's words before interpreting it.

3. **Read the sessions.** For each session in the window, read the page as written against the session as run. Count: completed vs interrupted; steps with a note or action vs steps on the page; `process:` notes (maintainer corrections of how the session ran); decisions still standing at the next session vs reversed; duration. For each answer from step 2, say whether the records confirm it, contradict it, or are silent.

4. **Take the reading.** Write one line in the fixed shape used by the log: completed/total · steps covered · corrections · decisions held · expected effects met/missed/unreadable · reported failures. Compare with the previous entry: better, worse, same, or unreadable. Where data is missing, write "unreadable" and why — never estimate.

5. **Collapse and rank.** Turn every answer, deviation, correction, and missed effect into a finding. Merge findings that share one cause. Rank by: (1) seen more than once, or carried from the last retrospective; (2) would leaving it change a decision the system makes; (3) the fix has an effect that can be checked next time. Work the top three at most. Park everything else with one line: the finding, why it ranked below the cut, and what would admit it next time.

6. **Propose the change.** For each worked finding state the strongest explanation and one alternative, then an exact edit to the process page and the effect it should have by the next retrospective, in checkable terms. Prefer removing or merging steps over adding. A finding about a problem, strategy, or the framework becomes a handoff to grooming or brainstorming, not an edit here. If the finding holds for more than one process, also propose a line for the [design rules](../design-rules.md).

7. **Decide.** Show the exact text to the maintainer. Apply approved edits session-bound with the SHA-guarded wiki edit. Keeping the page as it is is also a decision; record it with the reason.

8. **Close.** Append the entry to the process state log with `append_wiki_file`. Record in the session: boundary, reading, worked findings with their expected effects, parked items with triggers, handoffs, approved edits with the new page SHA, and the next trigger.

## Signal

Share of edits made by the previous retrospective whose expected effect was met, plus the reading trend from step 4. Unreadable until two retrospectives have run on the same process.

## Done when

Every session in the window was read; every maintainer answer is marked confirmed, contradicted, or silent against the records; the reading is taken or marked unreadable with a reason; every previous expected effect is marked met, missed, or unreadable; at most three findings were worked, each with an approved edit or a recorded keep, and an expected effect; every parked item has a trigger; the log entry is appended.
