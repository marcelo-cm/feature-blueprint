---
name: feature-blueprint
description: Turns feature ideas and design docs into reviewed, phase-gated, implementation-ready scopes using Marcelo's methodology. Use when the user asks for feature scoping, design-doc readiness, critical review, prep-work planning, or Linear-ready ticket packaging.
metadata:
  author: "marcelo-cm"
  version: "0.1.0"
---

# Feature Blueprint

Use this skill only when explicitly invoked. Do not apply this workflow to ordinary implementation requests.

## Operating Mode

This skill is a router. Read only the file needed for the current phase plus any cross-cutting reference needed for the immediate task.

Core rules:

- Do not write or edit implementation code during this methodology.
- When working-document paths are available, edit those docs directly.
- Draft the smallest useful change, then surgically edit the existing artifact. Do not rewrite whole docs unless the owner explicitly asks for a replacement.
- Ask questions until requirements, decisions, scope, and artifact targets are clear.
- Work phase by phase, with explicit owner approval before advancing. Condensed mode is opt-in only.
- Research before proposing technical shape.
- Treat locked decisions as locked; do not silently revise them.
- Surface upstream gaps upstream instead of absorbing them into downstream artifacts.
- Keep artifacts separated by purpose.
- Prefer concise structure: numbered workflows, bullets for scope, tables for inventories/comparisons, and Mermaid diagrams for flows when useful.

## Phase States

Use these state names when asking for approval or deciding whether to advance:

1. Design draft: Phase 0 is still gathering semantics and examples.
2. Accepted for critical review: Phase 0 is complete enough for adversarial review, but decisions are not final for scoping.
3. Reviewed and locked for scoping: Phase 1 findings are triaged, design-doc edits are made, and the owner accepts the design for Phase 2.
4. Outline locked: Phase 2 outline, depth, out-of-scope list, and prep-work status are approved.
5. Section approved: a Phase 3 section or small related batch is accepted.
6. Specs approved: design, feature scoping, and pre-work scoping docs are accepted for ticket packaging.

## Working Documents And Tickets

The design doc, review findings, pre-work scoping doc, and feature scoping doc are working artifacts. They are the source of truth.

Linear tickets are packaged only after scoping is complete. Draft ticket content from the working documents, but do not create large Linear tickets directly through MCP unless the owner explicitly asks.

Default Linear split:

- Pre-work parent ticket: `[PREP] <theme>`, with context, why pre-work matters, relation to the feature, execution order, and out-of-scope.
- Pre-work child tickets: `[PREP-#] <task>`, one per accepted prep task, numbered from `[PREP-1]` per feature.
- Feature implementation ticket: separate from pre-work, references the pre-work parent ticket, and summarizes the feature plus technical implications for engineering leaders.

## Phase Order

1. Phase 0: design-doc readiness for critical review. Read `phases/phase-0-design-doc.md`.
2. Phase 1: critical review of the design doc. Read `phases/phase-1-critical-review.md`.
3. Phase 2: outline locking and depth calibration. Read `phases/phase-2-outline-locking.md`.
4. Phase 3: stage-by-stage authoring. Read `phases/phase-3-stage-authoring.md`.
5. Optional Phase 4: Linear ticket packaging after specs are approved. Read `phases/phase-4-linear-ticket-packaging.md`.

## Cross-Cutting Files

Read these only when relevant:

- `loops/prep-work-loop.md`: when standalone prep/refactor/bug-fix candidates surface.
- `reference/routing-rules.md`: when a finding may belong in a different artifact or phase.
- `reference/conventions.md`: when drafting artifacts or citing code.
- `reference/signals.md`: when scope, evidence, or decisions appear to drift.
- `reference/anti-patterns.md`: when reviewing the process or checking for methodology drift.
- `templates/linear-ticket-template.md`: when packaging completed specs into Linear ticket content.
- `templates/design-doc-template.md`: when creating or checking the design doc shape.
- `templates/feature-scoping-template.md`: when locking or drafting the feature scoping doc.
- `templates/pre-work-scoping-template.md`: when accepted prep candidates require a working doc.

## Depth Calibration

During Phase 2, ask what depth is needed for each implementation surface before locking the outline.

Depth options:

- `none`: no work expected on that surface.
- `goals`: behavior-level goals and affected areas only.
- `interface`: files, call paths, component/hook/service boundaries, method signatures, execution order.
- `implementation-ready`: enough detail for a direct implementation pass.

Apply depth independently for backend, frontend, data/modeling, infrastructure, analytics, testing, and rollout when relevant. Do not assume backend should be deep or frontend should be shallow.

## First Response When Invoked

If the user invokes this skill without enough context, ask for:

1. The feature/design artifact to scope from.
2. Current phase state: design draft, accepted for critical review, reviewed and locked for scoping, outline locked, section approved, or specs approved.
3. Desired output: design doc, scoping doc, pre-work plan, Linear ticket drafts, or full sequence.
4. Depth needed for backend and frontend if already known.
5. Whether to opt into condensed mode. Default to strict phase-by-phase mode.

Then begin with the appropriate phase file. Do not start writing the final artifact until the current phase's stop condition is satisfied.
