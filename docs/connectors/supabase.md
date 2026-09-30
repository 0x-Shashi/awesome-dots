# Supabase MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Supabase via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-supabase`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `<ref>.supabase.co`
* Authentication: service_role key (per-user, project Settings \u2192 API)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `status` | Verify connection to supabase. | Autonomous Execution |
| `query` | Retrieve data from supabase. | Autonomous Execution |
| `execute` | Perform action in supabase. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
