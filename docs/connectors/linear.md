# Linear MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Linear via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-linear`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `api.linear.app`
* Authentication: Linear personal API key (per-user, linear.app/settings/api)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (viewer query) | Autonomous Execution |
| `issues` | your assigned issues (title, state, team) | Autonomous Execution |
| `create` | Execute create command. | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
