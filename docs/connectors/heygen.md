# Heygen MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Heygen via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-heygen`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.heygen.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key (free) | Autonomous Execution |
| `avatars` | list stock avatars (custom avatar IDs come from the app) | Autonomous Execution |
| `voices` | list voices | Autonomous Execution |
| `video-agent` | one-shot prompt-to-video | Autonomous Execution |
| `video-generate` | multi-scene | Autonomous Execution |
| `video-status` | poll until completed | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
