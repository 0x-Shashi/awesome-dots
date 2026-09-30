# Youtube MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Youtube via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-youtube`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `www.googleapis.com`
* Authentication: OAuth 2.0 (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `channel` | show a channel | Autonomous Execution |
| `video` | show a video | Autonomous Execution |
| `search` | search videos | Autonomous Execution |
| `playlist-items` | list playlist items | Autonomous Execution |
| `upload` | Execute upload command. | Supervised Execution |
| `comment` | Execute comment command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
