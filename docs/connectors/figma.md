# Figma MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Figma via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-figma`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.figma.com`
* Authentication: Figma personal access token (per-user, Figma Settings \u2192 Personal access tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | authenticated user (handle, email) | Autonomous Execution |
| `file` | file metadata: name, lastModified, version, thumbnailUrl | Autonomous Execution |
| `comment` | Execute comment command. | Autonomous Execution |
| `comment` | Execute comment command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
