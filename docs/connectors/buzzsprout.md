# Buzzsprout MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Buzzsprout via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-buzzsprout`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `www.buzzsprout.com`
* Authentication: API token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API token | Autonomous Execution |
| `episodes` | list episodes | Autonomous Execution |
| `episode-get` | get one episode | Autonomous Execution |
| `episode-create` | Execute episode-create command. | Supervised Execution |
| `episode-update` | Execute episode-update command. | Supervised Execution |
| `episode-delete` | delete (confirm first) | User Handoff |
| `players` | list embed players | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
