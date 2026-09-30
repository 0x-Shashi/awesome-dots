# Deepl MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Deepl via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-deepl`
* Runtime: Model Context Protocol (MCP) Server
* Category: AI and Search
* Target Host: `api-free.deepl.com`
* Authentication: API key (per-user; free keys use api-free.deepl.com, paid keys use api.deepl.com)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the key and show usage | Autonomous Execution |
| `translate` | translate text | Autonomous Execution |
| `translate` | Execute translate command. | Autonomous Execution |
| `languages` | list supported target languages | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
