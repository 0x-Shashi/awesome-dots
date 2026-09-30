# Netlify MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Netlify via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-netlify`
* Runtime: Model Context Protocol (MCP) Server
* Category: Cloud Infrastructure
* Target Host: `api.netlify.com`
* Authentication: personal access token (per-user, app.netlify.com \u2192 User settings \u2192 Applications)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `sites` | sites (name, url, deploy state) | Autonomous Execution |
| `deploys` | recent deploys (state, created) | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
