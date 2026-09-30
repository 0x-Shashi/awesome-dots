# Beatoven MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Beatoven via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-beatoven`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `public-api.beatoven.ai`
* Authentication: API token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify credential setup (no spend) | Autonomous Execution |
| `compose` | Execute compose command. | Autonomous Execution |
| `compose` | Execute compose command. | Autonomous Execution |
| `status` | poll until composed | Autonomous Execution |
| `download` | download the composed track | Autonomous Execution |
| `download` | download from a track URL directly | Autonomous Execution |
| `stems` | list the four stem URLs | Autonomous Execution |
| `stems` | download one stem | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
