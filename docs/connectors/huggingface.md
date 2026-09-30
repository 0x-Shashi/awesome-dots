# Huggingface MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Huggingface via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-huggingface`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `huggingface.co`
* Authentication: Hugging Face user access token (per-user, huggingface.co/settings/tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | whoami: name, email, account type | Autonomous Execution |
| `models` | search the model hub (id, likes, downloads), 10 results | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
