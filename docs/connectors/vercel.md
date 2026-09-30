# Vercel MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Vercel via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-vercel`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.vercel.com`
* Authentication: personal token (per-user, vercel.com/account/tokens)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | verify the connection (your user) | Autonomous Execution |
| `projects` | list projects (name, framework) | Autonomous Execution |
| `deployments` | recent deployments (url, state) | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
