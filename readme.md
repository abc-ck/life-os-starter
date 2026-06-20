---
type: map
created: 2026-06-19
reviewed: 2026-06-19
status: living
authority: canon
source: ai
---

# life os starter

**Bottom line:** A model-agnostic Obsidian operating system for personal knowledge, projects, recurring life areas, chronology, and agent collaboration. The structure is reusable; the owner's context is created through interview and approval.

**When to read this:** Read for a quick explanation of the starter. If this is your first time here, open `FRIEND-SETUP-GUIDE.md` next.

## quickest setup

Open `INSTALL-WITH-AN-AGENT.md` for the GitHub download options and one prompt you can give to Claude Code or Codex.

## first time here

1. Use `INSTALL-WITH-AN-AGENT.md` to make your own copy.
2. Read `SYSTEM-EXPLAINED.md` for the plain-English idea.
3. Follow `FRIEND-SETUP-GUIDE.md` one step at a time.
4. Use `START-HERE.md` as the agent's setup checklist.
5. Use `knowledge-map.md` for task routing after onboarding.

## methodology

- Local Markdown files are the durable source of truth.
- Agents retrieve through maps, filenames, summaries, and freshness metadata.
- Current authority outranks old or exploratory material.
- Raw capture is separated from durable knowledge.
- Projects end; areas continue.
- Archived material remains available but never loads as current truth.
- Validators catch metadata, link, index, and lifecycle drift.
- Git provides rollback; private remote hosting is optional and owner-approved.

## structure

- `00_inbox/` — raw or unclear intake awaiting one permanent home.
- `os/` — identity, rules, structure, retrieval, skills, setup, and history.
- `knowledge/` — durable concepts and people context.
- `areas/` — recurring responsibilities without finish lines.
- `projects/` — time-bound personal outcomes.
- `business/` — optional business ventures or independently versioned business repos.
- `journal/` — daily, weekly, monthly, and decision chronology.
- `archive/` — inactive material, never startup truth.
- `agent/templates/` — safe Markdown templates.
- `prompts/` — copy-and-run setup, testing, Git, and first-week prompts.

## privacy

This starter contains no personal profile or example journal. Keep the completed vault private unless the owner explicitly chooses otherwise. Never store passwords, API keys, seed phrases, private keys, credentials, or highly sensitive attachments in Git.
