# Intake session

Session type `aps-intake`.

## Purpose

Receive one or more inputs from one source, identify each input's kind, and preserve each faithfully through [`../intake.md`](../intake.md). The session ends at capture; it never grooms, decides, or starts work.

## When to run it

- The maintainer or another source brings feedback, an insight, an observation, a reference, or a proposed action and asks for it to be kept.
- A conversation turns out to be intake before any other session is open.

If an input appears during another session, do not open a second session: announce the switch and run `../intake.md` session-bound inside the current one.

## Procedure

1. **Frame.** State the source, the capture scope the source authorized, and the problem the inputs relate to when known. Conversation is not captured automatically.
2. **Split.** If the source brought several things, list them and agree the list before capturing any. One record per coherent input.
3. **For each input, run `../intake.md`** — announce the kind, search for existing items, preserve the statement, clarify, draft in the kind's shape, present, capture session-bound, stop.
4. **Close.** Record in the session: source, each input with its kind and destination (record or task key), links made to existing items, open clarification questions, and any input the source withdrew. End with outcome `completed` when every listed input is captured or withdrawn; `interrupted` otherwise, naming what remains.

## Boundaries

- Capture does not confer truth, priority, or approval; the record says so when the source might assume otherwise.
- No grooming offers, no follow-up tasks, no framework edits from inside this session. The next possible action is [grooming](grooming.md).
- When the maintainer corrects how the session is run, add a `session_note` starting with `process:` saying what was corrected and at which step.

## Signal

Read by the retrospective from session records: sessions ending `completed` ÷ sessions run; inputs per session left without a record or a withdrawal; `process:` corrections per session; together with the signal on `../intake.md`.
