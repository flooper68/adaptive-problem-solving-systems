# Grooming

Groom captured inputs, tasks, problems, verification evidence, and session lessons into one approved disposition per item, guided by the system strategy. Exact problem-state history lives in the ordinary project-owned [problem state log](../../records/problem-state-log.md); signal definitions remain in Verification and latest meaning remains in Current state.

Groom on maintainer request, before substantial work selection, when new evidence accumulates, when a dependency resolves, when verification cannot read a signal, when an item blocks a consumer, or after every third completed working session since the last grooming invocation.

For each item:

1. Orient to its authoritative Chaos House entity and linked evidence.
2. Clarify the claim, scope, current state, uncertainty, and relationship to problems and strategy.
3. Challenge duplication, unsupported inference, stale state, and premature work creation. Evidence never creates work without a separate approved disposition.
4. Propose one disposition: act, revise, keep with a reconsideration trigger, merge/link, or close with reason.
5. Present the exact canonical mutations and obtain owner approval. Apply approved actions session-bound; silence never authorizes them. Append approved readings and assessments to the ordinary project log with optimistic `append_wiki_file`; project a root judgement to project health with `save_project`, and leave health unset when no root judgement exists. Neither the log path nor its entries have product-level semantics.
6. Preserve provenance in both directions where the action model supports it, and state any normalization that remains only in content.
7. Reconfirm P1 signal state and selected next work at the end of a full invocation.

An invocation is complete when every item in scope has an approved recorded disposition, propagation is recoverable, and missing answers have evidence requests or next triggers.
