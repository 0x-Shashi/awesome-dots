# Elevenlabs MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Elevenlabs via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-elevenlabs`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.elevenlabs.io`
* Authentication: ElevenLabs API key (per-user, elevenlabs.io/app/settings/api-keys)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | subscription tier, character_count, character_limit | Autonomous Execution |
| `voices` | available voices (name, category) | Autonomous Execution |
| `text-to-speech` | Execute text-to-speech command. | Autonomous Execution |
| `text-to-speech` | Execute text-to-speech command. | Autonomous Execution |
| `text-to-speech` | Execute text-to-speech command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
