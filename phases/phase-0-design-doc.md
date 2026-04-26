# Phase 0: Design Doc

Phase 0 produces or validates the design doc. This phase answers what should happen, not how to implement it.

Do not write implementation code in this phase. Reading code to verify current behavior is allowed and often required.

## Phase Contract

- Entry condition: the owner has a feature idea, rough proposal, or existing design artifact.
- Allowed actions: ask product/design questions, read code to verify current behavior, query evidence when available, and edit the design doc directly when a path exists.
- Not allowed: implementation planning, ticket drafting, or code edits.
- Output: a ready-to-review design doc, readiness report, or numbered blocker questions.
- Approval needed: explicit owner signal that the design doc is accepted enough for critical review before Phase 1.

Keep technical details at the semantic boundary. Product-level persistence semantics, invariants, and trade-offs belong here when they affect product meaning or feasibility; file-level implementation shape, concrete migrations, and execution order belong in Phase 2 or Phase 3.

## Goal

Create or confirm a design doc ready for critical review with:

- product semantics,
- worked examples,
- decisions and rationale,
- composition rules,
- data model implications,
- trade-offs,
- open questions with named resolution phases,
- explicit out-of-scope items.

## Workflow

1. Content dump
   - Capture goals, business rationale, current conceptual state, expected conceptual changes, and relevant file references.
   - Do not structure too early. Establish vocabulary first.

2. Explore options
   - Name plausible solution shapes before choosing.
   - Include the unconstrained ideal before applying constraints.
   - Compare options on refactor size, migration cost, UX/domain implications, data-model complexity, reversibility, and forward-compatibility.

3. Refine and expand
   - Push on edge cases, production invariants, security, backwards compatibility, tier gates, and concrete examples.
   - Ask questions until every remaining ambiguity is either answered or explicitly deferred.
   - Query production data for frequency claims when available.

4. Choose and clarify
   - Lock each non-obvious decision with choice and rationale.
   - Move unresolved items into open questions with a named phase.
   - Confirm the owner treats the doc as stable enough for critical review.

5. Edit surgically
   - If a design doc path exists, patch only the affected sections.
   - Preserve existing decisions and wording unless the owner approved a change.
   - Do not replace the whole document to improve style.

## Required Sections

The design doc must include:

- Decisions table: `Decision | Choice | Why`.
- Worked examples with concrete inputs and outputs.
- Open questions, each with the phase that resolves it.
- Out-of-scope list.
- Follow-up work.

## Stop Condition

Stop after producing either:

- a ready-to-review design doc,
- a design-doc readiness report listing missing sections and questions,
- or a numbered set of design questions that must be answered before scoping.

Wait for owner signal that the design doc is accepted for critical review before moving to Phase 1.
