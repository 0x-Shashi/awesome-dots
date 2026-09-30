# OpenAI Dots Execution Architecture and Compatibility Guide

This technical guide details the execution lifecycle, runtime architecture, security governance, and extension mechanisms for OpenAI Dots.

## Runtime Architecture

OpenAI Dots operate as autonomous, persistent cloud agents powered by GPT-6 Astra. Unlike stateless conversational language models, each Dot runs inside an isolated cloud execution sandbox equipped with its own virtual browser, filesystem, tool orchestration engine, and persistent memory.

### Core Architectural Layers

1. Foundation Model Engine: Powered by GPT-6 Astra and GPT-6.1 Sol, optimized for long-horizon planning, multi-step error correction, and structured tool invocation.
2. Sandboxed Cloud Environment: An isolated Linux container with a virtual browser, Python script execution runtime, and local working directory storage.
3. Persistent State Engine: Retains context, user preferences, past execution logs, and standing responsibilities across conversation sessions.
4. Governance and Permission Filter: An enforcement layer that checks all proposed external actions against user-configured permission profiles before dispatching API calls.

## How OpenAI Dots Executes Workflows

An OpenAI Dot processes workflows through four distinct operational interfaces:

### 1. Standing Responsibilities (Continuous Tasks)
Users assign long-term responsibilities through conversational prompts (for example: "Every weekday at 8 AM, scan unresolved error traces in our Sentry logs and summarize open issues").
* The Dot parses the schedule and operational boundaries.
* The instruction is registered in the persistent state engine.
* The cloud container executes the recurring task autonomously during the designated intervals, publishing summary reports directly to the user activity view.

### 2. Custom Governance Rules
Custom rules establish strict operational boundaries. Every external action falls into one of four execution tiers:
* Autonomous Execution: Read-only data retrieval and local computation that proceed without user interruption.
* Prompt-Initiated Execution: Pre-approved actions explicitly commanded in the immediate conversation context.
* Supervised Execution: Consequential state changes (such as creating issues, posting messages, or modifying records) that pause and require interactive user confirmation.
* User Handoff: Actions strictly prohibited from automation (such as changing passwords, signing agreements, processing refunds, or transferring funds), requiring manual human completion.

### 3. Model Context Protocol (MCP) Tool Discovery
OpenAI Dots integrates with external web services and enterprise tools through the Model Context Protocol (MCP).
* The Dot dynamically queries connected MCP servers for available tools.
* Tool definitions expose standardized JSON-RPC schemas describing input parameters, return values, and required scopes.
* When a task requires external data, the Dot forms structured tool calls and dispatches them through the MCP client.

### 4. Local Machine Bridges via Secure Tunnels
When granted explicit access, a Dot can interact with a user local workstation using encrypted client tunnels (such as the official OpenAI tunnel client or community bridge tools).
* The tunnel creates an encrypted WebSocket connection between the cloud container and the local machine.
* The Dot can execute designated terminal commands, inspect repository files, and trigger local builds within authorized workspace paths.
* Local filesystem access remains strictly restricted to designated project directories.

## Universal Skill Specification Standard

To ensure that any operational skill can be executed reliably by an OpenAI Dot, every skill in this repository adheres to the following specification:

```yaml
---
name: service-workflow-identifier
category: engineering | research | operations | sales | content | productivity
description: Concise single-sentence summary of the workflow.
trigger_phrases:
  - keyword or phrase that activates the skill
dependencies:
  mcp_connector: dots-mcp-target-service
  permissions:
    - action: tool_name
      mode: Autonomous Execution | Prompt-Initiated Execution | Supervised Execution | User Handoff
---

### Standing Responsibility Prompt
The exact instruction string to assign this responsibility to an OpenAI Dot for recurring background execution.

### Step-by-Step Execution Protocol
1. Discovery and ingestion of target records.
2. Local processing, filtering, and transformation.
3. Drafting outputs in the sandboxed filesystem.
4. Requesting confirmation if mutation is required.

### Safety and Security Boundaries
* Specific data boundaries and operational restrictions to prevent unintended state changes.
```

## Security Best Practices

1. Never Pass Secrets in Prompts: API keys and credentials must be stored in environment variables or managed through OAuth 2.0 flows.
2. Default to Read-Only Ingestion: When configuring new integrations, grant read permissions first to verify the Dot behavior before adding write scopes.
3. Review Activity Feeds: Inspect periodic execution reports in the desktop activity panel to verify that scheduled responsibilities follow intended boundaries.
