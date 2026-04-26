# Conventions

## Writing Style

Prefer concise, structured artifacts:

- Numbered lists for ordered workflows, phases, execution order, and decisions.
- Bulleted lists for grouped facts, requirements, scope, and non-goals.
- Tables for inventories, migrations, comparisons, state matrices, and gap lists.
- Mermaid diagrams for data or control flows when they improve understanding.

Every sentence should be clear and useful. Cut filler, repeated rationale, vague qualifiers, and prose that does not change the reader's understanding or next action.

## Code References

Use references precise enough for an implementer to find the code again:

- `path/to/file.py`
- `path/to/file.py:function_or_symbol`
- `path/to/file.py:LINE` or `path/to/file.py:START-END` when line precision materially helps

Every code reference must be verified by direct file read before citing. Search output alone is not enough. Prefer durable file or symbol references unless implementation-ready depth needs line-level precision.

## Code Snippets

Default ceiling is interface-level:

- class or function signature,
- parameters and return type when relevant,
- one-line responsibility.

Only include implementation-level snippets when the owner explicitly selected implementation-ready depth.

## Cross-References

Cross-reference working docs instead of duplicating content.

Use phrases like:

- "see design section X",
- "see pre-work section Y",
- "see technical scoping section Z".

## Testing Sections

Name what to test and what parameterization matters.

Avoid test file paths unless the selected depth is implementation-ready and the owner asked for that level of detail.

## Diagrams

Use Mermaid for flows, not decoration. Every node should represent a real actor, state, code path, or artifact.
