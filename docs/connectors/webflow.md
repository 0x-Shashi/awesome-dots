# Webflow MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Webflow via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-webflow`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.webflow.com`
* Authentication: per-site token via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the connection (lists accessible sites) | Autonomous Execution |
| `sites` | list sites | Autonomous Execution |
| `site` | site details (domains, publish status) | Autonomous Execution |
| `collections` | list CMS collections on a site | Autonomous Execution |
| `items` | list CMS items in a collection | Autonomous Execution |
| `create-item` | Execute create-item command. | Supervised Execution |
| `update-item` | Execute update-item command. | Supervised Execution |
| `delete-item` | delete a CMS item | User Handoff |
| `publish` | publish the site | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
