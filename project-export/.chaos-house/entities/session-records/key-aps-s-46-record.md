---
entity:
  identity:
    type: slug
    value: key-aps-s-46-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-21T09:31:42.312Z
  outcome: completed
  session: session:key:APS-S-46
---

Brainstorming session on agent onboarding clarity (problem APS-P-2). Participants: maintainer, interactive agent.

Findings: AGENTS.md (CLAUDE.md symlink) explained neither Chaos House nor linked the framework compilation and operations processes; the APS wiki had no interactive-session lifecycle guidance (Chaos House has processes/interactive-sessions.md); session start and close are prose-driven — no hooks, no MCP server instructions.

Decisions: fold the interactive entry and the explicit close question into processes/process.md steps 4 and 8 instead of adding a page; rewrite AGENTS.md as what-is-APS / what-is-Chaos-House / operations project / how-to-work / this-repository; rule that commits and PRs carry no agent attribution trailers; force-push approved to strip existing trailers.

Changes: wiki aps-framework-operations/processes/process.md (steps 4, 8; final sha 706d7e92). Repo: AGENTS.md rewritten; commits above 7b8e0c5 rewritten without Co-Authored-By (d1bf9a6, e8ac9b4, 2b3c64a); origin/main = 2b3c64a; 7b8e0c5 remains ancestor so the exporter ancestry guard holds.

Expected effect of the process edit by next retrospective: interactive sessions whose first mutating action precedes start_session → 0; APS work left with no session → 0; sessions closed by a non-opener conversation → 0.

Validation: wiki edits SHA-guarded and session-bound; merge-base --is-ancestor verified before push.

Friction / open items: repository backup failing since 2026-08-17 — committed manifest is Projection V1, exporter accepts V2 only; needs Chaos House-side migration (not filed). The no-attribution rule is not yet mirrored in the Chaos House repo AGENTS.md. This session itself started after orientation reads — the very gap step 4 now closes.
