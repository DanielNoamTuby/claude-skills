---
name: work-report
description: Use when finishing a non-trivial change, investigation, review, or handoff and the result needs a concise, evidence-based summary.
---

# Work Report

Close substantive work with a scannable report that lets another person
understand the result without re-deriving it.

```markdown
**Done** — <one sentence: what now exists or works>

**Changed**
- `path/to/file:line` — what changed and why

**Verified**
- <check that actually ran and its result>

**Watch out**
- <known gap, assumption, or deliberate scope boundary>

**Next**
1. <concrete next action>
```

## Rules

- Make **Done** truthful. Failures and unfinished work belong there plainly.
- List only paths actually changed; include a line number when one site is
  specific.
- In **Verified**, report what ran, not what should work. “Not verified:
  <reason>” is valid.
- Put assumptions and judgment calls in **Watch out**.
- Make **Next** actionable rather than aspirational.
- Omit an empty section only when it is genuinely irrelevant; otherwise write
  `None`.
- Scale the format down for trivial work. A one-line fix usually needs only
  **Done** and **Changed**.
- For a question with no file changes, answer in plain prose instead.

Keep the report shorter than the work it describes. Offer to turn a genuinely
deferred fix into a tracked task when a task system is available.

Copyright (c) 2026 Daniel Noam Tuby. Licensed under the MIT License; see
`../LICENSE-MIT.txt`.
