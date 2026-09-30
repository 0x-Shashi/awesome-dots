# Canva MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Canva via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-canva`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.canva.com`
* Authentication: provider OAuth 2.0 + PKCE via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (prints the Canva user) | Autonomous Execution |
| `designs` | list designs, optional search | Autonomous Execution |
| `design` | get one design's details | Autonomous Execution |
| `folders` | list folders | Autonomous Execution |
| `folder-items` | list items in a folder | Autonomous Execution |
| `assets` | list uploaded assets | Autonomous Execution |
| `create` | Execute create command. | Supervised Execution |
| `upload-asset` | upload a local file as an asset | Supervised Execution |
| `upload-asset` | import an asset from a URL | Supervised Execution |
| `export` | submit an async export job (png, jpg, pdf, mp4, ...) | Autonomous Execution |
| `export-status` | poll the export job; prints download URLs when done | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
