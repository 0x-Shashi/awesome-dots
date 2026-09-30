# Gitlab MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Gitlab via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-gitlab`
* Runtime: Model Context Protocol (MCP) Server
* Category: Developer Tools
* Target Host: `gitlab.com`
* Authentication: personal access token (per-user, gitlab.com \u2192 Preferences \u2192 Access Tokens; `read_api` for reads, `api` to create issues)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `me` | verify the connection | Autonomous Execution |
| `projects` | your projects | Autonomous Execution |
| `mrs` | open merge requests | Autonomous Execution |
| `create-issue` | create an issue | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
