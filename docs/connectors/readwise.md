# Readwise MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Readwise via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-readwise`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `readwise.io`
* Authentication: access token (per-user, from readwise.io/access_token)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token | Autonomous Execution |
| `books` | list books in the library | Autonomous Execution |
| `highlights` | list highlights | Autonomous Execution |
| `highlights` | highlights for one book | Autonomous Execution |
| `add` | save a highlight | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
