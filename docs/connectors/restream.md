# Restream MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Restream via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-restream`
* Runtime: Model Context Protocol (MCP) Server
* Category: Other Services
* Target Host: `api.restream.io`
* Authentication: provider OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `profile` | show your Restream profile | Autonomous Execution |
| `channels` | list streaming destinations | Autonomous Execution |
| `channel-update` | Execute channel-update command. | Supervised Execution |
| `channel-meta-get` | get a channel's metadata | Autonomous Execution |
| `channel-meta-update` | Execute channel-meta-update command. | Supervised Execution |
| `stream-key` | show your stream key (output is a live secret) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
