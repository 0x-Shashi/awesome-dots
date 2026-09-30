# Anthropic MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Anthropic via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-anthropic`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.anthropic.com`
* Authentication: Anthropic API key (per-user, console.anthropic.com)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `models` | list models available to this key (id, display_name) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
