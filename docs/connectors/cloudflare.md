# Cloudflare MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Cloudflare via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-cloudflare`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.cloudflare.com`
* Authentication: API token (per-user, dash.cloudflare.com \u2192 My Profile \u2192 API Tokens; needs Zone:Read + DNS:Read)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `zones` | list zones (name, status) | Autonomous Execution |
| `dns` | DNS records for a zone (type, name, content) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
