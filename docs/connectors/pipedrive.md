# Pipedrive MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Pipedrive via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-pipedrive`
* Runtime: Model Context Protocol (MCP) Server
* Category: Sales and CRM
* Target Host: `{company}.pipedrive.com`
* Authentication: personal API token (per-user) + company subdomain

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API token | Autonomous Execution |
| `deals` | list deals | Autonomous Execution |
| `deals` | filter by status | Autonomous Execution |
| `persons` | list contacts | Autonomous Execution |
| `create-deal` | Execute create-deal command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
