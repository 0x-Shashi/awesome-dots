# Launch and Operations Production Use Cases

End-to-end operational workflows coordinating marketing launches, business operations, and customer support intelligence via OpenAI Dots.

## 1. Product Launch Content Workspace

* Connected Apps: Google Drive, Notion, Canva, and Figma.
* Trigger: Upcoming product release milestone or launch owner command.
* Execution Protocol:
  1. Discovery (Autonomous): Dot extracts verified product specifications, target metrics, and release features from approved engineering docs in Notion.
  2. Asset Extraction (Autonomous): Dot reviews Figma design tokens and exports approved brand visuals.
  3. Content Generation (Prompt-Initiated): Dot drafts multi-channel announcement copy (blog post, newsletter draft, changelog summary) and populates a launch checklist in Google Drive.
* Governance Boundary: Publishing content live to social feeds or external blogs requires mandatory User Handoff.

## 2. Customer Support Trend and Documentation Gap Audit

* Connected Apps: Slack, Gmail, and Notion.
* Trigger: Scheduled weekly interval.
* Execution Protocol:
  1. Ingestion (Autonomous): Dot analyzes customer inquiry volume across permitted support channels, clustering common points of confusion.
  2. Documentation Check (Autonomous): Dot compares recurring questions against internal knowledge base pages in Notion.
  3. Gap Reporting (Prompt-Initiated): Dot generates an anonymized report identifying missing help articles, obsolete screenshots, and suggested FAQ additions.
* Governance Boundary: Outbound replies to customers remain strictly in drafts; sending requires direct human review.

## 3. Commercial Deal Account Preparation

* Connected Apps: Apollo.io, HubSpot, and Gmail.
* Trigger: Scheduled account review or newly assigned enterprise prospect.
* Execution Protocol:
  1. Enrichment (Autonomous): Dot gathers verified firmographic data, recent company funding announcements, and technology stack information from Apollo.
  2. CRM Sync (Autonomous): Dot checks past correspondence notes and deal status in HubSpot.
  3. Dossier Assembly (Prompt-Initiated): Dot produces a concise one-page account executive briefing with tailored discovery questions and draft email outreach.
* Governance Boundary: Updating CRM lifecycle stages or sending correspondence requires explicit human approval.
