# Supermemory MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Supermemory via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-supermemory`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.supermemory.ai`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `add` | store a memory | Autonomous Execution |
| `search` | hybrid search | Autonomous Execution |
| `list` | list stored documents | Autonomous Execution |
| `upload` | upload a file | Supervised Execution |
| `settings` | tune extraction/chunking | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
