# Ramp MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Ramp via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-ramp`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.ramp.com`
* Authentication: OAuth 2.0 client credentials (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the credential | Autonomous Execution |
| `transactions` | list transactions | Autonomous Execution |
| `transactions` | Execute transactions command. | Autonomous Execution |
| `transaction-get` | one transaction | Autonomous Execution |
| `cards` | list cards | Autonomous Execution |
| `card-limits` | spending restrictions on one card | Autonomous Execution |
| `users` | list users | Autonomous Execution |
| `departments` | list departments | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
