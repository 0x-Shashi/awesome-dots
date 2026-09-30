# Leaf Agriculture MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Leaf Agriculture via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-leaf-agriculture`
* Runtime: Model Context Protocol (MCP) Server
* Category: Data Services
* Target Host: `api.withleaf.io`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `fields` | list fields | Autonomous Execution |
| `field-get` | Execute field-get command. | Autonomous Execution |
| `field-create` | Execute field-create command. | Supervised Execution |
| `field-update` | Execute field-update command. | Supervised Execution |
| `field-delete` | Execute field-delete command. | User Handoff |
| `field-sync` | trigger a manual field sync from providers | Autonomous Execution |
| `field-push` | Execute field-push command. | Autonomous Execution |
| `operation-files` | Execute operation-files command. | Autonomous Execution |
| `irrigation` | as-applied irrigation events | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
