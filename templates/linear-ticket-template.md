# Linear Ticket Templates

Use these only after scoping is complete. Draft ticket content from the working documents for copy/paste into Linear.

## Parent Pre-Work Ticket

Title:

```text
[PREP] <theme>
```

Body:

```markdown
# Why pre-work - how it relates to the feature design

<2-5 concise paragraphs explaining feature context, why current code shape makes the feature harder, and why these prep tasks are independently valuable.>

## Execution order

1. **PREP-1** first - <why first>.
2. **PREP-2** second - <why second>.
3. **PREP-N** last - <parallelization, optionality, or dependency notes>.

<Short paragraph describing independence, merge order, and which tasks can be skipped or folded into feature work if needed.>

## Out of scope

Explicitly not in pre-work - these are feature work:

- <Out-of-scope item>
- <Out-of-scope item>
- <Out-of-scope item>
```

## Child Pre-Work Ticket

Title:

```text
[PREP-#] <specific task>
```

Body:

```markdown
## <N>. PREP-# - <specific task>

### <N>.1 Goal

<2-4 concise paragraphs explaining the problem, why it matters now, and why this is valid pre-work.>

### <N>.2 Current State / Gaps

Use a table when there are multiple call sites, behaviors, or differences.

| Site | Today | After PREP-# |
|---|---|---|
| `<file>` or `<file:symbol>` | <current behavior> | <target behavior> |

### <N>.3 Proposed Shape

<Concise structural change. Include interface-level snippets only if needed.>

### <N>.4 What PREP-# Does NOT Touch

- <Feature work excluded from this prep>
- <Semantic changes excluded from this prep>
- <Risky or unrelated cleanup excluded from this prep>

### <N>.5 Test Expectations

- <Behavior or parity to test>
- <Important parameterization or regression coverage>

### <N>.6 Safe To Ship Alone

<One paragraph proving independent value, feature-PR shrinkage, and standalone safety.>

### <N>.7 Risk / Ordering Notes

<Optional. Include only if risk or ordering materially affects execution.>
```

## Feature Implementation Ticket

Title:

```text
<Feature name>
```

Body:

```markdown
## Summary

<Engineering-leader-readable summary of the feature and technical implications.>

## Technical implications

- <Major backend/frontend/data/rollout implication>
- <Major risk or dependency>

## Pre-work

References parent pre-work ticket: <ticket>.

## Source of truth

- Design doc: <path>
- Technical scoping doc: <path>
- Pre-work scoping doc: <path or none>
```
