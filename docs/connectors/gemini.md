# Gemini MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Gemini via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-gemini`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `generativelanguage.googleapis.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key (free) | Autonomous Execution |
| `models` | list available models | Autonomous Execution |
| `image` | Nano Banana text-to-image (or edit with --image) | Autonomous Execution |
| `image` | Execute image command. | Autonomous Execution |
| `imagen` | Imagen 4 | Autonomous Execution |
| `video` | Veo 3.1, prints an operation id | Autonomous Execution |
| `op-status` | poll the Veo operation | Autonomous Execution |
| `tts` | text-to-speech | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
