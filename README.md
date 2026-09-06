# Claude Skills

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE-MIT.txt)
[![License: Apache 2.0](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE-APACHE-2.0.txt)

A small pack of general-purpose [Claude Code](https://docs.claude.com/en/docs/claude-code) skills — reusable playbooks for disciplined agent behavior and design work. Each one is a single `SKILL.md`. Drop the folder you want into any project and Claude loads it automatically when a task matches.

None of these skills assume a particular repo, stack, tool, or private data. They only read and write files inside the project they're used in.

## What's inside

| Skill | Use it when |
| --- | --- |
| [`grill-me`](grill-me/SKILL.md) | A rough plan or design needs challenge before work begins |
| [`design-brief`](design-brief/SKILL.md) | A feature or page needs its problem, direction, and scope captured before implementation |
| [`information-architecture`](information-architecture/SKILL.md) | Navigation, content hierarchy, or user flows need defining before visual design |
| [`design-tokens`](design-tokens/SKILL.md) | A project needs a visual token system, or is missing a token category |
| [`brief-to-tasks`](brief-to-tasks/SKILL.md) | A design brief needs turning into an ordered, buildable checklist |
| [`frontend-design`](frontend-design/SKILL.md) | A frontend interface needs a deliberate visual direction instead of generic styling |
| [`design-review`](design-review/SKILL.md) | Built UI needs a structured critique against its brief |
| [`design-flow`](design-flow/SKILL.md) | You want the full design-to-build workflow, guided phase by phase |
| [`token-saver`](token-saver/SKILL.md) | A session is long, context is expensive, or work needs to stay efficient |
| [`work-report`](work-report/SKILL.md) | Non-trivial work needs a concise, evidence-based completion summary |

## Install

Claude Code skills live in a `SKILL.md` file under a `skills/` directory. Copy the folders you want:

```bash
git clone https://github.com/DanielNoamTuby/claude-skills.git /tmp/claude-skills
```

**Project-level** (this project only) — copy into `.claude/skills/`:

```bash
cp -r /tmp/claude-skills/design-brief .claude/skills/
```

**User-level** (every project) — copy into `~/.claude/skills/`:

```bash
cp -r /tmp/claude-skills/design-brief ~/.claude/skills/
```

Grab everything at once:

```bash
cp -r /tmp/claude-skills/{grill-me,design-brief,information-architecture,design-tokens,brief-to-tasks,frontend-design,design-review,design-flow,token-saver,work-report} ~/.claude/skills/
```

## How they work

Each `SKILL.md` starts with a `name` and `description`. Claude Code reads every installed skill's description and invokes the matching one automatically when a request fits — you don't need to remember a command, though asking for one by name (`grill me on this`, `write a design brief`) works too.

## The design flow

Seven of these skills chain into one workflow, orchestrated by `design-flow`:

```
grill-me → design-brief → information-architecture → design-tokens
         → brief-to-tasks → frontend-design → design-review
```

Invoke `design-flow` to run the whole sequence with checkpoints between phases, or call any phase on its own — each one also works standalone. `token-saver` and `work-report` are independent: the first is a standing efficiency discipline, the second is an output format for wrapping up any piece of work.

## License

This repo is dual-licensed by file:

- `token-saver`, `work-report` — [MIT](LICENSE-MIT.txt), Copyright (c) 2026 Daniel Noam Tuby
- everything else — [Apache License 2.0](LICENSE-APACHE-2.0.txt), adapted from [`designer-skills`](https://github.com/julianoczkowski/designer-skills) by Julian Oczkowski

See [NOTICE.md](NOTICE.md) for full attribution.

## Contributing

Issues and pull requests are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).
