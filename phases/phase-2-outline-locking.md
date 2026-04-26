# Phase 2: Outline Locking

Phase 2 locks the technical scoping outline before drafting prose.

## Phase Contract

- Entry condition: design doc is reviewed and locked for scoping.
- Allowed actions: read code for scope discovery, propose the scoping-doc outline, calibrate depth, identify prep-work candidates, and edit the scoping doc outline when a path exists.
- Not allowed: drafting full sections before the outline is approved, resolving design gaps downstream, or packaging Linear tickets.
- Output: proposed outline, deviations, depth by surface, answered clarifying questions, out-of-scope list, and pre-work status.
- Approval needed: owner approves the outline and depth choices before Phase 3.

## Goal

Agree on structure, scope, depth, deviations, and open questions so Phase 3 can author one section at a time without drifting. Before owner approval, call this the proposed outline; after approval, call it the locked outline.

## Mechanics

1. Start from `templates/feature-scoping-template.md`.
2. Propose deviations with reasons.
3. Calibrate depth per implementation surface. If the owner has not already chosen depth, ask; do not infer it.
4. Ask clarifying questions as a numbered list.
5. List explicit out-of-scope items.
6. Capture prep-work status as none needed, candidates pending research, or pre-work doc required.

## Depth Calibration

Ask for depth independently by surface:

| Surface | Depth options |
|---|---|
| Backend | `none`, `goals`, `interface`, `implementation-ready` |
| Frontend | `none`, `goals`, `interface`, `implementation-ready` |
| Data/modeling | `none`, `goals`, `interface`, `implementation-ready` |
| Infrastructure | `none`, `goals`, `interface`, `implementation-ready` |
| Analytics/audit | `none`, `goals`, `interface`, `implementation-ready` |
| Testing | `none`, `goals`, `interface`, `implementation-ready` |
| Rollout | `none`, `goals`, `interface`, `implementation-ready` |

Do not assume backend is deep or frontend is shallow. The selected depth controls section shape and citation expectations.

Depth meanings:

- `none`: explicitly out of scope except for cross-references.
- `goals`: desired behavior and affected areas, without file or interface commitments.
- `interface`: files, call paths, component/hook/service boundaries, method signatures, and execution order.
- `implementation-ready`: interface depth plus enough edge cases, test targets, and migration detail for a direct implementation pass.

## Clarifying Questions

Ask questions until scope is clear. Prefer numbered questions with concise context:

```markdown
1. Should frontend scoping stop at user-facing behavior, or include route/component/query boundaries?
2. Should the rollout section include deploy-unit splitting, or only ordering constraints?
3. Is this behavior a locked design decision or still open for scoping?
```

## Stop Condition

Stop after producing:

- proposed outline ready for approval,
- deviations and reasons,
- depth choices by surface,
- clarifying questions and answers,
- explicit out-of-scope list,
- pre-work status: none needed, candidates pending research, or pre-work doc required.

Wait for owner approval before treating the outline as locked or drafting Phase 3 sections.

Preferred output shape:

1. Proposed outline with section names and one-line intent.
2. Deviations from `templates/feature-scoping-template.md`, with reasons.
3. Depth table by surface.
4. Numbered clarifying questions or recorded answers.
5. Out-of-scope list.
6. Pre-work status.
