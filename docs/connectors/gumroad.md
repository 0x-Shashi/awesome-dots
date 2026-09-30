# Gumroad MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Gumroad via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-gumroad`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `api.gumroad.com`
* Authentication: Gumroad access token (per-user, app.gumroad.com \u2192 Settings \u2192 Advanced)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `products` | list products | Autonomous Execution |
| `sales` | recent sales | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
