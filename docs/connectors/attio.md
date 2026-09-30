# Attio MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Attio via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-attio`
* Runtime: Model Context Protocol (MCP) Server
* Category: Sales and CRM
* Target Host: `api.attio.com`
* Authentication: API key (per-workspace)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `objects` | list available objects | Autonomous Execution |
| `query` | query records | Autonomous Execution |
| `upsert` | create or update a record | Autonomous Execution |
| `note` | add a note | Autonomous Execution |
| `task` | add a task | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
