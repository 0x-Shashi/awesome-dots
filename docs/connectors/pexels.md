# Pexels MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Pexels via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-pexels`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.pexels.com`
* Authentication: free API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection | Autonomous Execution |
| `search` | search photos | Autonomous Execution |
| `search` | Execute search command. | Autonomous Execution |
| `curated` | trending photos, updated hourly | Autonomous Execution |
| `photo` | one photo's details and file URLs | Autonomous Execution |
| `search-videos` | search videos | Autonomous Execution |
| `popular-videos` | popular videos | Autonomous Execution |
| `video` | one video's details and file URLs | Autonomous Execution |
| `collection` | contents of a collection | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
