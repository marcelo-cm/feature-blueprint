# Routing Rules

Use these rules when a finding may belong somewhere other than the current artifact.

## Artifact Ownership

- Product semantics, examples, and decisions belong in the design doc.
- Implementation shape and execution order belong in the feature scoping doc.
- Standalone refactors and bug fixes belong in the pre-work scoping doc.
- Copy/paste ticket content belongs in Linear templates after scoping is complete.
- Implementation startup instructions should point to the approved source docs; do not create a separate hand-off artifact.

## Upstream Gaps

If scoping reveals a design contradiction, stop and surface it upstream. Do not patch the scoping doc around an unstable design decision.

If implementation planning reveals missing pre-work, evaluate it through the prep-work loop. Do not silently fold it into the feature plan.

## Locked Decisions

When a locked decision resurfaces:

1. Restate the existing decision.
2. Explain what new evidence challenges it.
3. Ask whether the owner wants to re-open it.
4. Wait for explicit approval before changing downstream artifacts.

## Linear Timing

Do not create or draft final Linear ticket bodies until scoping is complete. Working docs come first.
