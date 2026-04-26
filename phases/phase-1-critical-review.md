# Phase 1: Critical Review

Phase 1 reviews the design doc adversarially before technical scoping begins.

## Phase Contract

- Entry condition: Phase 0 design doc is explicitly accepted for critical review.
- Allowed actions: read the design doc, verify claims against code, produce findings, and surgically edit the design doc after owner triage.
- Not allowed: resolving findings without owner triage, starting technical scoping, or changing locked decisions silently.
- Output: numbered findings, followed by triaged design-doc edits and rejected-finding rationale.
- Approval needed: owner confirms findings are triaged, rejected-finding rationale is captured in the design doc, accepted/refined edits are made, and the design is locked for scoping before Phase 2.

## Goal

Find contradictions, gaps, hidden migrations, edge cases, and places where current code may fight the proposal.

Do not fix findings silently. The design owner triages them.

## Mechanics

1. Read the design doc end to end.
2. Verify code claims by reading current code when needed.
3. Produce numbered findings only. Do not include proposed fixes unless the finding needs a concrete example to be understandable.
4. Present findings without resolving them.
5. Owner triages each finding:
   - accept: edit the design doc,
   - reject: document in the design doc why it is not a concern,
   - refine: rework the proposal.
6. Apply only accepted or refined changes with targeted edits to the existing design doc.
7. Add rejected-finding rationale to the design doc, preferably near the relevant decision, trade-off, or open-question section.

If a finding is minor copy or structure cleanup, label it as non-blocking. If it can change semantics, rollout, data behavior, or implementation scope, treat it as blocking until triaged.

## What To Look For

- Composition rules that fail edge cases.
- Storage semantics that contradict existing code.
- Data migrations hidden behind "no schema changes."
- UI claims that imply backend complexity.
- Decisions whose cost is stated without contrast.
- Open questions without a named resolution phase.
- Deferred work that is actually required for correctness.

## Finding Format

Use a numbered list:

```markdown
1. **Finding title**
   - Concern: <what may be wrong>
   - Evidence: <doc section and/or verified file reference>
   - Why it matters: <impact if unresolved>
   - Severity: <blocking/non-blocking>
   - Needs owner decision: <yes/no and question>
```

## Stop Condition

Stop after delivering the findings list and asking the owner to triage each item.

Do not move to Phase 2 until triage outcomes are reflected in the design doc and the owner explicitly locks the design for scoping.
