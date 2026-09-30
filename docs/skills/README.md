# OpenAI Dots Skills Library

A curated repository of 160 production-ready, standardized agent skills structured specifically for OpenAI Dots.

## Overview

Each skill defines:
1. Standard Frontmatter & Trigger Keywords: Activates the skill when referenced.
2. Standing Responsibility Prompt: Copy-paste prompt to register persistent background tasks in your Dot.
3. 4-Tier Permission Mapping: Declares exact governance boundaries (Autonomous, Prompt-Initiated, Supervised, User Handoff).
4. MCP Dependency: Declares connected Model Context Protocol servers required for execution.

## Category Index

| Category | Skill Count | Description | Directory |
| :--- | :--- | :--- | :--- |
| **Engineering** | 45 | PR reviews, testing, CI/CD, debugging, infrastructure | [engineering/](engineering/) |
| **Research** | 25 | Competitor tracking, literature search, data analysis | [research/](research/) |
| **Operations** | 25 | Incident response, cloud spend audits, runbooks, compliance | [operations/](operations/) |
| **Sales** | 20 | Inbound lead qualification, CRM sync, deal tracking | [sales/](sales/) |
| **Content** | 20 | Release changelogs, newsletter drafting, transcript repurposing | [content/](content/) |
| **Productivity** | 25 | Morning briefings, inbox triage, calendar defense, travel | [productivity/](productivity/) |

## Complete Skills Catalog (160 Skills)

