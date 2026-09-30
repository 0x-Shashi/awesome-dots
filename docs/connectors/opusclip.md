# Opusclip MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Opusclip via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-opusclip`
* Runtime: Model Context Protocol (MCP) Server
* Category: Content and Media
* Target Host: `api.opus.pro`
* Authentication: API key via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | check connection (verifies against a project if given) | Autonomous Execution |
| `project-create` | Execute project-create command. | Supervised Execution |
| `project-get` | project status (stage: QUEUED -> rendering -> done) | Autonomous Execution |
| `clips` | list exportable clips with scores | Autonomous Execution |
| `upload-link` | generate a resumable upload link for a local file | Supervised Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
