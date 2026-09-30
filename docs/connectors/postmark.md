# Postmark MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Postmark via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-postmark`
* Runtime: Model Context Protocol (MCP) Server
* Category: Email and Marketing
* Target Host: `api.postmarkapp.com`
* Authentication: server API token (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the server token | Autonomous Execution |
| `send` | Execute send command. | Supervised Execution |
| `messages` | recent outbound messages | Autonomous Execution |
| `bounces` | recent bounces | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
