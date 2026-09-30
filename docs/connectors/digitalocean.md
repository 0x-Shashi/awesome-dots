# Digitalocean MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Digitalocean via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-digitalocean`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.digitalocean.com`
* Authentication: personal access token (per-user, cloud.digitalocean.com \u2192 API)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `droplets` | droplets (name, status, region) | Autonomous Execution |
| `domains` | domains (name) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
