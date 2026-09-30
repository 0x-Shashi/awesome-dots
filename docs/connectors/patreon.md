# Patreon MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Patreon via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-patreon`
* Runtime: Model Context Protocol (MCP) Server
* Category: Finance and Commerce
* Target Host: `www.patreon.com`
* Authentication: Creator's Access Token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the access token | Autonomous Execution |
| `identity` | show the current user | Autonomous Execution |
| `campaign` | show a campaign | Autonomous Execution |
| `members` | list campaign members | Autonomous Execution |
| `tiers` | list membership tiers | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
