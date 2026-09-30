# Mem0 MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Mem0 via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-mem0`
* Runtime: Model Context Protocol (MCP) Server
* Category: Productivity
* Target Host: `api.mem0.ai`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `add` | store a memory (async) | Autonomous Execution |
| `status` | poll an add/search event | Autonomous Execution |
| `search` | semantic search (async) | Autonomous Execution |
| `list` | list memories for a user | Autonomous Execution |
| `get` | get one memory | Autonomous Execution |
| `history` | change log of one memory | Autonomous Execution |
| `delete` | delete one memory (confirm first) | User Handoff |
| `wipe` | delete ALL memories in scope (confirm first) | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
