# AGENTS-dot-md

A drop-in [`AGENTS.md`](AGENTS.md) — operating instructions for coding agents.

## How to use

Open your coding agent in the repo where you want `AGENTS.md` installed and paste this prompt:

```text
Fetch AGENTS.md from https://github.com/obviousbread/AGENTS-dot-md and install it at the root of this repo.

Then adapt it to this project:
1. Read the codebase enough to understand the stack, package manager, build/test/lint commands, source and test layout, and any repo-specific conventions.
2. Fill in section 10 (Project context) with concrete values. Delete subsections that don't apply. No TODO placeholders left behind.
3. Leave section 11 (Project Learnings) empty — it grows from real corrections, not guesses.
4. Do not edit sections 0–9 or 12. They are intentionally generic.
5. For tools that don't read AGENTS.md natively, create symlinks: `ln -s AGENTS.md CLAUDE.md`, `ln -s AGENTS.md GEMINI.md`.
6. Show me the filled-in section 10 as a diff before committing.
```

The agent will read your repo, fill in the project-specific section, and leave the rest alone.

## What's in it

- Non-negotiables: no flattery, no fabrication, stop when confused.
- Plan before code; match existing patterns; surface assumptions.
- Simplicity first; surgical diffs; verify with running code, not plausibility.
- Direct communication; ask only when ambiguity materially changes the output.
- Self-improvement loop to keep the file honest (~100 lines, ceiling ~300).

## Credit

Synthesizes Sean Donahoe's IJFW principles, Karpathy's LLM coding observations, Boris Cherny's Claude Code workflow, Anthropic's best practices, and community anti-sycophancy patterns.
