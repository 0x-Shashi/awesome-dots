# Unsplash MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Unsplash via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-unsplash`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.unsplash.com`
* Authentication: access key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `search` | search photos | Autonomous Execution |
| `search` | Execute search command. | Autonomous Execution |
| `list` | latest photos | Autonomous Execution |
| `photo` | one photo's details and URLs | Autonomous Execution |
| `user-photos` | a photographer's photos | Autonomous Execution |
| `topic` | photos in a topic | Autonomous Execution |
| `download` | download an image file | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
