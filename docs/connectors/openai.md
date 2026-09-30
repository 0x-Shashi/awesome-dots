# Openai MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Openai via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-openai`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.openai.com`
* Authentication: OpenAI API key (per-user, platform.openai.com/api-keys)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `models` | list models available to this key (id, owned_by), truncated to 40 | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
