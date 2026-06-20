---
type: map
created: 2026-06-20
reviewed: 2026-06-20
status: living
authority: canon
source: ai
---

# your simple setup guide

**Bottom line:** You do not need to design this system yourself. Open the folder, let Claude or Codex interview you, approve the proposed setup, and let the agent build and test it one step at a time.

**When to read this:** Start here if this vault was given to you by a friend or you have never used an agent-driven Obsidian system.

Before setup, you can read `SYSTEM-EXPLAINED.md` for a two-minute explanation of how the pieces work together.

For a visual explanation of the knowledge-retrieval method and its measured results, open `READ-FIRST-KNOWLEDGE-SYSTEM.html` in a web browser.

## what this is

Think of this folder as a small operating system for your notes and your AI assistant.

- **Obsidian** is where you can read and edit everything.
- **Markdown files** are the permanent memory.
- **Claude or Codex** reads those files and helps you work.
- **Git** is a time machine that lets you restore earlier versions.

The AI tool can change later. Your files remain yours.

## what each folder means

- `00_inbox/` — the kitchen counter: new things land here before they are put away.
- `os/` — the instruction manual: who you are, how the agent should work, and how the system is organized.
- `knowledge/` — the reference shelf: useful information worth keeping.
- `areas/` — responsibilities that continue, such as health, home, or finances.
- `projects/` — things with a finish line.
- `business/` — optional business work.
- `journal/` — the timeline of what happened and what you decided.
- `archive/` — old material kept for history but no longer treated as current.

You do not need to memorize this. The agent uses the maps to put things in the right place.

## step 1 — open the folder

1. Install Obsidian if needed.
2. Choose **Open folder as vault**.
3. Select this repository folder.
4. Open `FRIEND-SETUP-GUIDE.md` in Obsidian.

Do not start creating lots of folders. The interview will determine what you actually need.

## step 2 — open an agent in this folder

Use Claude Code, Codex, or another file-capable coding agent with this folder as its working folder.

The agent must be able to read and edit local Markdown files. Ordinary browser chat without file access can conduct the interview, but it cannot finish the setup automatically.

## step 3 — run the interview

Open `prompts/01-onboarding-interview.md` and give that prompt to the agent.

The agent will:

1. Ask one small group of questions at a time.
2. Let you answer naturally.
3. Ask useful follow-ups.
4. Avoid changing files while interviewing you.
5. Show you a proposed setup before building anything.

There are no perfect answers. The goal is to learn how your real life and brain work.

## step 4 — approve the blueprint

The agent will summarize:

- what you want help with
- how you prefer to work
- your current projects and ongoing responsibilities
- your privacy and approval rules
- the smallest useful folder structure
- which routines might help

Correct anything that feels wrong. Remove anything that feels excessive. Say clearly when the blueprint is approved.

## step 5 — let the agent build it

After approval, use `prompts/02-build-approved-system.md`.

The agent will personalize the identity file, instructions, maps, areas, projects, templates, and selected routines. It should not add speculative folders or personal facts you did not approve.

## step 6 — test it

Use `prompts/03-review-and-test.md`.

The agent will check that:

- your real questions lead to the right files
- old notes cannot override current decisions
- every useful file is indexed
- links and metadata work
- no starter placeholders or another person's information remain
- the system is understandable without technical knowledge

Do not consider setup complete until the validator passes.

## step 7 — protect it with private version history

Use `prompts/04-private-git-setup.md`.

The starter already includes a clean local history. The agent will inspect your personalized files, exclude local settings and credentials, scan for secret-shaped text, save a new checkpoint, and optionally create a private remote repository after you approve it.

Keep this vault private by default.

## step 8 — use it for one week

For the first week:

- Put uncertain notes in `00_inbox/`.
- Ask the agent where something belongs instead of inventing a new folder.
- Use the system on real work.
- Notice what feels helpful or annoying.
- Do not rebuild it because one day felt messy.

At the end of the week, use `prompts/05-first-week-review.md`.

## the labels in plain English

Every important file carries small labels at the top:

- `status` — is this current, unfinished, replaced, completed, or historical?
- `authority` — is this a rule/spec, useful reference, or an untested idea?
- `source` — did you approve/write it, or did an agent draft it?
- `updated` — when the actual information changed.
- `reviewed` — when someone last checked whether its labels and currency were honest.

These labels help the agent avoid confidently using the wrong note.

## three rules to remember

1. **Use the inbox when unsure.** You do not need to organize while capturing.
2. **Projects finish; areas continue.** This prevents endless project lists.
3. **Archive instead of delete.** Old information remains recoverable without confusing current work.
