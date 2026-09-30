# Vapi MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Vapi via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-vapi`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.vapi.ai`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `assistants` | list assistants | Autonomous Execution |
| `assistant-get` | one assistant | Autonomous Execution |
| `phone-numbers` | list phone numbers | Autonomous Execution |
| `call-create` | Execute call-create command. | Supervised Execution |
| `call-get` | one call | Autonomous Execution |
| `call-list` | list calls | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
