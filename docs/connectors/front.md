# Front MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Front via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-front`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `api2.frontapp.com`
* Authentication: Front API token (per-user, Front Settings \u2192 API)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `inboxes` | list inboxes (name, address) | Autonomous Execution |
| `conversations` | recent conversations (subject, status) | Autonomous Execution |
| `teammates` | teammates (id, name, email) | Autonomous Execution |
| `reply` | Execute reply command. | Autonomous Execution |
| `reply` | Execute reply command. | Autonomous Execution |
| `assign` | Execute assign command. | Autonomous Execution |
| `assign` | Execute assign command. | Autonomous Execution |
| `tag` | Execute tag command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
