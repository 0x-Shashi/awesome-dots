# Render MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Render via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-render`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.render.com`
* Authentication: API key (per-user, dashboard.render.com \u2192 Account Settings \u2192 API Keys)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `services` | list services (name, type, region) | Autonomous Execution |
| `deploys` | recent deploys (status, created) | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
