# Dub MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Dub via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-dub`
* Runtime: Model Context Protocol (MCP) Server
* Category: Email and Marketing
* Target Host: `api.dub.co`
* Authentication: API key (per-workspace)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `links` | list links | Autonomous Execution |
| `create` | new short link | Supervised Execution |
| `update` | edit a link | Supervised Execution |
| `delete` | delete a link | User Handoff |
| `analytics` | click analytics | Autonomous Execution |
| `track-lead` | record a lead | Autonomous Execution |
| `track-sale` | record a sale | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
