# Ticktick MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Ticktick via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-ticktick`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.ticktick.com`
* Authentication: OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `projects` | list task lists | Autonomous Execution |
| `project-data` | tasks in one list | Autonomous Execution |
| `task-create` | Execute task-create command. | Supervised Execution |
| `task-complete` | Execute task-complete command. | Autonomous Execution |
| `task-delete` | Execute task-delete command. | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
