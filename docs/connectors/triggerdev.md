# Triggerdev MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Triggerdev via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-triggerdev`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.trigger.dev`
* Authentication: API key (per-environment)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `runs` | list recent runs | Autonomous Execution |
| `run` | show one run's status and output | Autonomous Execution |
| `trigger` | trigger a task run | Autonomous Execution |
| `trigger` | with a personal access token | Autonomous Execution |
| `cancel` | cancel a run | User Handoff |
| `schedules` | list schedules | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
