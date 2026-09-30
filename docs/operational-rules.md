# Operational Rule Profiles

Domain-specific governance templates for email, calendar, financial workflows, code repositories, and privacy management.

## Electronic Mail and Direct Messaging

* Autonomous Execution: Scanning incoming email messages, generating structured morning digests, and preparing draft responses stored directly in the drafts folder.
* Prompt-Initiated Execution: Dispatching an email reply that was explicitly requested with explicit recipient confirmation in the session prompt.
* Supervised Execution: Publishing announcements or updates to shared public channels within Slack or Microsoft Teams.
* User Handoff: Any outbound correspondence addressed to a novel external contact never encountered before, or participating directly in group discussions.

## Calendar and Scheduling

* Autonomous Execution: Reading calendar feeds, surfacing conflicts, and placing private focus blocks or reminder markers.
* Prompt-Initiated Execution: Sending meeting invites to team colleagues when directed within conversation context.
* Supervised Execution: Rescheduling existing commitments or accepting incoming invitations on behalf of the owner.

## Financial and Procurement Operations

* Autonomous Execution: Monitoring vendor prices, cataloging invoices, and assembling comparative shopping sheets.
* Prompt-Initiated Execution: Finalizing an item purchase previously approved by the user up to a specified dollar limit.
* User Handoff: Creating, modifying, or cancelling recurring software-as-a-service subscriptions, or making any unprompted purchase.

## Engineering and Code Repositories

* Autonomous Execution: Initializing Codex development sessions, investigating bug reproductions, and generating isolated pull request branches.
* Supervised Execution: Leaving review remarks or triaging issues in public or open repositories.
* User Handoff: Merging code changes to main branches, tagging releases, or initiating deployment triggers.

## Personal Privacy and Credentials

* Supervised Execution: Submitting standard non-sensitive forms across web interfaces.
* User Handoff: Editing user profile records, altering credential secrets, or disclosing government identification or personal phone details.
