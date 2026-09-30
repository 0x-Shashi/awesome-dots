# Resend MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Resend via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-resend`
* Runtime: Model Context Protocol (MCP) Server
* Category: Email and Marketing
* Target Host: `api.resend.com`
* Authentication: Resend API key (per-user, resend.com/api-keys)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `send` | Execute send command. | Supervised Execution |
| `get` | check delivery status of a sent email | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
