# Openweathermap MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Openweathermap via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-openweathermap`
* Runtime: Model Context Protocol (MCP) Server
* Category: Data Services
* Target Host: `api.openweathermap.org`
* Authentication: OpenWeatherMap API key (per-user, openweathermap.org \u2192 API keys; free tier fine)

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `weather` | current conditions | Autonomous Execution |
| `forecast` | 5-day forecast, first 8 slots | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
