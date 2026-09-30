# Openrouter MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Openrouter via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-openrouter`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `openrouter.ai`
* Authentication: API key (per-user, openrouter.ai/keys)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `models` | model catalog (id, name, prompt price) | Autonomous Execution |
| `key` | your key's label, usage, limit | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
