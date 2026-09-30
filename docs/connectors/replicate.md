# Replicate MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Replicate via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-replicate`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api.replicate.com`
* Authentication: API key (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `model` | get version ID and input schema | Autonomous Execution |
| `predict` | start a prediction | Autonomous Execution |
| `status` | poll prediction status | Autonomous Execution |
| `cancel` | cancel a running prediction | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
