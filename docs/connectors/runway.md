# Runway MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Runway via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-runway`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.dev.runwayml.com`
* Authentication: API secret via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify credential setup (no spend) | Autonomous Execution |
| `text-to-video` | Execute text-to-video command. | Autonomous Execution |
| `image-to-video` | Execute image-to-video command. | Autonomous Execution |
| `task-status` | poll until SUCCEEDED/FAILED | Autonomous Execution |
| `upscale` | upscale a video | Autonomous Execution |
| `lip-sync` | lip-sync a video | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
