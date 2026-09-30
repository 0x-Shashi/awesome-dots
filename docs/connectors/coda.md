# Coda MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Coda via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-coda`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `coda.io`
* Authentication: personal API token (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token (whoami) | Autonomous Execution |
| `docs` | list docs | Autonomous Execution |
| `tables` | list tables in a doc | Autonomous Execution |
| `rows` | read rows from a table | Autonomous Execution |
| `add-row` | add a row | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
