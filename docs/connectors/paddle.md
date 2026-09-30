# Paddle MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Paddle via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-paddle`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.paddle.com`
* Authentication: Paddle API key (per-user, Paddle Dashboard \u2192 Developer Tools \u2192 Authentication)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (via event-types) | Autonomous Execution |
| `transactions` | recent transactions | Autonomous Execution |
| `customers` | customers | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
