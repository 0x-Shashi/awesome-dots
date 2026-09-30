# Descript MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Descript via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-descript`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.descript.com`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the API key | Autonomous Execution |
| `projects` | list projects | Autonomous Execution |
| `project` | get one project | Autonomous Execution |
| `jobs` | list Underlord/agent jobs | Autonomous Execution |
| `job-status` | get job status once | Autonomous Execution |
| `job-status` | poll until job_state is "stopped" | Autonomous Execution |
| `publish` | submit a publish job (confirm first) | Supervised Execution |
| `job-delete` | delete a job (confirm first) | User Handoff |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
