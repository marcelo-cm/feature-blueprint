# Anti-Patterns

Avoid these process failures.

## Proposing Without Reading

Do not claim a call-site count, clean swap, or simple refactor before reading the relevant files.

## Writing Code During Scoping

This methodology produces artifacts. Implementation happens separately.

## Collapsing Artifacts

Do not combine design doc, technical scoping, pre-work scoping, and Linear tickets into one artifact.

## Separate Hand-Off Artifact

Do not create a separate implementation hand-off prompt. The approved design and scoping docs should be detailed enough for implementation startup.

## Ticket-First Planning

Do not start with Linear tickets. Working docs are the source of truth; tickets are packaged after scoping is complete.

## Re-Litigating Locked Decisions

If a decision is locked, do not revise it silently. Surface new evidence and ask whether to re-open it.

## Batch Drafting

Do not write many unrelated sections before feedback. Stage-gate authoring to catch drift early.

## Over-Including Prep Work

Prep work must pass all three gates. Cosmetic cleanup does not qualify.

## Pseudocode Creep

Interface-level snippets should not grow into pseudo-implementations unless implementation-ready depth was explicitly selected.

## Weak Out-Of-Scope

If non-goals are vague, scope will expand during implementation. Make out-of-scope explicit.
