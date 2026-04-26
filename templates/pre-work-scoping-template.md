# Pre-Work Scoping Template

Use only when at least one prep candidate passes the three-gate filter.

```markdown
# <Feature Name> Pre-Work Scoping

## 0. Purpose

<Explain that these refactors or bug fixes ship before the feature PR. Each is independently valuable, safe to ship alone, and shrinks the feature PR.>

## 1. Shared Inventory

| Code reference | What exists today | Prep relevance |
|---|---|---|
| `<file>` or `<file:symbol>` | <current behavior> | <why prep touches it> |

## 2. PREP-1 - <Task Name>

### 2.1 Goal

<What this prep task changes and why it matters.>

### 2.2 Current State / Gaps

| Site | Today | After PREP-1 |
|---|---|---|
| `<file>` or `<file:symbol>` | <current behavior> | <target behavior> |

### 2.3 Proposed Shape

<Interface-level shape or concise structural description.>

### 2.4 What PREP-1 Does NOT Touch

- <Feature work excluded>
- <Unrelated cleanup excluded>

### 2.5 Test Expectations

- <Parity or regression coverage>
- <Important parameterization>

### 2.6 Safe To Ship Alone

<Prove independent value, feature-PR shrinkage, and standalone safety.>

## N. Execution Order

1. **PREP-1** first - <why>.
2. **PREP-2** second - <why>.

## N+1. Out Of Scope

- <Feature work not included in pre-work>
```
