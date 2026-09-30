# Tesla Powerwall MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Tesla Powerwall via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-tesla-powerwall`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `fleet-api.prd.na.vn.cloud.tesla.com`
* Authentication: provider OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `sites` | list energy sites | Autonomous Execution |
| `status` | live power: solar, battery, grid, load | Autonomous Execution |
| `site-info` | site info and settings | Autonomous Execution |
| `history` | Execute history command. | Autonomous Execution |
| `set-reserve` | Execute set-reserve command. | Autonomous Execution |
| `set-mode` | Execute set-mode command. | Autonomous Execution |
| `storm-mode` | Execute storm-mode command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
