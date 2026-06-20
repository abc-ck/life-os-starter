---
type: note
created: 2026-06-20
reviewed: 2026-06-20
status: living
authority: canon
source: ai
---

# prompt 4 — private Git setup

**Bottom line:** Creates safe local version history and an optional private remote only after auditing the exact tracked snapshot.

**When to read this:** Use after personalization and acceptance testing are clean.

```text
Set up safe version control for this vault.

Before staging or creating a remote:
- Read the privacy and Git decisions in os/me.md, os/agent-rules.md, and
  os/vault-map.md.
- Inspect .gitignore and every candidate tracked file.
- Exclude local Obsidian/agent state, trash, credentials, secrets, temporary
  attachments, large generated files, and independently versioned nested repos.
- Scan candidate text for credential-shaped strings without printing secrets.
- Run ruby os/validate-life-os.rb.
- Explain in plain language exactly what will and will not be tracked.

If local Git is not initialized, initialize it only after the scope is clean.
If this starter already has Git history, preserve it and commit the personalized
system as a new checkpoint instead of replacing or rewriting history.
Create or push to a remote only if I explicitly approve it, and use a private
repository by default. Confirm local and remote commit IDs match.
```
