# Notion MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Notion via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-notion`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.notion.com`
* Authentication: Notion internal integration token (per-user, created at notion.so/my-integrations)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (search with page_size 1) | Autonomous Execution |
| `search` | search pages and databases | Autonomous Execution |
| `page` | read a page's properties | Autonomous Execution |
| `query-db` | query a database (first 20 rows) | Autonomous Execution |
| `page-create` | Execute page-create command. | Supervised Execution |
| `page-create` | Execute page-create command. | Supervised Execution |
| `block-append` | Execute block-append command. | Autonomous Execution |
| `page-update` | Execute page-update command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
