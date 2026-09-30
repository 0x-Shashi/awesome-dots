# Tiktok MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Tiktok via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-tiktok`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `open.tiktokapis.com`
* Authentication: OAuth 2.0 (per-user; TikTok app approval required)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `me` | authorized user's profile | Autonomous Execution |
| `videos` | list the user's videos with stats | Autonomous Execution |
| `videos` | next page | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
