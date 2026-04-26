# Phase 4: Linear Ticket Packaging

Phase 4 is optional. It packages approved working docs into Linear-ready ticket content after scoping is complete.

## Phase Contract

- Entry condition: design doc, pre-work scoping doc if any, and feature scoping doc are approved.
- Allowed actions: read approved working docs, draft copy/paste ticket bodies, and create tickets only when the owner explicitly asks.
- Not allowed: changing scope, reopening decisions, adding new implementation detail, or using Linear tickets as the source of truth.
- Output: Linear-ready parent prep, child prep, and feature ticket drafts as needed.
- Approval needed: owner confirms ticket drafts are accurate before any MCP ticket creation.

## Goal

Turn the completed specs into reviewable execution tickets without weakening the working docs as the source of truth.

## Mechanics

1. Read `templates/linear-ticket-template.md`.
2. Read the approved working docs.
3. Identify which tickets are needed:
   - pre-work parent ticket,
   - pre-work child tickets,
   - feature implementation ticket.
4. Draft ticket content from the working docs.
5. Keep ticket bodies concise and link back to the source docs.
6. Ask for owner approval before creating tickets through Linear MCP.

## Source Rules

- Design semantics come from the design doc.
- Prep task scope comes from the pre-work scoping doc.
- Implementation order and technical implications come from the feature scoping doc.
- If the docs conflict, stop and ask which source should be corrected. Do not resolve conflicts inside the ticket body.

## Stop Condition

Stop after producing Linear-ready drafts or, if explicitly requested, after creating the approved tickets.
