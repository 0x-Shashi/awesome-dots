# Twitch MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Twitch via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-twitch`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.twitch.tv`
* Authentication: provider OAuth via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token (returns own profile) | Autonomous Execution |
| `user` | channel profile (omit --login for own) | Autonomous Execution |
| `followers` | follower count + recent followers | Autonomous Execution |
| `stream` | live now? viewer count, title, game | Autonomous Execution |
| `videos` | past broadcasts and clips | Autonomous Execution |
| `channel-update` | confirm first | Supervised Execution |
| `clip-create` | confirm first | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
