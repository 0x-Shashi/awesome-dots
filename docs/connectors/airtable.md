# Airtable MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Airtable via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-airtable`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.airtable.com`
* Authentication: Airtable personal access token (per-user, airtable.com/create/tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `bases` | list bases (name, id) | Autonomous Execution |
| `records` | read records (flattened fields), 10 max | Autonomous Execution |
| `records` | Execute records command. | Autonomous Execution |
| `create` | Execute create command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
