# Cartesia MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Cartesia via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-cartesia`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.cartesia.ai`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | Execute auth command. | Autonomous Execution |
| `voices` | Execute voices command. | Autonomous Execution |
| `voice-get` | Execute voice-get command. | Autonomous Execution |
| `tts` | Execute tts command. | Autonomous Execution |
| `tts` | Execute tts command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
