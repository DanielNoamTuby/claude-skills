# Contributing

Small, focused pull requests are the easiest to review and merge.

## Adding or changing a skill

- Keep `SKILL.md` self-contained: no reference to a specific repo, directory
  layout, command, service, or private data. A skill in this pack must work
  in any project.
- Keep the YAML frontmatter to `name` and `description`. The description is
  what Claude Code matches against — write it as "Use when …" so it's
  obvious when the skill should trigger.
- If a skill is adapted from another project, add an attribution note at the
  bottom of the file and update [NOTICE.md](NOTICE.md) with the source,
  author, and license.
- Update the table in [README.md](README.md) when adding, removing, or
  renaming a skill.

## Reporting an issue

Open a GitHub issue with the skill name, what you expected, and what
happened instead. Include the prompt that should (or shouldn't) have
triggered it if the issue is about matching.

## License

By contributing, you agree your changes are licensed under the same terms
as the file you're editing (MIT or Apache-2.0 — see [README.md](README.md#license)).
