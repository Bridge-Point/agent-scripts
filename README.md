# Agent Scripts

Shared agent guardrails, skills, and helper scripts. Forked from [@steipete's agent-scripts](https://github.com/steipete/agent-scripts) and adapted for Nick Kemp's environment.

## Pointer-Style AGENTS
- Shared guardrail text lives in this repo: `AGENTS.MD` (shared rules + tool list).
- Every consuming repo's `AGENTS.MD` is reduced to the pointer line `READ ~/GitHub/agent-scripts/AGENTS.MD BEFORE ANYTHING (skip if missing).` Place repo-specific rules **after** that line if they're truly needed.
- Do **not** copy the shared blocks into other repos. Instead, keep this repo updated and have downstream workspaces re-read `AGENTS.MD` when starting work.

## Syncing With Other Repos
- Treat this repo as the canonical mirror for shared guardrail helpers.
- When someone says "sync agent scripts," pull the latest changes here, ensure downstream repos have the pointer-style `AGENTS.MD`, and reconcile differences before moving on.
- Keep every file dependency-free and portable: scripts must run in isolation across repos.

## Skills
Reusable skill definitions live in `skills/`. Each has a `SKILL.md` with instructions and optional `references/` and `scripts/` dirs.

## Slash Commands
Repo-local slash command docs live in `docs/slash-commands/`.
