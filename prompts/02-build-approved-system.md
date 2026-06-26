---
type: note
created: 2026-06-20
updated: 2026-06-26
reviewed: 2026-06-26
status: living
authority: canon
source: ai
---

# prompt 2 — build the approved system

**Bottom line:** Turns an explicitly approved interview blueprint into the personalized Markdown system.

**When to read this:** Give this prompt to the agent only after correcting and approving the blueprint.

```text
The onboarding blueprint is approved. Build it now.

Read AGENTS.md, os/skills/system-setup.md, os/retrieval.md, and
os/vault-map.md before editing.

Requirements:
- Use only facts, preferences, folders, projects, areas, and routines that I
  approved.
- Update os/me.md and knowledge/people/owner.md without overloading startup.
- Preserve the baked-in agent rules unless the approved blueprint explicitly
  changes them.
- Personalize os/agent-rules.md only where my approved preferences or
  boundaries differ from the starter defaults.
- Update knowledge-map.md and folder readmes to route my real tasks.
- Create only approved area, project, business, and topic folders.
- Keep uncertain material draft/exploratory.
- Mark owner-approved statements source: owner; keep agent drafts source: ai.
- Add top summaries and accurate metadata.
- Preserve privacy and never store credentials.
- Run ruby os/validate-life-os.rb and fix every failure.
- Show me the files created/changed, remaining unknowns, and a layman's summary.
- Do not initialize or publish Git yet; that is a separate approved step.

Continue until the approved build and validation are complete.
```
