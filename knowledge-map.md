---
type: map
created: 2026-06-19
reviewed: 2026-06-19
status: draft
authority: canon
source: ai
---

# knowledge map

**Bottom line:** Root task-to-file router for the owner. Core system routes are ready; personal, project, business, and area routes must be added from the approved onboarding blueprint.

**When to read this:** At the start of a task after `os/me.md`, or whenever the correct context file is unclear.

## core routes

### start or orient

Read `os/me.md` -> `os/agent-rules.md` -> `os/vault-map.md`. Add `os/skill-map.md` when the task may match a repeatable routine.

### setup or personalization

Read `START-HERE.md` -> `os/onboarding-interview.md` -> `os/skills/system-setup.md`.

### retrieval, metadata, or structure

Retrieval: `os/retrieval.md`. Structure: `os/vault-map.md`. Metadata maintenance: `os/skills/metadata-audit.md`.

### inbox

Start at `00_inbox/readme.md`, then use `os/skills/inbox-triage.md`.

### durable knowledge

Start at `knowledge/readme.md`. Load `knowledge/people/owner.md` only when deeper personal context materially helps.

### projects, areas, or business

Personal projects: `projects/readme.md`. Ongoing responsibilities: `areas/readme.md`. Business ventures: `business/readme.md`.

### chronology or decisions

Start at `journal/readme.md`; durable owner decisions live in `journal/decisions.md`.

### saved continuity

Start at `os/history/readme.md`. Prefer current status and living handoffs over transcripts.

### templates

Start at `agent/templates/readme.md`.

## personalized routes

Add routes here only after onboarding identifies real recurring tasks. Keep each instruction to four files or fewer.

## source hierarchy

1. The owner's current words.
2. `os/me.md`, `os/agent-rules.md`, and `os/vault-map.md`.
3. Current project or business status/spec files.
4. `journal/decisions.md`.
5. Living reference notes.
6. Draft or exploratory notes.
7. Superseded, done, and archived records for history only.

## maintenance

Update this map when current work or routing changes. Run `ruby os/validate-life-os.rb` afterward.
