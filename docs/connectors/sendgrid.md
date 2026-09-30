# Sendgrid MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Sendgrid via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-sendgrid`
* Runtime: Model Context Protocol (MCP) Server
* Category: Email and Marketing
* Target Host: `api.sendgrid.com`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `send` | Execute send command. | Supervised Execution |
| `stats` | email stats for the last 7 days | Autonomous Execution |
| `stats` | stats from a date | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
