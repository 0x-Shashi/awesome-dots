# Veed MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Veed via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-veed`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `the host you pass via --api-host`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | check readiness (no free status endpoint) | Autonomous Execution |
| `background-remove` | Execute background-remove command. | User Handoff |
| `background-remove` | Execute background-remove command. | User Handoff |
| `background-remove` | Execute background-remove command. | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
