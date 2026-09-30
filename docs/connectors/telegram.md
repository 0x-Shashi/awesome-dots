# Telegram MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Telegram via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-telegram`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `api.telegram.org`
* Authentication: Telegram bot token from @BotFather (per-user, single token)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | bot identity (getMe) | Autonomous Execution |
| `send` | send a message | Supervised Execution |
| `updates` | recent incoming updates (limit 20) | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
