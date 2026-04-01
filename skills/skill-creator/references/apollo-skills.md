# Creating Apollo Solutions Skills

This guide provides specific guidance for creating skills in the Apollo Solutions skills repository.

## Repository Structure

Apollo Solutions skills live in the `skills/` directory:

```
skills/
├── skill-creator/
└── your-new-skill/
```

## Skill Categories

### Solutions Skills

Skills for Apollo Solutions and Field team use cases:

- Customer implementation patterns and workflows
- Experimental features or integrations
- Field-tested configurations and approaches
- Cross-product integration patterns

### Convention Skills

Skills for GraphQL conventions and best practices relevant to Solutions work:

- Schema design patterns
- Query and mutation patterns
- Performance optimization approaches

## Description Patterns

Use consistent trigger patterns in descriptions:

```yaml
# Solutions skill pattern
description: >
  Help users implement [what] with [approach]. Use this skill when:
  (1) implementing [use case] for a customer,
  (2) working with [pattern] in a solutions context,
  (3) troubleshooting [common issue],
  (4) working with files containing [identifier].

# Convention skill pattern
description: >
  Guide for [topic] following best practices. Use this skill when:
  (1) designing new [thing],
  (2) reviewing existing [thing] for improvements,
  (3) implementing [pattern],
  (4) ensuring [quality aspect].
```

## Process Structure

Use a consistent process structure with checkboxes:

```markdown
## Process

Follow this process. **DO NOT skip any steps.**

### Step 1: Research

- [ ] Understand the requirements
- [ ] Ask the user for clarification if needed
- [ ] Fetch relevant documentation
- [ ] DO NOT write code until research is complete

### Step 2: Implement

- [ ] Create the solution using patterns below
- [ ] Follow the reference files for detailed guidance

### Step 3: Validate

- [ ] Run validation commands
- [ ] Fix any errors before proceeding

### Step 4: Test

- [ ] Create or update tests
- [ ] Verify the solution works correctly
```

## Code Examples

### GraphQL Schema Examples

```graphql
"""
A user in the system.
"""
type User {
  id: ID!
  email: String!
  name: String
  posts(first: Int = 10, after: String): PostConnection!
}
```

### TypeScript Examples

```typescript
import { ApolloClient, InMemoryCache } from "@apollo/client";

const client = new ApolloClient({
  uri: "https://api.example.com/graphql",
  cache: new InMemoryCache(),
});
```

### Rover CLI Examples

```bash
# Publish a subgraph
rover subgraph publish my-graph@current \
  --name products \
  --schema ./schema.graphql

# Run local development
rover dev --supergraph-config supergraph.yaml
```

## Reference File Organization

Organize reference files by topic:

```
references/
├── setup.md           # Installation and quick start
├── patterns.md        # Common patterns and examples
├── troubleshooting.md # Common errors and solutions
└── api.md             # API reference
```

## Ground Rules Format

Use consistent formatting for ground rules:

```markdown
## Ground Rules

- NEVER make up syntax not in the specification
- NEVER skip validation steps
- ALWAYS ask for clarification when requirements are unclear
- ALWAYS validate with appropriate commands after changes
- PREFER [recommended approach] over [alternative]
- USE [tool/pattern] for [specific use case]
```

## Documentation Links

Include links to official Apollo documentation:

```markdown
## Resources

- [Apollo Client Documentation](https://www.apollographql.com/docs/react/)
- [Apollo Server Documentation](https://www.apollographql.com/docs/apollo-server/)
- [Apollo Connectors Documentation](https://www.apollographql.com/docs/graphos/schema-design/connectors/)
- [Rover CLI Documentation](https://www.apollographql.com/docs/rover/)
```

## Experimental Skills

Skills in this repository may be experimental. When creating an experimental skill:

- Note the experimental status in the `compatibility` field
- Document any known limitations in a `## Known Limitations` section
- Include a disclaimer in the skill description if appropriate

```yaml
compatibility: Experimental. Works with Claude Code and similar AI coding assistants. Not officially supported.
```

## Validation Checklist

Before submitting a new Apollo Solutions skill:

- [ ] Skill follows the Agent Skills specification
- [ ] Description includes numbered trigger conditions
- [ ] `metadata.author` is set to `apollosolutions`
- [ ] Code examples use current API versions
- [ ] Commands include required flags and options
- [ ] Links to official Apollo documentation are correct
- [ ] Content follows Apollo Voice guidelines
- [ ] Known limitations are documented if applicable
