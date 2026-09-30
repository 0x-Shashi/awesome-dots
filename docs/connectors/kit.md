# Kit MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Kit via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-kit`
* Runtime: Model Context Protocol (MCP) Server
* Category: Email and Marketing
* Target Host: `api.kit.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `subscribers` | list subscribers | Autonomous Execution |
| `broadcasts` | list broadcasts | Autonomous Execution |
| `broadcast-create` | create a broadcast draft | Supervised Execution |
| `broadcast-create` | send to the list (confirm first) | Supervised Execution |
| `sequences` | list sequences | Autonomous Execution |
| `tags` | list tags | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
