# Apollo MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Apollo via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-apollo`
* Runtime: Model Context Protocol (MCP) Server
* Category: Sales and CRM
* Target Host: `api.apollo.io`
* Authentication: API key (per-user; Professional plan or higher)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `search` | search people | Autonomous Execution |
| `enrich` | enrich one person (uses credits) | Autonomous Execution |
| `org-enrich` | enrich one company | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
