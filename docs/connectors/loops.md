# Loops MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Loops via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-loops`
* Runtime: Model Context Protocol (MCP) Server
* Category: Email and Marketing
* Target Host: `app.loops.so`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `find` | look up a contact | Autonomous Execution |
| `create` | add a contact | Supervised Execution |
| `upsert` | create or update | Autonomous Execution |
| `event` | fire an event | Autonomous Execution |
| `send-email` | transactional email | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
