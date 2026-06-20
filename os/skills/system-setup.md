---
type: skill
created: 2026-06-20
reviewed: 2026-06-20
status: living
authority: canon
source: ai
---

# system setup

## purpose

Turn an approved onboarding blueprint into a small, personalized, validated Obsidian agent system.

## trigger

Run after the owner explicitly approves the interview blueprint, or approves a major redesign.

## inputs

- `os/onboarding-interview.md`
- approved interview synthesis and corrections
- `os/retrieval.md`
- `os/vault-map.md`
- starter files and templates

## steps

1. Restate the approved scope and exact files/folders to change.
2. Update `os/me.md` with short startup-relevant identity and collaboration context.
3. Put deeper approved context in `knowledge/people/owner.md` only when useful.
4. Personalize agent rules, environment, capture, privacy, and Git boundaries.
5. Create only approved area, project, business, and topic folders.
6. Update root/local maps and readmes with task-based routes.
7. Activate only approved skills; leave uncertain routines draft or remove them.
8. Mark owner-approved content `source: owner`; keep unapproved drafts `source: ai`.
9. Run the validator and resolve every failure.
10. Explain what changed in plain language and list remaining owner decisions.

## boundaries

- Do not build before explicit blueprint approval.
- Do not invent personal facts, routines, projects, or privacy preferences.
- Do not copy another person's identity, businesses, journal, or knowledge.
- Do not create folders merely to make the system look complete.
- Do not initialize/publish Git unless that separate step is approved.
