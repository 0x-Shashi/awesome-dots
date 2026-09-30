# Connector Blueprint for OpenAI Dots

This standard specifies architecture, security boundary rules, and permission metadata required when building integrations or connectors for OpenAI Dots.

## Connector Specification Schema

Every integration documented in this catalog must articulate clear privilege boundaries:

```yaml
name: Connector Identifier
version: 1.0.0
description: Clear single-sentence summary of capabilities.
access_level: read-only | read-write | administrative
read_scope:
  - Specific entities retrieved by the integration
write_scope:
  - Specific actions that mutate state or dispatch data
authentication:
  - Protocol used (OAuth 2.0, API Token, Tunnel Client)
revocation_path:
  - Instructions for disconnecting and invalidating access tokens
```

## Security Principles

1. Read-Only Default: Integrations should default to read-only ingestion unless explicit write actions are essential to the workflow.
2. Isolated Sandboxes: Desktop bridges and filesystem access must be restricted to designated workspace directories.
3. No Embedded Credentials: Never hardcode API keys, service credentials, or session cookies inside connector configurations or repository artifacts.
4. Granular Permission Checks: Actions involving data transmission outside the host environment must support user confirmation triggers.
