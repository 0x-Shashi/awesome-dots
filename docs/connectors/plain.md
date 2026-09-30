# Plain MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Plain via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-plain`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `core-api.uk.plain.com`
* Authentication: Machine-user API key

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the Machine User API key | Autonomous Execution |
| `customer-find` | find a customer by email | Autonomous Execution |
| `threads` | list threads (Relay cursor pagination, max 100 per page) | Autonomous Execution |
| `customer-upsert` | create or update a customer | Autonomous Execution |
| `thread-create` | open a support thread | Supervised Execution |
| `thread-reply` | reply to a thread | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
