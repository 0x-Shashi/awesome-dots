# Mercury MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Mercury via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-mercury`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.mercury.com`
* Authentication: Mercury API token (per-user, app.mercury.com \u2192 Settings \u2192 API Tokens; a Read-Only token suffices)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `accounts` | list bank accounts | Autonomous Execution |
| `transactions` | recent transactions for account A | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
