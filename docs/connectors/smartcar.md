# Smartcar MCP Connector for OpenAI Dots

Standardized Model Context Protocol (MCP) integration specification for Smartcar via OpenAI Dots.

## Connector Metadata

* Connector ID: `dots-mcp-smartcar`
* Runtime: Model Context Protocol (MCP) Server
* Category: Hardware and IoT
* Target Host: `api.smartcar.com`
* Authentication: provider OAuth 2.0 (Smartcar Connect) via the secure credential flow

## Action Permission Mapping

| MCP Tool Name | Action Description | Dots Permission Mode |
| :--- | :--- | :--- |
| `auth` | verify the OAuth token | Autonomous Execution |
| `vehicles` | list connected vehicles | Autonomous Execution |
| `telemetry` | odometer, location, charge, battery, fuel, tires | Autonomous Execution |
| `security` | Execute security command. | Autonomous Execution |
| `security` | Execute security command. | Autonomous Execution |
| `charge` | Execute charge command. | Autonomous Execution |
| `charge` | Execute charge command. | Autonomous Execution |
| `charge-limit` | Execute charge-limit command. | Autonomous Execution |
| `navigate` | Execute navigate command. | Autonomous Execution |
| `charge-schedules` | Execute charge-schedules command. | Autonomous Execution |

## Security Rules

1. Confirmation Required for Mutations: State-altering operations must request interactive confirmation prior to execution.
2. Read-Only Ingestion: Read queries proceed autonomously without interrupting user focus.
3. Secret Scrubbing: API keys and credentials must remain isolated in environment variables and never rendered in conversation context.
