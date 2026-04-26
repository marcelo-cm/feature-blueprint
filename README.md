# Feature Blueprint

Feature Blueprint is an agent skill for turning feature ideas and design docs into reviewed, phase-gated, implementation-ready scopes using Marcelo's methodology.

## Install

Install from GitHub with the Skills CLI:

```bash
npx skills add marcelo-cm/feature-blueprint
```

To install globally instead of into the current project:

```bash
npx skills add marcelo-cm/feature-blueprint --global
```

To target Cursor explicitly:

```bash
npx skills add marcelo-cm/feature-blueprint --agent cursor
```

## Verify

List the skills available from this repo:

```bash
npx skills add marcelo-cm/feature-blueprint --list
```

The expected skill name is `feature-blueprint`.

## Repository Layout

This repo is a single-skill package. `SKILL.md` lives at the repository root, and the supporting phase guides, templates, and references live in direct subdirectories.

```text
.
├── SKILL.md
├── phases/
├── loops/
├── reference/
└── templates/
```

The Skills CLI supports this layout and discovers the root `SKILL.md` as `feature-blueprint`.
