# Typeform MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Typeform via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-typeform`
* Runtime: Model Context Protocol (MCP) Server
* Category: Forms and Surveys
* Target Host: `api.typeform.com`
* Authentication: personal access token (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token (GET /me) | Autonomous Execution |
| `forms` | list forms | Autonomous Execution |
| `form-get` | one form + its fields | Autonomous Execution |
| `responses` | list form responses | Autonomous Execution |
| `webhooks-list` | list the form's webhooks | Autonomous Execution |
| `webhook-create` | Execute webhook-create command. | Supervised Execution |
| `webhook-delete` | Execute webhook-delete command. | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
