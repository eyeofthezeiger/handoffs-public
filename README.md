# handoffs-public

Reusable handoff docs: context files you give an agent (or a person) so it can pick up a kind of work cold. Every file here is generic and scrubbed.

## What goes here

- Handoffs that work for anyone's project, with no company, client, people or personal context.
- Each one starts from [templates/handoff.md](templates/handoff.md).

## Folder map

- `agents/` setting up and running agents
- `builds/` building and shipping software
- `research/` research and analysis jobs
- `ops/` operations, maintenance and automation
- `templates/handoff.md` the template

## Using a handoff

1. Copy the file into your project.
2. Fill in the Context section with your own details.
3. Give it to your agent as its starting instructions.

## How things get added

Handoffs are written privately first, scrubbed with the checklist in [CONTRIBUTING.md](CONTRIBUTING.md), and arrive here only through a pull request the owner reviews and merges.

## Naming

`YYYY-MM-DD-<project>-<target-agent>-<slug>.md`, e.g. `2026-11-07-starter-repo-coding-agent-add-ci.md`.

## Sibling repos

- [ai-kit](https://github.com/eyeofthezeiger/ai-kit): skills, prompts, MCP servers and evals a handoff can point to
- [patterns](https://github.com/eyeofthezeiger/patterns): snippets and configs
- [fullstack-starter](https://github.com/eyeofthezeiger/fullstack-starter) and [agent-starter](https://github.com/eyeofthezeiger/agent-starter): project templates

## License

MIT. See [LICENSE](LICENSE).
