# Prep-Work Loop

The prep-work loop runs across all phases. It identifies standalone refactors or bug fixes that should ship before the feature PR.

## Trigger Question

Ask during design review, outline locking, each authoring section, and late scoping discoveries:

> Is there a standalone refactor or bug fix in the surrounding code that would shrink the feature PR and is independently shippable?

## Three-Gate Filter

A candidate becomes prep work only if all three are true:

1. Independently valuable.
   - Correct even if the feature never ships.

2. Measurably shrinks the feature PR.
   - You can point to the feature scoping doc and show what becomes simpler.

3. Safe to ship alone.
   - No coordinated feature release.
   - No required feature flag.
   - No risky migration unless explicitly idempotent and reversible.

If any gate fails, it is not prep work.

## Candidate Statuses

Track candidates with one status:

- Proposed: surfaced but not evaluated; common in Phase 2 before section-level research.
- Pending research: needs Phase 3 code research before the three-gate filter can be applied.
- Accepted: passed all three gates.
- Rejected: failed a gate; record why.
- Promoted to feature: belongs in the feature PR.
- Promoted to design: exposes a design gap and must go upstream.

## Pre-Work Working Doc

Create a pre-work scoping doc only when at least one candidate is accepted.

The doc should be detailed enough to copy into Linear later, but Linear tickets are created only after scoping is complete.

When a pre-work doc already exists, edit it surgically:

- add new accepted candidates in numbered order,
- update only affected candidate sections,
- preserve rejected/promoted rationale,
- do not rewrite the full doc for style.

## Freeze Point

Prep enumeration freezes when either:

- Phase 3 is complete and the final two section checkpoints surfaced no new prep candidates,
- or the owner explicitly freezes prep scope.

New candidates after freeze go into follow-up work unless the owner re-opens prep scoping.
