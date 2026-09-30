# Firecrawl MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Firecrawl via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-firecrawl`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.firecrawl.dev`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key (costs one map call) | Autonomous Execution |
| `scrape` | scrape one page to markdown | Autonomous Execution |
| `crawl` | start a crawl; returns a job id | Autonomous Execution |
| `crawl-status` | poll a crawl job | Autonomous Execution |
| `map` | list URLs on a site | Autonomous Execution |
| `search` | web search | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
