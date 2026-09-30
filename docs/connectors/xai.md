# Xai MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Xai via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-xai`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.x.ai`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `models` | list available foundation models | Autonomous Execution |
| `chat` | one completion (spends tokens) | Autonomous Execution |
| `chat` | Execute chat command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
