# Discord MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Discord via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-discord`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `discord.com`
* Authentication: Bot token (per-server install)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the bot token | Autonomous Execution |
| `guilds` | list servers the bot joined | Autonomous Execution |
| `channels` | list channels in a server | Autonomous Execution |
| `history` | read recent messages | Autonomous Execution |
| `send` | post a message | Supervised Execution |
| `dm` | open a DM and send | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
