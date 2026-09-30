# Posthog MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Posthog via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-posthog`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `configurable`
* Authentication: personal API key (per-user, PostHog Settings \u2192 Personal API keys; starts `phx_`)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | verify the connection | Autonomous Execution |
| `projects` | list projects | Autonomous Execution |
| `insights` | saved insights in a project | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
