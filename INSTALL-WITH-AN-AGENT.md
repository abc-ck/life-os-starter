---
type: note
created: 2026-06-20
reviewed: 2026-06-20
status: living
authority: reference
source: ai
---

# install with an agent

**Bottom line:** Make your own copy of this repository, open it with Claude Code or Codex, and paste the prompt below. The agent will verify the starter and begin a guided interview before personalizing anything.

**When to read this:** Read when installing the system from GitHub.

## easiest option

1. On GitHub, select **Use this template**.
2. Create a private repository in your own GitHub account.
3. Open or clone that new repository with Claude Code or Codex.
4. Paste the setup prompt below.

Using the template keeps the clean starter unchanged while giving you your own version history.

## download option

1. On GitHub, select **Code**, then **Download ZIP**.
2. Unzip the folder somewhere private on your computer.
3. Open that folder as an Obsidian vault.
4. Open Claude Code or Codex with that same folder as its working folder.
5. Paste the setup prompt below.

## setup prompt

```text
Help me install and personalize this Obsidian agent system.

First, confirm you can access the repository files. Then read:
- AGENTS.md
- FRIEND-SETUP-GUIDE.md
- START-HERE.md
- os/me.md
- os/agent-rules.md
- os/vault-map.md
- os/retrieval.md
- os/onboarding-interview.md

Run ruby os/validate-life-os.rb and tell me whether the clean starter passes.

Then follow prompts/01-onboarding-interview.md. Explain the process in plain
language and ask only Section 1. Continue one section at a time.

Do not edit or create files during the interview. At the end, show me the
proposed blueprint and exact change list. Wait for my explicit approval before
personalizing the system. After approval, follow the remaining prompts in order
and keep explaining each step simply.

Do not publish, share, delete, or create a remote repository without asking me.
```

## one important limitation

Ordinary browser chat can explain the files and conduct the interview, but it usually cannot install or edit local files by itself. Use Claude Code, Codex, or another agent that can work directly inside a folder on your computer for the complete setup.

## after setup

The agent will guide you through building, testing, private version history, and a first-week review. You do not need to learn Git or design the folder structure yourself.
