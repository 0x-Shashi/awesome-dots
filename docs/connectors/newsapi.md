# Newsapi MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Newsapi via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-newsapi`
* Runtime: Model Context Protocol (MCP) Server
* Category: Data Services
* Target Host: `newsapi.org`
* Authentication: NewsAPI key (per-user, newsapi.org/register; free tier 100 requests/day)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `headlines` | top headlines | Autonomous Execution |
| `search` | search all news | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
