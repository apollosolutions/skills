# Apollo product landscape

Use this map to route customer questions to the right documentation. All URLs are on the public [Apollo documentation](https://www.apollographql.com/docs/) site. Prefer the latest stable doc paths returned by **Apollo Docs Search** if a link moves.

## Graph platform and schema

| Product | What it is | Doc entry | Common question topics |
| --- | --- | --- | --- |
| **GraphOS** | Apollo’s platform for managing graphs, schema delivery, checks, and operations | [GraphOS Platform](https://www.apollographql.com/docs/graphos/) | Launches, variants, Studio, contracts, metrics, proposals |
| **Federation** | Composing multiple subgraphs into one supergraph | [Federated schemas](https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/) | `@key`, entities, composition, subgraph patterns |
| **Connectors** | Declarative integration of REST and other APIs into the graph | [Connectors](https://www.apollographql.com/docs/graphos/connectors/) | Mapping, `@connect`, batching, errors |
| **Schema design** | Naming, nullability, entities, evolution | [Schema design](https://www.apollographql.com/docs/graphos/schema-design/) | Best practices, deprecations, demand-oriented design |

## Routing and gateway

| Product | What it is | Doc entry | Common question topics |
| --- | --- | --- | --- |
| **Apollo Router** | Rust-based GraphQL router / gateway (GraphOS Router / Apollo Router Core) | [Routing](https://www.apollographql.com/docs/graphos/routing/) | YAML config, coprocessors, Rhai, security, telemetry, subscriptions, self-hosted deploy |
| **Cloud Routing** | GraphOS-managed cloud routers for cloud supergraphs | [Cloud Routing](https://www.apollographql.com/docs/graphos/cloud-routing/) | Cloud supergraphs, router status, configuration, plan-specific behavior (see current docs) |

## Server and subgraphs

| Product | What it is | Doc entry | Common question topics |
| --- | --- | --- | --- |
| **Apollo Server** | Node.js GraphQL server | [Apollo Server](https://www.apollographql.com/docs/apollo-server/) | Plugins, context, subscriptions, deployment, federation subgraph setup |

## Clients

| Product | What it is | Doc entry | Common question topics |
| --- | --- | --- | --- |
| **Apollo Client (Web)** | GraphQL client for browser and Node | [Apollo Client](https://www.apollographql.com/docs/react/) | Queries, cache, links, React hooks, error handling |
| **Apollo iOS** | Native iOS client | [Apollo iOS](https://www.apollographql.com/docs/ios/) | Codegen, caching, Swift |
| **Apollo Kotlin** | Android / Kotlin client | [Apollo Kotlin](https://www.apollographql.com/docs/kotlin/) | Gradle plugin, normalized cache |

## Tooling and operations

| Product | What it is | Doc entry | Common question topics |
| --- | --- | --- | --- |
| **Rover CLI** | CLI for graphs, subgraphs, supergraphs, and related workflows | [Rover CLI](https://www.apollographql.com/docs/rover/) | `subgraph`, `supergraph`, `graph`, auth, CI/CD |
| **Apollo MCP Server** | MCP server for exposing GraphQL operations as tools to AI clients | [Apollo MCP Server](https://www.apollographql.com/docs/apollo-mcp-server/) | Config, tools, deployment, security |
| **GraphOS MCP Tools** | Hosted MCP tools for docs search/read and Connectors spec | [GraphOS MCP Tools](https://www.apollographql.com/docs/graphos/platform/graphos-mcp-tools/) | `mcp.apollographql.com`, Claude/Cursor setup |
| **Apollo Operator** | Kubernetes operator for supergraphs | [Apollo Operator](https://www.apollographql.com/docs/apollo-operator/) | CRDs, subgraphs, clusters |

## IDE and developer experience

| Product | What it is | Doc entry | Common question topics |
| --- | --- | --- | --- |
| **IDE support** | Editor extensions for GraphQL | [IDE support](https://www.apollographql.com/docs/ide-support/) | VS Code, JetBrains, Vim (links to schema-design IDE pages) |

## OSS vs enterprise framing

- **OSS:** Apollo Server, Router, Rover, Federation libraries, and public client libraries are documented in the open docs above.
- **GraphOS / cloud:** Features such as schema checks, launches, Studio, and managed routing are documented under GraphOS; some capabilities are plan-dependent. When unsure, link the doc and note that exact entitlement may depend on their contract.

## Quick disambiguation

- **“Gateway” or “edge”** → Often **Apollo Router** (self-hosted) or **Cloud Routing** (GraphOS-managed); confirm which they use.
- **“Studio” or “schema publish”** → **GraphOS** schema management and Rover publish flows.
- **“Subgraph” errors** → **Federation** composition and subgraph libraries.
- **“Connect REST”** → **Connectors** (not the same as generic REST in resolvers).

When in doubt, run **Apollo Docs Search** with the customer’s exact product name and symptom before picking a single landing page.
