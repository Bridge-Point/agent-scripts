# Changelog

## 2026-02-22 — Adapt for Nick's Environment
- Rewrote `AGENTS.MD`, `tools.md`, and `README.md` for Nick Kemp's setup (`~/GitHub`, `pnpm`, VS Code).
- Removed all steipete-specific tools, paths, and references.
- Forked from [@steipete/agent-scripts](https://github.com/steipete/agent-scripts).

## 2025-12-22 — Remove Custom rm Shim
- Dropped `bin/rm` and `scripts/trash.ts`; rely on the system `trash` command for recoverable deletes.

## 2025-11-08 — Initial Toolkit Import
- Established the repo with shared guardrail toolkit (docs, slash commands, skills).
