# Slack MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Slack via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-slack`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `slack.com`
* Authentication: Slack OAuth (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (auth.test) | Autonomous Execution |
| `channels` | list channels (public + private) | Autonomous Execution |
| `history` | recent messages in a channel | Autonomous Execution |
| `post` | post a message | Supervised Execution |
| `users` | list workspace users | Autonomous Execution |
| `search` | search messages (needs search:read on the token) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
