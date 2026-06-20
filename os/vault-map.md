---
type: map
created: 2026-06-19
reviewed: 2026-06-19
status: living
authority: canon
source: ai
---

# vault map

**Bottom line:** Structural source of truth for this Obsidian vault. The top-level lanes are stable; specific area, project, business, and knowledge folders are created only when the onboarding interview or real use justifies them.

**When to read this:** Read when deciding where a file belongs, adding structure, or resolving conflicting organization rules.

## three layers

1. **Notes** — the owner's Markdown thinking in `knowledge/`, `areas/`, `projects/`, `business/`, `journal/`, and `00_inbox/`.
2. **OS** — `os/` holds identity, rules, routing, skills, setup, validation, and history.
3. **Tools** — Obsidian, Claude, Codex, and future/local models. Tools are replaceable; files are durable.

## folder map

- `00_inbox/` — raw or unclear intake; a waiting room, never permanent storage.
- `os/` — operating layer and agent contract.
- `knowledge/` — durable people and topic reference.
- `areas/` — ongoing responsibilities with no finish line.
- `projects/` — time-bound personal outcomes.
- `business/` — optional ventures or independently versioned business repositories.
- `journal/` — chronological daily, weekly, monthly, and decision records.
- `archive/` — inactive material; available for history, excluded from startup truth.
- `agent/` — templates and agent-facing support files.
- `prompts/` — owner-facing setup prompts; operational rules still live in `os/`.

## routing rules

Route each item to one primary home:

- durable concept/reference -> `knowledge/topics/`
- person context -> `knowledge/people/`
- business venture -> `business/<venture>/`
- time-bound personal outcome -> `projects/<project>/`
- ongoing responsibility -> `areas/<area>/`
- dated record -> `journal/`
- durable decision and rationale -> `journal/decisions.md`
- repeatable agent routine -> `os/skills/` and `os/skill-map.md`
- task-to-file routing -> `knowledge-map.md` at the relevant root
- saved continuity -> `os/history/`
- inactive material -> `archive/<date-topic>/`
- unclear/raw -> `00_inbox/`

## conventions

### naming

- lowercase kebab-case for ordinary files/folders
- daily: `YYYY-MM-DD.md`
- weekly: `YYYY-Www.md`
- monthly: `YYYY-MM.md`
- history: `YYYY-MM-DD-topic.md`

### linking and retrieval

- Agent retrieval uses maps, filenames, summaries, and freshness markers. See `os/retrieval.md`.
- Wikilinks and backlinks support human navigation and real conceptual jumps; do not add them merely for density.
- Daily notes may link to touched projects, areas, people, and topics to create a human timeline.

### frontmatter

Every active note uses the schema in `os/retrieval.md`. The generic provenance values are `source: owner` and `source: ai`.

### human and AI authorship

Agent-drafted notes remain `source: ai` until the owner approves and adopts them. Agents do not silently overwrite owner-authored meaning.

## environment

Personalize after interview:

- local vault path and devices
- capture method and sync choice
- private Git or backup strategy
- independently versioned nested repositories
- files/directories excluded from version control

Keep the vault private by default. Open it as one Obsidian vault; do not rely on Obsidian-only features for core meaning.
