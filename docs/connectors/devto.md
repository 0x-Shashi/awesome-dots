# Devto MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Devto via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-devto`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `dev.to`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | verify the API key | Autonomous Execution |
| `my-articles` | published articles | Autonomous Execution |
| `my-articles` | published + drafts | Autonomous Execution |
| `articles-by-user` | public reads, no key needed | Autonomous Execution |
| `article-create` | draft by default | Supervised Execution |
| `article-create` | confirm first: goes live | Supervised Execution |
| `article-update` | confirm first | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
