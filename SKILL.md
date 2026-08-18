---
name: project-bootstrap
description: Bootstrap a new development repository, add concise project-scoped agent instructions, or normalize an existing repository. Use when setting up a dev project or its AGENTS.md, README, Git basics, or minimal supporting configuration.
---

# Project bootstrap

Create the smallest useful repository configuration supported by verified
project facts. Preserve working configuration and do not scaffold speculative
process.

## Procedure

1. Inspect the repository, detected stack, documentation, commands, Git state,
   and existing configuration.
2. Infer facts from files. Ask only for decisions that cannot be discovered
   safely.
3. Match the requested scope: project rules only, new-project bootstrap, or
   existing-project normalization.
4. Create or update only applicable files. Do not replace working configuration
   merely to standardize it.
5. Run the smallest relevant verification and inspect the final diff.

## Default files

For a new project, create only what applies:

- `.gitignore` for the detected stack;
- `README.md` with verified setup and usage;
- `AGENTS.md` with project-specific facts and boundaries.

Initialize Git when the request includes creating a repository. Do not create a
remote, push, publish, or commit unless the user requests it or the surrounding
instructions clearly authorize it.

## Conditional files

Create only when justified:

- `.env.example` when the project actually uses environment variables;
- `LICENSE` when the user selects a license;
- CI when verified test or check commands exist;
- `CLAUDE.md` when Claude Code compatibility is required;
- one persistent spec when work must survive sessions or agents, or carries
  substantial product or operational risk.

Do not create `WORKFLOW.md`, `CHANGELOG.md`, planning directories, brainstorm or
plan templates, ADR directories, release configuration, branch protection, or
other process scaffolding by default.

## AGENTS.md

Keep `AGENTS.md` short and project-specific. Include only applicable sections:

```markdown
# AGENTS.md

## Project

One to three sentences describing the project and its current state.

## Commands

- Install: `<verified command>`
- Run: `<verified command>`
- Test: `<verified command>`
- Check: `<verified command>`

## Structure

- `<non-obvious path>` — `<purpose>`

## Boundaries

- `<security, generated-file, external-system, or destructive-action boundary>`

## Project-specific rules

- `<convention not evident from the codebase>`

## Gotchas

- `<verified failure mode and how to check it>`
```

Remove empty sections. Never teach general programming practices or duplicate
global, harness, or user instructions. Add a rule only when it records a real
project constraint, a non-obvious decision, or a verified failure mode.

## Workflow

Resolve material ambiguity in chat before implementation. For bounded,
reversible work, implement and verify directly.

Create one persistent spec only when the decision must outlive the current
context. Use a topic branch and draft pull request when a change is broad,
risky, difficult to review, or expected to span sessions. Do not require local
plan artifacts as ceremony.

## Completion

Report changed files, verified commands, unresolved decisions, and optional
infrastructure deliberately skipped.
