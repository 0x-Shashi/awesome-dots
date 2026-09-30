# Elai MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Elai via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-elai`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `apis.elai.io`
* Authentication: API token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | Execute auth command. | Autonomous Execution |
| `avatars` | Execute avatars command. | Autonomous Execution |
| `videos` | Execute videos command. | Autonomous Execution |
| `video-get` | Execute video-get command. | Autonomous Execution |
| `render` | Execute render command. | Autonomous Execution |
| `render-status` | Execute render-status command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
