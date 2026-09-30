# Ideogram MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Ideogram via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-ideogram`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.ideogram.ai`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key (free balance read) | Autonomous Execution |
| `balance` | read billing balance (free) | Autonomous Execution |
| `generate` | Execute generate command. | Autonomous Execution |
| `edit` | Magic Fill edit | Supervised Execution |
| `remix` | style transfer | Autonomous Execution |
| `upscale` | upscale | Autonomous Execution |
| `describe` | describe an image | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
