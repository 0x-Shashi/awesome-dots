# Luma MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Luma via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-luma`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.lumalabs.ai`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key (free) | Autonomous Execution |
| `generate` | submit a generation | Autonomous Execution |
| `generate` | image-to-video | Autonomous Execution |
| `generate` | Execute generate command. | Autonomous Execution |
| `status` | poll (no faster than every 5s) | Autonomous Execution |
| `cancel` | cancel a queued/running generation | User Handoff |
| `upload` | upload an image for reference frames | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
