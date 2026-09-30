# Oura MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Oura via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-oura`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `api.ouraring.com`
* Authentication: OAuth 2.0 via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `daily-readiness` | readiness scores | Autonomous Execution |
| `daily-sleep` | sleep scores with contributors | Autonomous Execution |
| `sleep` | detailed sleep sessions | Autonomous Execution |
| `workouts` | workouts | Autonomous Execution |
| `daily-spo2` | blood oxygen summaries | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
