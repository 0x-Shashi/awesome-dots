# X MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for X via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-x`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `api.x.com`
* Authentication: OAuth2 PKCE (per-user; paid read access)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `post` | post a tweet | Supervised Execution |
| `search` | search recent tweets | Autonomous Execution |
| `like` | like a tweet (resolves your user ID first) | Autonomous Execution |
| `dm` | send a DM | Autonomous Execution |
| `delete` | delete a tweet | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
