# Home Assistant MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Home Assistant via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-home-assistant`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `your instance host`
* Authentication: Home Assistant long-lived access token (per-user, Profile \u2192 Security \u2192 Long-Lived Access Tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to home-assistant. | Autonomous Execution |
| `query` | Retrieve data from home-assistant. | Autonomous Execution |
| `execute` | Perform action in home-assistant. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
