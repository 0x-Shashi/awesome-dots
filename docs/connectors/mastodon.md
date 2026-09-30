# Mastodon MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Mastodon via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-mastodon`
* Runtime: Model Context Protocol (MCP) Server
* Category: Communication
* Target Host: `your Mastodon instance host`
* Authentication: provider OAuth via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `verify` | verify the token (own profile) | Autonomous Execution |
| `my-posts` | recent toots | Supervised Execution |
| `followers` | own followers | Autonomous Execution |
| `post` | confirm first | Supervised Execution |
| `post` | Execute post command. | Supervised Execution |
| `media-upload` | returns a media id for post --media-ids | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
