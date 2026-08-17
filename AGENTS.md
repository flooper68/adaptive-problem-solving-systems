# Agent guidance

APS (Adaptive Problem Solving) is a framework for systems that solve
problems and improve how they solve them using evidence from real outcomes.
Artifacts, validation, learning, and adaptation support that purpose rather
than replace it.

## Source of truth: the Chaos House instance

Since 2026-08-17 the APS Framework Operations system lives in the maintainer's
Chaos House instance as project `aps-framework-operations` (key `APS`), not in
this repository. Framework documents, problems, tasks, sessions, streams, and
the timeline are all canonical there. This repository is the projection Chaos
House pushes back as a backup.

Reach the instance through the `chaos-house` MCP server declared in
`.mcp.json` (HTTP, over the maintainer's Tailscale network at
`http://100.121.4.25:4321/mcp`). If the tools are unavailable, say so and ask
the maintainer to approve the project MCP server or check connectivity —
do not fall back to answering from local files.

Rules that follow from this:

- **Read current state live.** Answer questions about problems, tasks,
  sessions, or the framework from the MCP tools (`get_board_overview`,
  `get_project`, `list_tasks`, `get_task`, `list_sessions`, `list_timeline`,
  `read_wiki_file`), never from `project-export/` — the export lags canonical
  state whenever the backup is pending or failing.
- **Work through sessions.** Perform APS work as typed work sessions:
  `start_session` pins the process to follow, `session_note` records material
  steps and decisions, `end_session` closes with the outcome and record. Task
  state changes go through the task tools; the maintainer approves
  completion.
- **Edit framework documents in the wiki.** The normative framework lives at
  wiki paths `framework/…` (README, VOCABULARY, SCHEMA, CHANGELOG,
  VISUALIZATION); processes live under `processes/…`. Use the wiki tools with
  their SHA-guarded edit calls.

## This repository

- `project-export/` is machine-written by the Chaos House repository backup,
  which pushes snapshots to `main` (fast-forward only). Never hand-edit it and
  never rewrite `main` history; both break the exporter's integrity guard.
  Manual commits to `main` outside `project-export/` are possible but should
  stay rare and deliberate.
- `framework/` and `operations/` are the pre-migration repository capsule,
  kept as history. They are stale: the current framework text is the wiki
  projection under `project-export/wiki/framework/`. Do not extend or edit the
  legacy trees.
- Branch `chaos-house-backup` preserves the pre-migration `main`
  (`43b9f69`, 2026-08-07) and is frozen.
