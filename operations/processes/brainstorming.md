# Brainstorming

## Purpose

Discuss an APSS idea, task, or research topic with the maintainer, use relevant
evidence and existing knowledge, and compile reviewable changes directly into
the framework or a concrete APSS instantiation. Iterate with the maintainer until
the result reaches an accepted stopping point.

## Procedure

1. **Frame.** State the topic, intended result, responsible user, relevant goal
   and open problem when applicable, boundary, and what a useful stopping point
   would be.
2. **Orient.** Read the current framework or instantiation, relevant streams,
   prior decisions, task files, feedback, and knowledge. Keep missing context explicit.
3. **Explore.** Elicit observations, interpretations, alternatives, constraints,
   and trade-offs. Ask one load-bearing question at a time and adapt the next
   question to the answer.
4. **Distinguish.** Keep source evidence, interpretation, unresolved questions,
   authorized decisions, and possible actions conceptually separate.
5. **Compile.** Apply the current conclusions directly as uncommitted changes to
   the authoritative framework knowledge or system instantiation. For framework
   knowledge, follow [`knowledge-compilation.md`](knowledge-compilation.md); for
   an instantiation, follow its declared compilation process. Update the
   artifact's simple changelog when its compiled knowledge materially changes.
   Do not create a parallel candidate folder, compilation report, or manifest.
6. **Review iteratively.** Present the changes to the maintainer, incorporate
   corrections and further ideas, and repeat exploration and compilation as
   needed. Do not infer approval from exploratory language or silence.
7. **Close.** Stop when the maintainer accepts the result, explicitly ends the
   session, or leaves a clear unresolved question or next trigger. Follow the
   system's declared authority before committing, publishing, or using an
   adaptation.

## Evidence and retention

Raw evidence remains in its source streams. Git provides the reviewable diff and
accepted history; the compiled artifact's changelog summarizes material
knowledge changes. Retain one working-session record with participants,
affected problems and tasks, material decisions, changed artifacts, and the
stopping point. Link independently managed insights or decisions rather than
duplicating their full content.
