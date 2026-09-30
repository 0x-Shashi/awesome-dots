# Railway MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Railway via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-railway`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `backboard.railway.com`
* Authentication: API token (account or workspace)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the token | Autonomous Execution |
| `projects` | list projects (id, name) | Autonomous Execution |
| `project` | inspect one project | Autonomous Execution |
| `deployments` | list deployments for a project | Supervised Execution |
| `set-var` | set an env var (confirm first) | Autonomous Execution |
| `redeploy` | redeploy a deployment (confirm first) | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
