---
type: note
created: 2026-06-20
reviewed: 2026-06-20
status: living
authority: canon
source: ai
---

# prompt 3 — review and test

**Bottom line:** Runs an independent structural and behavioral acceptance test before setup is declared complete.

**When to read this:** Give this prompt to an agent after the approved build passes its first validator run.

```text
Perform an independent read-only acceptance review of this personalized vault.

Do not edit during the first review pass.

Test:
1. The startup instructions and owner profile are clear.
2. Ten realistic questions from my actual life route to the smallest correct
   set of files.
3. Current owner decisions outrank drafts, old notes, and history.
4. Every active content file appears in a map or index.
5. Metadata, summaries, links, and superseded pointers are valid.
6. No starter placeholders or another person's personal/business context remain.
7. Sensitive context is not loaded by default.
8. The folder system matches my approved life and does not contain speculative
   structure.
9. A nontechnical owner can understand where capture, projects, areas,
   knowledge, chronology, and archive belong.
10. ruby os/validate-life-os.rb passes.

Report findings by severity first. If there are findings, ask for permission
to fix them, then rerun the complete test until clean. Do not declare the system
finished merely because metadata parses.
```
