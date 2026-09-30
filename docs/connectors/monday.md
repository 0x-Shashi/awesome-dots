# Monday MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Monday via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-monday`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.monday.com`
* Authentication: personal API token (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token | Autonomous Execution |
| `boards` | list boards | Autonomous Execution |
| `items` | list items on a board | Autonomous Execution |
| `create-item` | create an item | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
