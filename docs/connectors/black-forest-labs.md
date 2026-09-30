# Black Forest Labs MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Black Forest Labs via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-black-forest-labs`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.bfl.ai`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify credential setup (no spend) | Autonomous Execution |
| `generate` | submit; prints a polling_url | Autonomous Execution |
| `generate` | Execute generate command. | Autonomous Execution |
| `generate` | Execute generate command. | Autonomous Execution |
| `status` | poll until Ready | Autonomous Execution |
| `result` | fetch the result | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
