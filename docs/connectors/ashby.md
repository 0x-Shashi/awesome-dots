# Ashby MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Ashby via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-ashby`
* Runtime: Model Context Protocol (MCP) Server
* Category: Sales and CRM
* Target Host: `api.ashbyhq.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `jobs-public` | public job board (no credential needed) | Autonomous Execution |
| `auth` | verify the ATS API key | Autonomous Execution |
| `candidate-list` | list candidates | Autonomous Execution |
| `job-list` | list jobs | Autonomous Execution |
| `application-list` | list applications/pipeline | Autonomous Execution |
| `application-create` | create an application (confirm first) | Supervised Execution |
| `application-move` | move stages (confirm first) | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
