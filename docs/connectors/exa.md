# Exa MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Exa via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-exa`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.exa.ai`
* Authentication: Exa API key (per-user, dashboard.exa.ai/api-keys)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `search` | search with page text | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
