# Docusign MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Docusign via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-docusign`
* Runtime: Model Context Protocol (MCP) Server
* Category: Business Services
* Target Host: `demo.docusign.net`
* Authentication: OAuth 2.0 Authorization Code Grant (per-user)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify OAuth; list accounts | Autonomous Execution |
| `envelopes` | list envelopes | Autonomous Execution |
| `envelope-get` | envelope details | Autonomous Execution |
| `envelope-status` | status + recipient state | Autonomous Execution |
| `envelope-create` | Execute envelope-create command. | Supervised Execution |
| `envelope-send` | Execute envelope-send command. | Supervised Execution |
| `document-download` | Execute document-download command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
