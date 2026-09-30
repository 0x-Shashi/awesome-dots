# Brave Search MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Brave Search via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-brave-search`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.search.brave.com`
* Authentication: Brave Search API key (per-user, brave.com/search/api; free tier 2,000 queries/month)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `search` | web search | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
