---
summary: 'Slash commands overview and redirect to docs/slash-commands.'
read_when:
  - Editing or adding slash commands.
---
# Slash Commands

Moved to `docs/slash-commands/`. See `docs/slash-commands/README.md` for the index.

## Creating Commands

### Repo-Local (Claude Code)

Create markdown files in `.claude/commands/`:

```bash
mkdir -p .claude/commands
echo "# /mycommand\n\nYour prompt instructions..." > .claude/commands/mycommand.md
```

Use the command in any Claude Code session: `/mycommand`

### Shared Commands

This repo stores shared command docs in `docs/slash-commands/`.

## Best Practices

- **Be specific:** Include exact commands, safety checks, and exit conditions
- **Document constraints:** No destructive git, coordination rules, scope boundaries
- **Make them reusable:** Avoid task-specific details (dates, ticket numbers)
- **Test them:** Run the slash command to verify it works as expected
- **Version control:** Store project-specific commands in `.claude/commands/` (repo-local)
