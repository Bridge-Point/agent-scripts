# Tools Reference

CLI tools available on Nick's machines. Use these for agentic tasks.

## gh
GitHub CLI for PRs, issues, CI, releases.

**Usage**: `gh help`

When someone shares a GitHub URL, use `gh` to read it:
```bash
gh issue view <url> --comments
gh pr view <url> --comments --files
gh run list / gh run view <id>
```

---

## trash
Move files to macOS Trash instead of permanently deleting.

**Usage**: `trash <file-or-dir> …`

---

## tailscale
VPN/mesh networking for reaching other machines.

**Usage**: `tailscale status` to list hosts/IPs.
