# Todoist MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Todoist via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-todoist`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.todoist.com`
* Authentication: Todoist API token (per-user, Settings \u2192 Integrations \u2192 Developer)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `tasks` | list tasks (content, due date, priority, project) | Autonomous Execution |
| `create` | create a task | Supervised Execution |
| `complete` | mark a task done | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
