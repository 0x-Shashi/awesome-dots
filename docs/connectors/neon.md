# Neon MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Neon via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-neon`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `console.neon.tech`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `projects` | list projects | Autonomous Execution |
| `project-get` | one project | Autonomous Execution |
| `branches` | list branches | Autonomous Execution |
| `branch-create` | Execute branch-create command. | Supervised Execution |
| `branch-delete` | Execute branch-delete command. | User Handoff |
| `databases` | list databases | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
