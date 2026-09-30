# Letta MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Letta via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-letta`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.letta.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `agents` | list agents | Autonomous Execution |
| `core-memory` | read core-memory blocks | Autonomous Execution |
| `archival-memory` | list archival passages | Autonomous Execution |
| `archival-memory` | add a passage | Autonomous Execution |
| `block-create` | create a standalone block | Supervised Execution |
| `message` | let the agent record it | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
