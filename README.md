# Apollo Solutions Skills

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENCE-MIT)

A collection of skills for AI coding agents, maintained by the Apollo Solutions and Field teams. These skills are experimental or not fully supported in the same way as the official [Apollo GraphQL skills repository](https://github.com/apollographql/skills).

Apollo Skills follow the [Agent Skills](https://agentskills.io/) format and are available via the [Skills CLI](https://skills.sh/).

> **The code in this repository is experimental and has been provided for reference purposes only. Community feedback is welcome but this project may not be supported in the same way that repositories in the official [Apollo GraphQL GitHub organization](https://github.com/apollographql) are. If you need help you can file an issue on this repository, [contact Apollo](https://www.apollographql.com/contact-sales) to talk to an expert, or create a ticket directly in Apollo Studio.**

## Installation

Install skills using the [Skills CLI](https://skills.sh/docs/cli):

```bash
npx skills add apollosolutions/skills
```

The CLI guides you through an interactive installation:

1. **Select skills** - Choose which skills to install
2. **Select agents** - Pick target agents (Claude Code, Codex, Cursor, Gemini CLI, Goose, OpenCode)
3. **Installation scope** - Project (committed with your code) or Global
4. **Installation method** - Symlink (recommended) or Copy

## Claude Code Plugin

You can also install skills as a [Claude Code plugin](https://code.claude.com/docs/en/discover-plugins).

Once installed, skills are available as namespaced slash commands (e.g., `/apollo-solutions-skills:skill-creator`).

## Available Skills

### skill-creator

Guide for creating effective skills for this repository.

**Install:**

```bash
npx skills add apollosolutions/skills@skill-creator
```

**Use when:**

- Creating a new skill for this repository
- Updating an existing skill's structure or content
- Learning skill best practices and patterns
- Writing SKILL.md files or reference documentation

**References:**
[SKILL.md](skills/skill-creator/SKILL.md) ·
[Apollo Skills](skills/skill-creator/references/apollo-skills.md)

---

## Usage

Skills activate automatically once installed. The agent uses them when relevant tasks are detected.

## Skill Structure

Each skill contains:

- `SKILL.md` - Instructions for the agent (required)
- `references/` - Supporting documentation (optional)

## Contributing

Have a skill idea for the Solutions or Field teams? See [CONTRIBUTING.md](CONTRIBUTING.md) to get started.

## Resources

- [Apollo Client Documentation](https://www.apollographql.com/docs/react/)
- [Apollo Server Documentation](https://www.apollographql.com/docs/apollo-server/)
- [Apollo Connectors Documentation](https://www.apollographql.com/docs/graphos/schema-design/connectors/)
- [Apollo Federation Documentation](https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/)
- [Apollo MCP Server](https://www.apollographql.com/docs/apollo-mcp-server/)
- [Rover CLI Documentation](https://www.apollographql.com/docs/rover/)
- [Official Apollo Skills Repository](https://github.com/apollographql/skills)

## Disclaimer

The code in this repository is experimental and for reference purposes only. Community feedback is welcome but this project is not officially supported in the same way that repositories in the official [Apollo GraphQL GitHub organization](https://github.com/apollographql) are. If you need help you can file an issue on this repository, [contact Apollo](https://www.apollographql.com/contact-sales) to talk to an expert, or create a ticket directly in Apollo Studio.
