# Hubspot MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Hubspot via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-hubspot`
* Runtime: Model Context Protocol (MCP) Server
* Category: Sales and CRM
* Target Host: `api.hubapi.com`
* Authentication: HubSpot private app token (per-user, HubSpot Settings \u2192 Integrations \u2192 Private Apps)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `contacts` | list contacts | Autonomous Execution |
| `search-contacts` | search contacts | Autonomous Execution |
| `create-contact` | Execute create-contact command. | Supervised Execution |
| `deals` | list deals | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
