# Question patterns and search strategies

Use this file with [apollo-product-landscape.md](apollo-product-landscape.md). All research must stay on **public** Apollo documentation (GraphOS MCP Tools or WebFetch).

## Tools by step

| Step | Prefer (MCP available) | If MCP unavailable |
| --- | --- | --- |
| Broad topic | `ApolloDocsSearch` | WebFetch a section index or landscape doc URL from the product map |
| Deep page / reference | `ApolloDocsRead` | WebFetch the specific doc URL |
| Connectors authoring | `ApolloDocsSearch` + `ApolloConnectorsSpec` | WebFetch Connectors docs + spec pages linked from docs |

## Categories

### Setup and installation

- **Goal:** Install or bootstrap a component.
- **First query examples:** `"Apollo Router install Docker"`, `"Rover install authenticate"`, `"Apollo Server getting started"`.
- **Typical doc sections:** Quickstart, install, prerequisites.
- **Watchouts:** OS, package manager, and cloud provider vary; ask one clarifying question if the environment is missing.

### Configuration

- **Goal:** YAML, env vars, CLI flags, or config files.
- **First query examples:** `"Apollo Router yaml reference"`, `"Router coprocessor configuration"`, `"Apollo Server plugin"`.
- **Typical doc sections:** Configuration reference, feature guides.
- **Watchouts:** Router and GraphOS options change by version; pull the exact snippet from **Apollo Docs Read** or WebFetch.

### Troubleshooting

- **Goal:** Errors, unexpected behavior, or integration failures.
- **First query examples:** Use the **error string** or **log keyword** plus product name: `"Router subgraph error"`, `"composition error"`.
- **Typical doc sections:** Troubleshooting, errors reference, federation hints.
- **Watchouts:** Without versions and repro steps, give doc-based checks only and suggest escalation for root cause. If behavior matches a **bug**, **regression**, or **undocumented gap**, recommend reporting at [support.apollographql.com](https://support.apollographql.com) (see main `SKILL.md`).

### Migration

- **Goal:** Move between major versions or products (e.g. Gateway to Router, Federation 1 to 2).
- **First query examples:** `"migrate Apollo Router v1 v2"`, `"Federation 2 upgrade"`.
- **Typical doc sections:** Upgrade guides, changelog links from docs.
- **Watchouts:** Migrations are high-risk; link the official guide, list breaking changes from docs, and recommend validation in their environment.

### Best practices

- **Goal:** How to design schemas, operate graphs, or secure endpoints.
- **First query examples:** `"GraphOS schema checks"`, `"Router security persisted queries"`, `"demand oriented schema design"`.
- **Typical doc sections:** Schema design guides, production readiness, security.
- **Watchouts:** Distinguish **recommendation** from **requirement**; quote the doc.

### Version and compatibility

- **Goal:** “What version is current?” “Does X work with Y?”
- **First query examples:** `"Apollo Server latest"`, `"Router federation version support"`.
- **Typical doc sections:** Changelog, “What’s new”, compatibility matrices.
- **Watchouts:** Prefer **changelogs or version callouts on the doc page** over training-data memory. If the doc does not state compatibility, say so and link the closest official page.

## Example: well-scoped (good first-pass)

**Question:** “How do I set up GraphOS schema linting?”

- Search: `"GraphOS schema linting"`.
- Read: the linting overview and configuration pages.
- Answer: Short summary + link + any config example from the page.

## Example: needs context

**Question:** “Our router keeps timing out.”

- Ask: Router version, deployment (self-hosted vs cloud), timeout symptom (client vs subgraph), recent config changes.
- Search: `"Apollo Router timeout"` and related terms from their answers.
- Answer: Doc-based timeouts / traffic shaping pointers + link; note escalation if logs are needed.

## Example: escalate

**Question:** “Why was our invoice wrong last quarter?”

- Out of scope for this skill (billing).
- Response: Brief boundary statement + link to [Apollo contact](https://www.apollographql.com/contact-sales) or support channel as appropriate for their relationship; do not invent policy.

## Example: too deep for docs-only

**Question:** “Design our entire federated migration with 40 subgraphs.”

- Acknowledge scope.
- Link high-level migration and federation docs; suggest phased approach **as described in docs** only.
- Recommend human Solutions or architecture engagement; do not produce a bespoke multi-month plan without engagement.
