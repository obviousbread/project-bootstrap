# AGENTS-dot-md

![AGENTS.md — drop-in operating instructions for coding agents](assets/feature.webp)

A drop-in [`AGENTS.md`](AGENTS.md) — operating instructions for coding agents. Read once, fill in the project section, prune over time.

## Deploy

When asked to deploy / install this `AGENTS.md` into a repo, follow these steps exactly. This procedure is the single source of truth for the bootstrap — it is self-contained, so a pointer to it is all an agent needs. Confirm each step before acting.

1. **Fetch** the raw `AGENTS.md` from this repo to a temp path, then copy it into the target repo root. Don't clone the repo into the project. The fetched file is the only allowed source — never author it from memory or a template. If the fetch fails, STOP and ask.
2. **Create `CLAUDE.md`** at the repo root as a real file whose only content is `@AGENTS.md` (a pointer, not a symlink). Other AGENTS.md-native tools (Codex, Cursor, Windsurf, Copilot, Aider, Devin, Amp) need nothing extra.
3. **Fill section 10 (Project context)** with concrete values read from the repo: stack, package manager, build/test/lint/run commands, source and test layout, repo-specific conventions. Delete subsections that don't apply — no `TODO` placeholders left behind.
4. **Leave section 11 (Project Learnings) empty.** It grows from real corrections, not guesses.
5. **Touch nothing else.** Sections 0–9 are intentionally generic; do not edit them.
6. **Verify:** diff the deployed file against the fetched temp source. The only difference should be section 10. If anything else differs, discard and redo.

Raw file: `https://raw.githubusercontent.com/obviousbread/AGENTS-dot-md/main/AGENTS.md`

## What's in it

- Non-negotiables: no flattery, no fabrication, stop when confused.
- Plan before code; match existing patterns; surface assumptions.
- Simplicity first; surgical diffs; verify with running code, not plausibility.
- Direct communication; ask only when ambiguity materially changes the output.
- Self-improvement loop to keep the file honest (~100 lines, ceiling ~300).

## Credit

This boilerplate synthesizes:

- Sean Donahoe's IJFW ("It Just F\*cking Works") principles: one install, working code, no ceremony.
- Andrej Karpathy's observations on LLM coding pitfalls (think-first, simplicity, surgical changes, goal-driven execution).
- Boris Cherny's public Claude Code workflow (reactive pruning, keep it ~100 lines, only rules that fix real mistakes).
- Anthropic's official Claude Code best practices (explore-plan-code-commit, verification loops, context as the scarce resource).
- Community anti-sycophancy patterns (explicit banned phrases, direct-not-diplomatic).
- The [AGENTS.md](https://agents.md) open standard (Linux Foundation / Agentic AI Foundation) for cross-tool portability.
