---
type: map
created: 2026-06-19
reviewed: 2026-06-19
status: living
authority: canon
source: ai
---

# retrieval

**Bottom line:** Agents retrieve through task maps, descriptive filenames, top summaries, and lifecycle/authority metadata. Obsidian's graph is useful for human exploration but is not the agent index.

**When to read this:** Read when finding, ranking, creating, auditing, or resolving conflicts between notes.

## retrieval order

1. Start at the relevant `knowledge-map.md` or folder readme.
2. Narrow candidates by descriptive filename.
3. Read each candidate's bottom line and when-to-read block.
4. Check lifecycle, authority, source hierarchy, and content date.
5. Search full text for anything the maps miss.
6. Load only the files required by the task.

## conflict ranking

1. The owner's current words always win.
2. Never treat `superseded` or `archived` files as current; follow `superseded_by`.
3. `canon`/`spec` outrank `reference`, which outranks `exploratory`.
4. For build behavior, `spec` wins; for principles, `canon` wins. Project source hierarchies provide the exact local order.
5. Break equal-authority ties with `updated`, falling back to `created`. `reviewed` does not imply fresh content.
6. Prefer `source: owner` over `source: ai` for the owner's intentions and decisions.

## metadata schema

```yaml
---
type: note            # note | map | identity | skill | daily | weekly | monthly | decision-log | history | status
created: YYYY-MM-DD
updated: YYYY-MM-DD    # content/current truth changed; omit if unknown
reviewed: YYYY-MM-DD   # last currency/metadata audit; not content freshness
status: living         # living | draft | superseded | done | archived
authority: reference   # canon | spec | reference | exploratory
source: owner          # owner | ai
# conditional/optional
superseded_by: path/to/current-file.md
domain:
applies_to:
related:
---
```

- `living` — current and maintained.
- `draft` — incomplete, unapproved, or not yet validated.
- `superseded` — replaced; requires `superseded_by`.
- `done` — completed time-bound record.
- `archived` — historical, not current.
- `canon` — settled operating truth or principle.
- `spec` — governing product/build behavior.
- `reference` — useful but not authoritative.
- `exploratory` — unvalidated ideas or research leads.

## top summary

Every knowledge, project, status, and routing file opens after its H1 with:

- **Bottom line:** the real claim, state, or contents in 1–3 lines.
- **When to read this:** the task that should route an agent here in 1–2 lines.

Do not restate the title. If the conclusion or current state changes, update the bottom line.

## routing maps

A routing map answers "for task X, read Y before Z."

- Use one root `knowledge-map.md`, plus local maps only when an area/repo becomes large enough.
- Group by task, not folder taxonomy.
- Keep each instruction to four files or fewer; split broad lanes by intent.
- Name current authority and identify draft, historical, or time-sensitive material explicitly.

## maintenance

- Use YAML frontmatter, not duplicate inline status labels.
- Content change -> bump `updated`.
- Currency/metadata audit only -> set `reviewed`; do not fake freshness.
- Never invent dates or authority. Omit unknown `updated`; use `draft`/`exploratory` when uncertain.
- Update maps and folder readmes when files move or lifecycle changes.
- Run `ruby os/validate-life-os.rb` after structural or metadata work.

## scale boundary

Files, maps, search, and modern long context are sufficient at ordinary personal-vault scale. Add a vector database or external RAG layer only after measured retrieval failures justify its complexity.
