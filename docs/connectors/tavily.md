# Tavily MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Tavily via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-tavily`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.tavily.com`
* Authentication: Tavily API key (per-user, tavily.com)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `search` | Execute search command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
