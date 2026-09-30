# Zep MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Zep via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-zep`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.getzep.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `user-create` | create a user container | Supervised Execution |
| `thread-create` | create a thread | Supervised Execution |
| `message-add` | append a message | Autonomous Execution |
| `context` | distilled facts for the thread | Autonomous Execution |
| `messages` | conversation history | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
