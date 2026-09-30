# Asana MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Asana via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-asana`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `app.asana.com`
* Authentication: Asana personal access token (per-user, My Settings \u2192 Apps \u2192 Manage Developer Apps)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | verify the connection, shows user gid | Autonomous Execution |
| `tasks` | tasks assigned to me | Autonomous Execution |
| `create` | create a task | Supervised Execution |
| `create` | Execute create command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
