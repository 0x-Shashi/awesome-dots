# Flyio MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Flyio via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-flyio`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.machines.dev`
* Authentication: API token (app or org scoped)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `apps` | list apps in an org | Autonomous Execution |
| `machines` | list machines in an app | Autonomous Execution |
| `volumes` | list volumes in an app | Autonomous Execution |
| `machine-create` | create a machine (confirm first) | Supervised Execution |
| `machine-stop` | stop a machine (confirm first) | Autonomous Execution |
| `machine-start` | start a machine (confirm first) | Autonomous Execution |
| `machine-restart` | restart a machine (confirm first) | Autonomous Execution |
| `exec` | run a command in a machine (confirm first) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