| Skill | Category | Primary MCP | Documentation |
| :--- | :--- | :--- | :--- |
| **Brand Guidelines** | Content | `dots-mcp-custom` | [brand-guidelines.md](content/brand-guidelines.md) |
| **Brand Identity** | Content | `dots-mcp-custom` | [brand-identity.md](content/brand-identity.md) |
| **Case Study Builder** | Content | `dots-mcp-custom` | [case-study-builder.md](content/case-study-builder.md) |
| **Changelog Comms** | Content | `dots-mcp-slack` | [changelog-comms.md](content/changelog-comms.md) |
| **Changelog Pro** | Content | `dots-mcp-github` | [changelog-pro.md](content/changelog-pro.md) |
| **Content Strategist** | Content | `dots-mcp-custom` | [content-strategist.md](content/content-strategist.md) |
| **Copywriter** | Content | `dots-mcp-custom` | [copywriter.md](content/copywriter.md) |
| **Documentation Pro** | Content | `dots-mcp-github` | [documentation-pro.md](content/documentation-pro.md) |
| **Email Marketer** | Content | `dots-mcp-custom` | [email-marketer.md](content/email-marketer.md) |
| **Newsletter Pro** | Content | `dots-mcp-github` | [newsletter-pro.md](content/newsletter-pro.md) |
| **Podcast Marketer** | Content | `dots-mcp-custom` | [podcast-marketer.md](content/podcast-marketer.md) |
| **Pr Specialist** | Content | `dots-mcp-github` | [pr-specialist.md](content/pr-specialist.md) |
| **Press Release Drafter** | Content | `dots-mcp-github` | [press-release-drafter.md](content/press-release-drafter.md) |
| **Seo Content Writer** | Content | `dots-mcp-custom` | [seo-content-writer.md](content/seo-content-writer.md) |
| **Seo Specialist** | Content | `dots-mcp-custom` | [seo-specialist.md](content/seo-specialist.md) |
| **Social Media Manager** | Content | `dots-mcp-custom` | [social-media-manager.md](content/social-media-manager.md) |
| **Speech Writer** | Content | `dots-mcp-custom` | [speech-writer.md](content/speech-writer.md) |
| **Technical Writer** | Content | `dots-mcp-custom` | [technical-writer.md](content/technical-writer.md) |
| **Ui Copywriter** | Content | `dots-mcp-custom` | [ui-copywriter.md](content/ui-copywriter.md) |
| **Video Editor** | Content | `dots-mcp-custom` | [video-editor.md](content/video-editor.md) |
| **Api Integration Specialist** | Engineering | `dots-mcp-custom` | [api-integration-specialist.md](engineering/api-integration-specialist.md) |
| **Argo Cd Pro** | Engineering | `dots-mcp-github` | [argo-cd-pro.md](engineering/argo-cd-pro.md) |
| **Bash Pro** | Engineering | `dots-mcp-github` | [bash-pro.md](engineering/bash-pro.md) |
| **Ci Cd Specialist** | Engineering | `dots-mcp-custom` | [ci-cd-specialist.md](engineering/ci-cd-specialist.md) |
| **Clean Architecture** | Engineering | `dots-mcp-custom` | [clean-architecture.md](engineering/clean-architecture.md) |
| **Clean Code** | Engineering | `dots-mcp-github` | [clean-code.md](engineering/clean-code.md) |
| **Cloud Security** | Engineering | `dots-mcp-custom` | [cloud-security.md](engineering/cloud-security.md) |
| **Code Review Pro** | Engineering | `dots-mcp-github` | [code-review-pro.md](engineering/code-review-pro.md) |
| **Container Security** | Engineering | `dots-mcp-custom` | [container-security.md](engineering/container-security.md) |
| **Database Designer** | Engineering | `dots-mcp-custom` | [database-designer.md](engineering/database-designer.md) |
| **Debugging Pro** | Engineering | `dots-mcp-github` | [debugging-pro.md](engineering/debugging-pro.md) |
| **Dependabot Review** | Engineering | `dots-mcp-custom` | [dependabot-review.md](engineering/dependabot-review.md) |
| **Dependency Scanner** | Engineering | `dots-mcp-custom` | [dependency-scanner.md](engineering/dependency-scanner.md) |
| **Devops Pro** | Engineering | `dots-mcp-github` | [devops-pro.md](engineering/devops-pro.md) |
| **Django Pro** | Engineering | `dots-mcp-github` | [django-pro.md](engineering/django-pro.md) |
| **Docker Pro** | Engineering | `dots-mcp-github` | [docker-pro.md](engineering/docker-pro.md) |
| **E2E Testing Pro** | Engineering | `dots-mcp-github` | [e2e-testing-pro.md](engineering/e2e-testing-pro.md) |
| **Fastapi Pro** | Engineering | `dots-mcp-github` | [fastapi-pro.md](engineering/fastapi-pro.md) |
| **Git Pro** | Engineering | `dots-mcp-github` | [git-pro.md](engineering/git-pro.md) |
| **Github Actions Pro** | Engineering | `dots-mcp-github` | [github-actions-pro.md](engineering/github-actions-pro.md) |
| **Graphql Pro** | Engineering | `dots-mcp-github` | [graphql-pro.md](engineering/graphql-pro.md) |
| **Helm Pro** | Engineering | `dots-mcp-github` | [helm-pro.md](engineering/helm-pro.md) |
| **Incident Commander** | Engineering | `dots-mcp-slack` | [incident-commander.md](engineering/incident-commander.md) |
| **Incident Comms** | Engineering | `dots-mcp-slack` | [incident-comms.md](engineering/incident-comms.md) |
| **Incident Responder** | Engineering | `dots-mcp-slack` | [incident-responder.md](engineering/incident-responder.md) |
| **Kubernetes Pro** | Engineering | `dots-mcp-github` | [kubernetes-pro.md](engineering/kubernetes-pro.md) |
| **Linux Pro** | Engineering | `dots-mcp-github` | [linux-pro.md](engineering/linux-pro.md) |
| **Microservices Pro** | Engineering | `dots-mcp-github` | [microservices-pro.md](engineering/microservices-pro.md) |
| **Monorepo Pro** | Engineering | `dots-mcp-github` | [monorepo-pro.md](engineering/monorepo-pro.md) |
| **Nextjs Pro** | Engineering | `dots-mcp-github` | [nextjs-pro.md](engineering/nextjs-pro.md) |
| **Performance Pro** | Engineering | `dots-mcp-github` | [performance-pro.md](engineering/performance-pro.md) |
| **Postgres Pro** | Engineering | `dots-mcp-github` | [postgres-pro.md](engineering/postgres-pro.md) |
| **Python Pro** | Engineering | `dots-mcp-github` | [python-pro.md](engineering/python-pro.md) |
| **React Pro** | Engineering | `dots-mcp-github` | [react-pro.md](engineering/react-pro.md) |
| **Redis Pro** | Engineering | `dots-mcp-github` | [redis-pro.md](engineering/redis-pro.md) |
| **Refactoring Pro** | Engineering | `dots-mcp-github` | [refactoring-pro.md](engineering/refactoring-pro.md) |
| **Rest Api Pro** | Engineering | `dots-mcp-github` | [rest-api-pro.md](engineering/rest-api-pro.md) |
| **Security Auditor** | Engineering | `dots-mcp-custom` | [security-auditor.md](engineering/security-auditor.md) |
| **Sentry Pro Dev** | Engineering | `dots-mcp-github` | [sentry-pro-dev.md](engineering/sentry-pro-dev.md) |
| **Sre Pro** | Engineering | `dots-mcp-github` | [sre-pro.md](engineering/sre-pro.md) |
| **Tdd Pro** | Engineering | `dots-mcp-github` | [tdd-pro.md](engineering/tdd-pro.md) |
| **Terraform Pro** | Engineering | `dots-mcp-github` | [terraform-pro.md](engineering/terraform-pro.md) |
| **Testing Pro** | Engineering | `dots-mcp-github` | [testing-pro.md](engineering/testing-pro.md) |
| **Typescript Pro** | Engineering | `dots-mcp-github` | [typescript-pro.md](engineering/typescript-pro.md) |
| **Vulnerability Management** | Engineering | `dots-mcp-custom` | [vulnerability-management.md](engineering/vulnerability-management.md) |
| **Alert Rules** | Operations | `dots-mcp-sentry` | [alert-rules.md](operations/alert-rules.md) |
| **Audit Logger** | Operations | `dots-mcp-custom` | [audit-logger.md](operations/audit-logger.md) |
| **Backup Strategist** | Operations | `dots-mcp-custom` | [backup-strategist.md](operations/backup-strategist.md) |
| **Backup Strategy** | Operations | `dots-mcp-custom` | [backup-strategy.md](operations/backup-strategy.md) |
| **Budget Checkin** | Operations | `dots-mcp-stripe` | [budget-checkin.md](operations/budget-checkin.md) |
| **Capacity Planner** | Operations | `dots-mcp-custom` | [capacity-planner.md](operations/capacity-planner.md) |
| **Cloud Pricing** | Operations | `dots-mcp-github` | [cloud-pricing.md](operations/cloud-pricing.md) |
| **Compliance Mapper** | Operations | `dots-mcp-custom` | [compliance-mapper.md](operations/compliance-mapper.md) |
| **Cron Monitoring** | Operations | `dots-mcp-custom` | [cron-monitoring.md](operations/cron-monitoring.md) |
| **Escalation Policies** | Operations | `dots-mcp-custom` | [escalation-policies.md](operations/escalation-policies.md) |
| **Financial Modeler** | Operations | `dots-mcp-custom` | [financial-modeler.md](operations/financial-modeler.md) |
| **Iam Pro** | Operations | `dots-mcp-github` | [iam-pro.md](operations/iam-pro.md) |
| **Invoice Reconciler** | Operations | `dots-mcp-stripe` | [invoice-reconciler.md](operations/invoice-reconciler.md) |
| **License Auditor** | Operations | `dots-mcp-custom` | [license-auditor.md](operations/license-auditor.md) |
| **Mfa Rollout** | Operations | `dots-mcp-custom` | [mfa-rollout.md](operations/mfa-rollout.md) |
| **On Call Guide** | Operations | `dots-mcp-custom` | [on-call-guide.md](operations/on-call-guide.md) |
| **On Call Handoff** | Operations | `dots-mcp-custom` | [on-call-handoff.md](operations/on-call-handoff.md) |
| **Procurement Gatekeeper** | Operations | `dots-mcp-github` | [procurement-gatekeeper.md](operations/procurement-gatekeeper.md) |
| **Rbac Designer** | Operations | `dots-mcp-custom` | [rbac-designer.md](operations/rbac-designer.md) |
| **Runbook Writer** | Operations | `dots-mcp-custom` | [runbook-writer.md](operations/runbook-writer.md) |
| **Saas Security Essentials** | Operations | `dots-mcp-custom` | [saas-security-essentials.md](operations/saas-security-essentials.md) |
| **Secrets Manager** | Operations | `dots-mcp-custom` | [secrets-manager.md](operations/secrets-manager.md) |
| **Soc Analyst** | Operations | `dots-mcp-custom` | [soc-analyst.md](operations/soc-analyst.md) |
| **Status Page** | Operations | `dots-mcp-custom` | [status-page.md](operations/status-page.md) |
| **Zero Trust Architect** | Operations | `dots-mcp-custom` | [zero-trust-architect.md](operations/zero-trust-architect.md) |
| **Calendar Guardian** | Productivity | `dots-mcp-google-workspace` | [calendar-guardian.md](productivity/calendar-guardian.md) |
| **Calendar Pro** | Productivity | `dots-mcp-github` | [calendar-pro.md](productivity/calendar-pro.md) |
| **Daily Briefing** | Productivity | `dots-mcp-custom` | [daily-briefing.md](productivity/daily-briefing.md) |
| **Deep Work Planner** | Productivity | `dots-mcp-custom` | [deep-work-planner.md](productivity/deep-work-planner.md) |
| **Email Triage** | Productivity | `dots-mcp-custom` | [email-triage.md](productivity/email-triage.md) |
| **Executive Coach** | Productivity | `dots-mcp-custom` | [executive-coach.md](productivity/executive-coach.md) |
| **Focus Modes** | Productivity | `dots-mcp-custom` | [focus-modes.md](productivity/focus-modes.md) |
| **Goal Setter** | Productivity | `dots-mcp-custom` | [goal-setter.md](productivity/goal-setter.md) |
| **Habit Tracker** | Productivity | `dots-mcp-custom` | [habit-tracker.md](productivity/habit-tracker.md) |
| **Habit Tracker Coach** | Productivity | `dots-mcp-custom` | [habit-tracker-coach.md](productivity/habit-tracker-coach.md) |
| **Home Task Manager** | Productivity | `dots-mcp-custom` | [home-task-manager.md](productivity/home-task-manager.md) |
| **Inbox Zero Coach** | Productivity | `dots-mcp-custom` | [inbox-zero-coach.md](productivity/inbox-zero-coach.md) |
| **Meeting Notes Ai** | Productivity | `dots-mcp-google-workspace` | [meeting-notes-ai.md](productivity/meeting-notes-ai.md) |
| **Meeting Optimizer** | Productivity | `dots-mcp-google-workspace` | [meeting-optimizer.md](productivity/meeting-optimizer.md) |
| **Meeting Prep Brief** | Productivity | `dots-mcp-github` | [meeting-prep-brief.md](productivity/meeting-prep-brief.md) |
| **Note Taker** | Productivity | `dots-mcp-custom` | [note-taker.md](productivity/note-taker.md) |
| **Pomodoro Coach** | Productivity | `dots-mcp-custom` | [pomodoro-coach.md](productivity/pomodoro-coach.md) |
| **Reminder System** | Productivity | `dots-mcp-custom` | [reminder-system.md](productivity/reminder-system.md) |
| **Second Brain** | Productivity | `dots-mcp-custom` | [second-brain.md](productivity/second-brain.md) |
| **Task Manager** | Productivity | `dots-mcp-custom` | [task-manager.md](productivity/task-manager.md) |
| **Time Tracker** | Productivity | `dots-mcp-custom` | [time-tracker.md](productivity/time-tracker.md) |
| **Travel Day Planner** | Productivity | `dots-mcp-custom` | [travel-day-planner.md](productivity/travel-day-planner.md) |
| **Weekly Review** | Productivity | `dots-mcp-custom` | [weekly-review.md](productivity/weekly-review.md) |
| **Weekly Review Ritual** | Productivity | `dots-mcp-custom` | [weekly-review-ritual.md](productivity/weekly-review-ritual.md) |
| **Zettelkasten** | Productivity | `dots-mcp-custom` | [zettelkasten.md](productivity/zettelkasten.md) |
| **Academic Writing** | Research | `dots-mcp-custom` | [academic-writing.md](research/academic-writing.md) |
| **Ai Research** | Research | `dots-mcp-custom` | [ai-research.md](research/ai-research.md) |
| **Bayesian Statistics** | Research | `dots-mcp-custom` | [bayesian-statistics.md](research/bayesian-statistics.md) |
| **Causal Inference** | Research | `dots-mcp-custom` | [causal-inference.md](research/causal-inference.md) |
| **Citation Manager** | Research | `dots-mcp-custom` | [citation-manager.md](research/citation-manager.md) |
| **Competitive Intelligence** | Research | `dots-mcp-custom` | [competitive-intelligence.md](research/competitive-intelligence.md) |
| **Data Labeling** | Research | `dots-mcp-custom` | [data-labeling.md](research/data-labeling.md) |
| **Data Scientist** | Research | `dots-mcp-custom` | [data-scientist.md](research/data-scientist.md) |
| **Deep Work Planner** | Research | `dots-mcp-custom` | [deep-work-planner.md](research/deep-work-planner.md) |
| **Eval Frameworks** | Research | `dots-mcp-custom` | [eval-frameworks.md](research/eval-frameworks.md) |
| **Experiment Designer** | Research | `dots-mcp-custom` | [experiment-designer.md](research/experiment-designer.md) |
| **Grant Writing** | Research | `dots-mcp-custom` | [grant-writing.md](research/grant-writing.md) |
| **Literature Review** | Research | `dots-mcp-custom` | [literature-review.md](research/literature-review.md) |
| **Llm Benchmarks** | Research | `dots-mcp-custom` | [llm-benchmarks.md](research/llm-benchmarks.md) |
| **Market Researcher** | Research | `dots-mcp-custom` | [market-researcher.md](research/market-researcher.md) |
| **Methods Writing** | Research | `dots-mcp-custom` | [methods-writing.md](research/methods-writing.md) |
| **Patent Search** | Research | `dots-mcp-custom` | [patent-search.md](research/patent-search.md) |
| **Peer Review Checklist** | Research | `dots-mcp-custom` | [peer-review-checklist.md](research/peer-review-checklist.md) |
| **Qualitative Analysis** | Research | `dots-mcp-custom` | [qualitative-analysis.md](research/qualitative-analysis.md) |
| **Rag Engineer** | Research | `dots-mcp-custom` | [rag-engineer.md](research/rag-engineer.md) |
| **Research Paper Assistant** | Research | `dots-mcp-custom` | [research-paper-assistant.md](research/research-paper-assistant.md) |
| **Statistical Modeling** | Research | `dots-mcp-custom` | [statistical-modeling.md](research/statistical-modeling.md) |
| **Survey Designer** | Research | `dots-mcp-custom` | [survey-designer.md](research/survey-designer.md) |
| **Time Series Analysis** | Research | `dots-mcp-custom` | [time-series-analysis.md](research/time-series-analysis.md) |
| **Trend Analyzer** | Research | `dots-mcp-custom` | [trend-analyzer.md](research/trend-analyzer.md) |
| **Account Based Marketing** | Sales | `dots-mcp-custom` | [account-based-marketing.md](sales/account-based-marketing.md) |
| **B2B Demand Gen** | Sales | `dots-mcp-custom` | [b2b-demand-gen.md](sales/b2b-demand-gen.md) |
| **Channel Sales** | Sales | `dots-mcp-custom` | [channel-sales.md](sales/channel-sales.md) |
| **Client Onboarding** | Sales | `dots-mcp-custom` | [client-onboarding.md](sales/client-onboarding.md) |
| **Contract Reviewer** | Sales | `dots-mcp-custom` | [contract-reviewer.md](sales/contract-reviewer.md) |
| **Conversion Optimizer** | Sales | `dots-mcp-custom` | [conversion-optimizer.md](sales/conversion-optimizer.md) |
| **Crm Specialist** | Sales | `dots-mcp-custom` | [crm-specialist.md](sales/crm-specialist.md) |
| **Customer Success** | Sales | `dots-mcp-custom` | [customer-success.md](sales/customer-success.md) |
| **Customer Support Playbook** | Sales | `dots-mcp-custom` | [customer-support-playbook.md](sales/customer-support-playbook.md) |
| **Deal Desk** | Sales | `dots-mcp-custom` | [deal-desk.md](sales/deal-desk.md) |
| **Influencer Outreach** | Sales | `dots-mcp-custom` | [influencer-outreach.md](sales/influencer-outreach.md) |
| **Lead Scoring** | Sales | `dots-mcp-custom` | [lead-scoring.md](sales/lead-scoring.md) |
| **Outbound Prospecting** | Sales | `dots-mcp-github` | [outbound-prospecting.md](sales/outbound-prospecting.md) |
| **Partnership Manager** | Sales | `dots-mcp-custom` | [partnership-manager.md](sales/partnership-manager.md) |
| **Pitch Deck Creator** | Sales | `dots-mcp-custom` | [pitch-deck-creator.md](sales/pitch-deck-creator.md) |
| **Pricing Strategist** | Sales | `dots-mcp-github` | [pricing-strategist.md](sales/pricing-strategist.md) |
| **Proposal Figures** | Sales | `dots-mcp-github` | [proposal-figures.md](sales/proposal-figures.md) |
| **Retention Specialist** | Sales | `dots-mcp-custom` | [retention-specialist.md](sales/retention-specialist.md) |
| **Rfp Response Builder** | Sales | `dots-mcp-custom` | [rfp-response-builder.md](sales/rfp-response-builder.md) |
| **Sales Coach** | Sales | `dots-mcp-custom` | [sales-coach.md](sales/sales-coach.md) |

## How to Use Any Skill with Your OpenAI Dot

1. Open your ChatGPT Desktop or Web client.
2. In your Dot conversation, paste the **Standing Responsibility Prompt** from the skill document.
3. Configure your permissions according to the **Governance and Permission Mapping** table.
4. Your Dot will maintain this responsibility in its persistent memory and run it on schedule.
