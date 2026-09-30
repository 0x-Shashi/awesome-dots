# Podbean MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Podbean via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-podbean`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.podbean.com`
* Authentication: provider OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `podcasts` | list podcasts on the account | Autonomous Execution |
| `episodes` | list episodes | Autonomous Execution |
| `episode-create` | Execute episode-create command. | Supervised Execution |
| `episode-update` | Execute episode-update command. | Supervised Execution |
| `episode-delete` | delete (confirm first) | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
