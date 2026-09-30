# Starter Policy for OpenAI Dots

This document outlines baseline permission configurations and governance rules to apply to an always-on OpenAI Dot before connecting personal or workplace services.

## Overview of Governance Modes

OpenAI Dots operate with four distinct action execution modes:

1. Autonomous Execution: The agent performs the specified action automatically without pausing for user intervention.
2. Prompt-Initiated Execution: The agent executes the action only if the user explicitly commanded it in a previous prompt; otherwise, it requests approval.
3. Supervised Execution: The agent stops and requires interactive user confirmation prior to executing the action.
4. User Handoff: The agent stops entirely and directs the user to complete the action directly.

## Baseline Five-Rule Safety Set

Before enabling active tools, configure the following five baseline safeguards:

| Target Action | Configured Mode | Purpose |
| :--- | :--- | :--- |
| Outbound communication (email, Slack, Teams) | Supervised Execution | Prevents unexpected external messages from being sent without explicit sign-off. |
| Financial transactions and subscriptions | User Handoff | Protects payment credentials and prevents unintended spending. |
| Record deletion and file removal | Supervised Execution | Protects against unrecoverable data loss in local and cloud stores. |
| External file and document sharing | Supervised Execution | Ensures proprietary assets are not shared across organization boundaries. |
| Granting third-party app permissions | User Handoff | Prevents security privilege escalation without explicit review. |

## Mandatory Non-Overridable Limits

Certain actions are strictly protected by platform security policies and cannot be bypassed via custom rules:

* Credential alterations and monetary transfers always trigger a mandatory user handoff.
* Permanent file purge operations require explicit manual authorization.
* Automated safety checks cannot be disabled or relaxed.
* Background background tasks cannot autonomously dispatch external messages, update plugins, or control local desktop interfaces without supervision.
* In enterprise workspaces, administrator-level controls override individual user configurations.
