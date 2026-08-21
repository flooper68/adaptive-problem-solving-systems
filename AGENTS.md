# Agent guidance

## What APS is

APS (Adaptive Problem Solving) is a framework for systems that solve
problems and improve how they solve them using evidence from real outcomes.
Artifacts, validation, learning, and adaptation support that purpose rather
than replace it. The compiled framework is the wiki folder `framework/` of
the operations project below — start with `framework/README.md`, then
`framework/VOCABULARY.md`; `SCHEMA.md`, `VISUALIZATION.md` and `CHANGELOG.md`
complete it.

## What Chaos House is

Chaos House is the maintainer's self-hosted orchestrator that runs APS
systems: projects declared by problem, strategy, verification and process
pages; work performed in typed sessions; durable knowledge in a wiki; an
append-only timeline. Reach the instance through the `chaos-house` MCP
server declared in `.mcp.json` (HTTP over the maintainer's Tailscale
network, `http://100.121.4.25:4321/mcp`). If its tools are unavailable, say
so and ask the maintainer to approve the project MCP server or check
connectivity — do not fall back to answering from local files.

## The operations project

Since 2026-08-17 the APS Framework Operations system is the Chaos House
project `aps-framework-operations` (key `APS`). Framework documents,
problems, tasks, sessions, streams and the timeline are canonical there;
this repository is the backup projection Chaos House pushes back.

- `processes/process.md` — the operating loop every piece of work follows
- `processes/README.md` — index of the other processes and of the session
  types (`brainstorming`, `grooming`, `aps-intake`, `aps-dogfooding`,
  `retrospective`)

Read wiki pages with `read_wiki_file` as `aps-framework-operations/<path>`.

## How to work here

- **Read current state live.** Answer questions about problems, tasks,
  sessions or the framework from the MCP tools (`get_board_overview`,
  `get_project`, `list_tasks`, `get_task`, `list_sessions`, `list_timeline`,
  `read_wiki_file`), never from `project-export/` — the export lags canonical
  state whenever the backup is pending or failing.
- **Work in sessions, per `process.md` steps 4 and 8.** Start the typed
  session before the work — infer the type from the maintainer's request or
  ask — and announce its key. Bind every action to it. When the work seems
  finished, ask whether to close; close only on the maintainer's go, and
  only a session you started in this conversation.
- **Edit framework documents in the wiki.** The normative framework lives
  at `framework/…`; processes under `processes/…`. Use the wiki tools with
  their SHA-guarded edit calls and the session id.
- **Ask in plain text.** Never call `AskUserQuestion` or any equivalent
  structured multiple-choice prompt. When a routine call can be made with a
  stated assumption, make it and say so.
- **No agent attribution in git.** Commits, PR titles and PR bodies carry
  no `Co-Authored-By`, "Generated with", or other agent notes; the session
  record is the attribution.

## This repository

- `project-export/` is machine-written by the Chaos House repository
  backup, which pushes snapshots to `main` (fast-forward only). Never
  hand-edit it and never rewrite `main` history; both break the exporter's
  integrity guard. Manual commits to `main` outside `project-export/` are
  possible but should stay rare and deliberate.
- `framework/` and `operations/` are the pre-migration repository capsule,
  kept as history. They are stale: the current framework text is the wiki
  projection under `project-export/wiki/framework/`. Do not extend or edit
  the legacy trees.
- Branch `chaos-house-backup` preserves the pre-migration `main`
  (`43b9f69`, 2026-08-07) and is frozen.
