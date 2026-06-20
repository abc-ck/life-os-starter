---
type: note
created: 2026-06-20
reviewed: 2026-06-20
status: living
authority: canon
source: ai
---

# implement the knowledge retrieval system

**Bottom line:** Copy-and-run prompt for adding the maps, summaries, metadata, currency checks, indexes, and before/after testing that make a Markdown knowledge base reliable for AI agents.

**When to read this:** Give the prompt below to Claude Code, Codex, or another agent that can read and edit the full vault.

```text
Implement a reliable AI knowledge-retrieval system in this Markdown/Obsidian
vault. Work carefully until the system is implemented, tested, corrected, and
tested again.

The goal is not to create more tags or a denser backlink graph. The goal is to
help an agent quickly answer four questions:
1. Where should I start for this task?
2. Which file is relevant?
3. Which source is current and authoritative?
4. Which old, draft, or historical source must not override current truth?

OPERATING RULES

- Read the vault's AGENTS.md, CLAUDE.md, root readme, current maps, status files,
  specs, decision logs, and folder indexes before proposing changes.
- During the first pass, do not edit, delete, rename, or move anything.
- Preserve the owner's meaning and existing source hierarchy.
- Never invent dates, approval, authority, or currency.
- Never bulk-label files as current merely because they exist.
- Archive instead of delete unless the owner explicitly directs otherwise.
- Keep backlinks for meaningful human navigation. Do not add links merely to
  make the graph denser.
- Do not add a vector database, graph database, embeddings, or external RAG
  layer unless measured failures show that files, maps, search, and ordinary
  context are insufficient.

PHASE 1: RECONNAISSANCE AND BASELINE

1. Inventory all active Markdown files by folder.
2. Identify the existing sources of truth: owner instructions, canon, specs,
   status, decisions, operating manuals, references, drafts, and archives.
3. Find conflicting, stale, duplicated, undated, or ambiguously labeled files.
4. Find large folders without useful indexes.
5. Find important files without a clear top summary.
6. Check whether multiple metadata conventions are in use.
7. Design 10-14 realistic retrieval questions covering routine lookups,
   conflicting sources, retired concepts, drafts, time-sensitive facts, and
   historical material.
8. Run a read-only baseline. For each question record:
   - files opened
   - source selected
   - whether conflicts were handled correctly
   - whether the answer was correct
   - whether provenance was clear
   - unnecessary files opened

Report the baseline and a proposed implementation plan. Wait for the owner's
explicit approval before editing.

PHASE 2: CREATE THE RETRIEVAL STANDARD

Create or update one governing retrieval document. Use this small schema unless
the vault already has an approved equivalent:

---
type: note # allowed: note, map, identity, skill, daily, weekly, monthly,
           # decision-log, history, status
created: YYYY-MM-DD
updated: YYYY-MM-DD
reviewed: YYYY-MM-DD
status: living | draft | superseded | done | archived
authority: canon | spec | reference | exploratory
source: owner | ai
superseded_by: path/to/current-file.md
---

Rules:
- created = known creation date.
- updated = when the actual content or current truth changed. Omit if unknown.
- reviewed = when currency or metadata was checked. It does not prove the
  content changed or that external facts are still current.
- living = current and maintained.
- draft = incomplete, unapproved, or uncertain.
- superseded = replaced and must include superseded_by.
- done = completed time-bound record.
- archived = historical and never current startup truth.
- canon/spec outrank reference; reference outranks exploratory.
- source: owner outranks source: ai for the owner's intentions and decisions.
- The owner's current words outrank all files.
- Never allow superseded or archived files to override living sources.

Every important content or routing file should open after its H1 with:
- Bottom line: the real claim, state, or contents in 1-3 lines.
- When to read this: the task that should route an agent here in 1-2 lines.

PHASE 3: BUILD PROGRESSIVE DISCLOSURE

1. Create one root task-to-file knowledge map.
2. Organize routes by real task, not merely by folder name.
3. Keep each route to four files or fewer and state the reading order.
4. Name the governing source and clearly identify draft, historical,
   superseded, or time-sensitive material.
5. Add a short index to each knowledge-heavy folder: one line per file saying
   what it contains and when to read it.
6. Add local maps only when a folder is large enough to need one.
7. Use descriptive filenames that make text search useful.

PHASE 4: PILOT BEFORE SCALING

1. Choose one high-value, conflict-prone folder as a pilot.
2. Before setting status, compare every file against current canon, specs,
   status, and decisions.
3. Add accurate frontmatter and top summaries.
4. Mark replaced files superseded and point to the current source.
5. Mark historical files archived.
6. Leave uncertain files draft/reference and flag the uncertainty.
7. Update the folder index and root map.
8. Validate links, YAML, lifecycle values, and index coverage.
9. Report the pilot findings and wait for owner review before scaling.

PHASE 5: SCALE FOLDER BY FOLDER

Repeat the pilot method for each approved folder. Do not run a blind metadata
migration. Currency verification is the work.

Do not silently rewrite owner-authored body content. Add metadata and summaries,
then separately propose any body corrections needed to remove stale claims.

PHASE 6: VALIDATE

Create or adapt a validator that checks at minimum:
- required frontmatter and allowed vocabulary
- honest date semantics
- superseded_by on superseded files
- H1, Bottom line, and When to read this
- broken Markdown and wiki links
- every active content file appears in a map or folder index
- archived/superseded material is not presented as current
- no legacy inline status system conflicts with frontmatter
- no credential-shaped text or personal data leaks during templating

Run it after every folder and fix every real failure.

PHASE 7: REPEAT THE ACCEPTANCE TEST

Run the same baseline questions with fresh, read-only agent passes. Score each
task from 0-2 on:
- source selection
- conflict handling
- answer correctness
- retrieval efficiency
- provenance

Compare before and after using:
- total score and percentage
- correctness failures
- average files opened per task
- stale/conflict tasks handled correctly
- routes that still cause over-fetching

Do not claim a wall-clock speed improvement unless seconds were actually timed.
Describe reduced file opening and fewer wrong turns as retrieval efficiency.
Disclose one-run, analytical-baseline, or other test limitations.

PHASE 8: FINISHING GATE

Continue reviewing, fixing, validating, and retesting until:
- no high- or medium-severity retrieval defect remains
- every active content file is indexed
- stale files cannot masquerade as current truth
- current authority is unambiguous
- the validator passes
- the acceptance test has zero correctness failures
- the owner can understand the system in plain language

At the end, report:
1. What changed.
2. Currency conflicts found.
3. Before/after results.
4. Remaining low-risk limitations.
5. The maintenance routine and when to run it.

Do not commit or push until the owner reviews the final report and explicitly
approves version-control actions.
```
