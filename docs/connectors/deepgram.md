# Deepgram MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Deepgram via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-deepgram`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.deepgram.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | Execute auth command. | Autonomous Execution |
| `projects` | Execute projects command. | Autonomous Execution |
| `transcribe` | Execute transcribe command. | Autonomous Execution |
| `transcribe` | Execute transcribe command. | Autonomous Execution |
| `tts` | Execute tts command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
