# Dogfooding

Take one thing noticed while using APS and fix it in the same sitting:
write down what was seen, work out what it means, decide, change the
page, check. This is for small, clear changes the maintainer wants done
now rather than waiting for grooming. Whoever starts the session judges
whether the item is small enough; if it turns out not to be, step 3 hands
it on.

Unlike grooming, this session both records the input and decides on it.
Unlike brainstorming, it starts from one concrete observation, not a
topic. Unlike the retrospective, it looks at one fresh observation now,
not at a process's run history.

## Steps

1. **Say what was noticed.** The maintainer states the observation in
   their own words and what a good outcome looks like. Search records,
   tasks, and problems for the same observation; if it already exists,
   use that record instead of making a new one.

2. **Record it.** Propose the stream and the exact text, then call
   `capture_record` bound to the session. Starting the session is the
   permission for this one record; anything else noticed along the way
   needs its own approval. The record holds what was seen, not the fix.

3. **Work out what it means.** Read the pages the observation touches —
   process pages, declarations, session types, or `framework/`. Name the
   cause, the page or pages that would change, and what would change.
   If it turns out bigger than expected — it touches many pages, changes
   a problem statement or strategy, or needs evidence that is not at
   hand — say so. The record stays captured; with the maintainer's go,
   hand it on to grooming or brainstorming (as a task if they want one)
   and go to step 7.

4. **Decide.** Show the recommended change, one alternative (or say
   plainly that there is no sensible one), the strongest objection, and
   the effect the change should have by the time it is next looked at.
   The maintainer accepts, changes, or rejects it.

5. **Change the page.** Show the exact new text. A `framework/` change is
   prepared and published the way brainstorming does it: follow
   `../knowledge-compilation.md` for the draft (one canonical target,
   exact text, its `framework/CHANGELOG.md` line, overlap and plain-
   wording check) and `../framework-adaptation.md` for approval and
   publication. A process page change states the effect it should have,
   so the retrospective can check it later. Session types change through
   `save_session_type`. Apply only approved text, session-bound, with the
   SHA-guarded edit or write.

6. **Check.** Re-read every written page, its links, and — for session
   types — that the process resolves. Then `groom_record` the record as
   accepted, naming the decision and the changed paths. This standard
   disposition needs no separate approval.

7. **Close.** Summarise: the record, the cause, the decision, the changed
   paths with their new SHAs, the expected effect, and any handoff. Close
   on the maintainer's go.

## Signal

Read by the retrospective from session records: sessions ending in an
applied change ÷ sessions run; applied changes reverted later; expected
effects met at the next retrospective.
