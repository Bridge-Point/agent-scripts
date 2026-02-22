---
summary: 'Checklist for curating CHANGELOG.md from recent commits'
read_when:
  - Updating CHANGELOG.md or drafting release notes.
---
# Update CHANGELOG.md

Purpose: curate user-facing changes since the last release tag and record them in `CHANGELOG.md` (Unreleased section).

## Scope & Inputs
- Read the repo's `AGENTS.MD` first (and the repo-local release doc if it exists).
- Baseline version: use the provided baseline; otherwise the latest tag from `git describe --tags --abbrev=0`.
- Target file: the repo's `CHANGELOG.md`.

## Steps
1) **Pick baseline**
   - If none given: `git describe --tags --abbrev=0` → `<tag>`.
2) **Collect commits since baseline**
   ```bash
   git log <tag>..HEAD --oneline --reverse
   ```
   Skim the diff as needed to understand user-visible impact.
3) **Curate entries (user-facing only)**
   - Include: shipped features, fixes, breaking changes, notable UX or behavior tweaks.
   - Exclude: internal refactors, typo-only edits, dependency bumps without user impact, features added then removed in the same window.
   - Order by impact: breaking → features → fixes → misc.
   - Add PR/issue numbers when available (`#123`).
4) **Edit `CHANGELOG.md`**
   - Ensure there is an `## Unreleased` section at the top; create it if missing.
   - Append bullets under `Unreleased`; keep existing style (bullets, past-tense verbs or short descriptors, code in backticks).
5) **Sanity checks**
   - Markdown renders; no duplicate entries; wording concise.

## Quick format example
```markdown
## Unreleased
- Added configurable refresh interval. #123
- Fixed icon dimming on sleep/wake. #128
```
