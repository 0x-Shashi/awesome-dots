# Uber Direct MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Uber Direct via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-uber-direct`
* Runtime: Model Context Protocol (MCP) Server
* Category: Business Services
* Target Host: `api.uber.com`
* Authentication: provider OAuth 2.0 client-credentials via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the credentials | Autonomous Execution |
| `quote` | Execute quote command. | Autonomous Execution |
| `dispatch` | Execute dispatch command. | Autonomous Execution |
| `get` | Execute get command. | Autonomous Execution |
| `cancel` | Execute cancel command. | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
