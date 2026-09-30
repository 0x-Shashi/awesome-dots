# Cloudinary MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Cloudinary via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-cloudinary`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.cloudinary.com`
* Authentication: cloud_name + API key + secret via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (also shows plan usage) | Autonomous Execution |
| `usage` | plan usage: credits, storage, bandwidth, transformations | Autonomous Execution |
| `upload` | upload an image | Supervised Execution |
| `upload` | upload a video | Supervised Execution |
| `upload` | upload into a folder | Supervised Execution |
| `list` | list image assets | Autonomous Execution |
| `get` | asset details | Autonomous Execution |
| `update` | Execute update command. | Supervised Execution |
| `delete` | delete an asset | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
