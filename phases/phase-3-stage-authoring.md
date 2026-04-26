# Phase 3: Stage-By-Stage Authoring

Phase 3 writes the scoping document one section at a time.

## Phase Contract

- Entry condition: owner approved the Phase 2 outline, depth choices, out-of-scope list, and pre-work status.
- Allowed actions: research current code, draft approved sections, edit the scoping doc directly, and evaluate prep-work candidates.
- Not allowed: drafting unrelated sections ahead, changing locked design decisions, or folding standalone prep work into the feature plan without evaluation.
- Output: one approved section or a small batch of tightly related sections.
- Approval needed: owner signals continue, revise, next section, or escalate after each checkpoint.

## Goal

Produce a technical scoping working doc that is implementation-ready at the selected depth without relitigating design decisions.

## Per-Section Loop

For each section:

1. Research first.
   - Read files, follow call chains, inspect current behavior.
   - Do not describe code you have not checked.

2. Verify citations.
   - Every code reference must come from a direct file read.
   - Search output alone is not enough.
   - Use file or symbol references by default; use line references when they materially help implementation.

3. Draft the section.
   - Use the locked outline and selected depth.
   - Prefer tables for inventories and migrations.
   - Use Mermaid only when it clarifies flow.

4. Pause with a summary.
   - What research confirmed.
   - What contradicted the outline.
   - Decisions needed before continuing.
   - Prep-work candidates surfaced.

5. Wait for signal.
   - Continue, revise, next section, or escalate.

Strict mode is the default. Condensed mode is allowed only when the owner opts in; in condensed mode, draft at most one small batch of tightly related sections before stopping. Treat sections as tightly related only when they share the same research path and approval decision, such as backend interface plus data migration for the same persistence change.

## Revision Rule

Revise sections in place. Do not append "v2" addenda.

If a requested revision changes a locked design decision, stop and ask the owner to re-lock the decision before editing.

If research contradicts the approved outline:

- Design semantics changed or contradicted: return to Phase 0 or Phase 1.
- Technical structure or depth is wrong: return to Phase 2.
- Standalone refactor or bug fix surfaced: run the prep-work loop.
- New technical question within the locked scope: add it to the scoping doc's new open questions and pause if it blocks the current section.
- Minor section-level detail changed: revise the section and call out the change at the checkpoint.

## Prep-Work Checks

At each research point, ask whether a standalone refactor or bug fix would shrink the feature PR. If yes, read `loops/prep-work-loop.md`.

## Stop Condition

Stop after each section or small batch of tightly related sections in condensed mode.

Do not draft ahead across unrelated sections without owner signal.
