# Clickup MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Clickup via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-clickup`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.clickup.com`
* Authentication: ClickUp personal API token (per-user, Settings \u2192 Apps \u2192 API Token)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `teams` | workspaces (id, name) | Autonomous Execution |
| `tasks` | tasks in a list (name, status, due date) | Autonomous Execution |
| `create` | create a task | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
