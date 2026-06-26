---
type: status
created: 2026-06-19
updated: 2026-06-26
reviewed: 2026-06-26
status: draft
authority: canon
source: ai
---

# start here

**Bottom line:** This is a clean Obsidian agent-system starter. Its default agent behavior is already baked in; identity, areas, projects, priorities, routines, privacy choices, and intentional deviations are personalized through the onboarding interview.

**When to read this:** This is the agent's setup checklist. A new owner should begin with `FRIEND-SETUP-GUIDE.md` instead.

## before setup

The owner may read `SYSTEM-EXPLAINED.md` for a plain-English overview. Do not personalize files until the interview is complete and the owner has explicitly approved the blueprint.

## setup sequence

1. Open this folder as an Obsidian vault.
2. Start Claude or Codex from the vault root.
3. Give the agent the prompt in `os/onboarding-interview.md`.
4. Complete the interview one section at a time.
5. Review and approve the proposed blueprint before files are personalized.
6. Let the agent update `os/me.md`, the root maps, folder readmes, chosen areas/projects, and approved skills.
7. Run `ruby os/validate-life-os.rb` and resolve every failure.
8. Initialize a private Git repository only after checking the tracked files and exclusions.

## completion gate

Onboarding is complete when:

- `os/me.md` accurately describes the owner and is approved.
- `os/agent-rules.md` preserves the starter's baseline behavior and reflects any owner-approved communication or action-boundary changes.
- `knowledge-map.md` routes the owner's real tasks.
- Only justified areas, projects, businesses, and skills exist.
- The validator passes.
- The owner can answer "where does this go?" and "what should the agent read first?" without guessing.
