# Transistor MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Transistor via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-transistor`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.transistor.fm`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `shows` | list your shows | Autonomous Execution |
| `episodes` | list episodes of a show | Autonomous Execution |
| `episode-create` | Execute episode-create command. | Supervised Execution |
| `episode-update` | update title/description | Supervised Execution |
| `episode-delete` | delete an episode | User Handoff |
| `authorize-upload` | step 1 of audio upload (prints raw JSON) | Supervised Execution |
| `upload` | Execute upload command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
