# Engineering and Product Production Use Cases

End-to-end production workflows combining official ChatGPT plugins, local client bridges, and OpenAI Dots autonomous scheduling.

## 1. Automated Error Triage to Patch Verification

* Connected Apps: Sentry, GitHub, Slack, and local client tunnel.
* Trigger: Unresolved production exception detected in error tracking with more than 10 impacted users.
* Execution Protocol:
  1. Ingestion (Autonomous): Dot reads the exception stack trace and affected release version from Sentry.
  2. Investigation (Autonomous): Dot inspects the local Git repository via secure tunnel, locating the exact file and commit where the regression was introduced.
  3. Reproduction (Autonomous): Dot synthesizes an isolated test script reproducing the failure inside the sandbox.
  4. Drafting (Prompt-Initiated): Dot generates a candidate branch and drafts a pull request containing the fix and regression test.
  5. Notification (Supervised): Dot drafts an incident brief in a dedicated Slack channel with links to the Sentry trace, test results, and PR draft.
* Governance Boundary: Branch merge and production deployment require explicit User Handoff.

## 2. Release Readiness and Verification Audit

* Connected Apps: GitHub, Vercel, and Linear.
* Trigger: New release candidate tag published or scheduled weekly pre-release audit.
* Execution Protocol:
  1. Audit (Autonomous): Dot compares open pull requests, milestone targets in Linear, and required CI check runs in GitHub.
  2. Inspection (Autonomous): Dot accesses the Vercel preview deployment via virtual cloud browser to confirm build health and asset integrity.
  3. Gap Detection (Autonomous): Dot highlights unresolved blockers, unmerged documentation changes, or failing tests.
  4. Reporting (Prompt-Initiated): Dot compiles a structured go/no-go audit sheet linking directly to unresolved items.
* Governance Boundary: Deploying to production environments or altering release tags requires mandatory User Handoff.

## 3. Customer Feedback to Prioritized Backlog

* Connected Apps: Slack, Notion, and Linear.
* Trigger: Scheduled weekly triage or user command.
* Execution Protocol:
  1. Synthesis (Autonomous): Dot parses incoming feedback threads across support channels and community spaces, grouping requests into thematic clusters.
  2. Deduplication (Autonomous): Dot cross-references existing product roadmap notes in Notion to prevent duplicate tickets.
  3. Drafting (Prompt-Initiated): Dot drafts structured issue cards with user stories, acceptance criteria, and source citations.
* Governance Boundary: Creating live tickets in the production Linear backlog pauses for interactive human approval.
