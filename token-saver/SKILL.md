---
name: token-saver
description: Use when a session is long, context is expensive, tool calls are repetitive, or the user asks for efficient work without sacrificing correctness.
---

# Token Saver

Reach the fewest-token result that still gets the work done and verified. A
short session is not successful if it leaves the human to reconstruct what
happened.

## Where cost comes from

The main cost is input repeated across turns. Avoid:

- reading a whole file when a targeted range answers the question;
- rereading files immediately after a successful edit;
- using screenshots or large DOM dumps when text is enough;
- polling a slow job in a tight loop;
- narrating a plan, executing it, and then repeating the plan;
- dumping raw command output instead of summarizing the finding.

## Cheap path

1. Locate before reading. Search for the symbol or relevant lines, then read
   only the needed range. When editing, read enough surrounding context to
   preserve the file's invariants.
2. Use the cheapest surface that answers the question:

   ```
   CLI or API → filesystem → rendered UI
   ```

   Shape output at the source: request selected JSON fields, inspect a diff
   summary before a full diff, and limit logs to the relevant interval.
3. Batch independent searches, reads, and commands in one turn.
4. Treat a successful edit or trusted green check as evidence. Recheck only
   when another process could have changed the result.
5. Prefer blocking waits, background jobs, or scheduled wakeups over polling.
6. Delegate only when the conclusion is cheaper than loading the search output
   into the current context. Do not duplicate the same investigation yourself.
7. Stop when the answer is reached. Do not add speculative cleanup.

## Communication

- Ask one batched round of questions, or none when a sensible default exists.
- Do not narrate routine tool use.
- Report the one to three findings that carry the conclusion.
- Spend freely on verification that the task genuinely requires. Cheapness is
  never a reason to guess.

## When to optimize less

Read broadly when changing a central or unfamiliar component, reviewing a
large diff, or investigating a failure whose cause may be elsewhere. The
rework from an incomplete mental model costs more than the initial context.

For completion reports, use the companion `work-report` skill.

Copyright (c) 2026 Daniel Noam Tuby. Licensed under the MIT License; see
`../LICENSE-MIT.txt`.
