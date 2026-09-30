# Bluesky MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Bluesky via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-bluesky`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `bsky.social`
* Authentication: App password (per-account; session-based)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the session | Autonomous Execution |
| `profile` | view a profile (add --target to view someone else) | Autonomous Execution |
| `timeline` | home timeline | Autonomous Execution |
| `search` | search posts | Autonomous Execution |
| `post` | publish a post (confirm first) | Supervised Execution |
| `follow` | follow an account (confirm first) | Autonomous Execution |
| `notifications` | list notifications | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
