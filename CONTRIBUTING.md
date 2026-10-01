# Contributing to Awesome OpenAI Dots

Thank you for your interest in contributing to Awesome OpenAI Dots. This repository aims to be the most comprehensive, structured, and production-tested resource collection for the OpenAI Dots ecosystem.

By contributing, you help developers, researchers, and operators discover, build, and deploy safe agentic workflows.

---

## Table of Contents

- [Ways to Contribute](#ways-to-contribute)
- [Submission Guidelines](#submission-guidelines)
  - [1. Adding a New Dot Skill](#1-adding-a-new-dot-skill)
  - [2. Adding a New MCP Connector](#2-adding-a-new-mcp-connector)
  - [3. Adding Curated Resources or Tools](#3-adding-curated-resources-or-tools)
  - [4. Improving Safety Policies or Documentation](#4-improving-safety-policies-or-documentation)
- [Quality and Formatting Standards](#quality-and-formatting-standards)
- [Pull Request Process](#pull-request-process)
- [License and Attribution](#license-and-attribution)

---

## Ways to Contribute

You can contribute in several ways:
- Submit new, tested Dot Skills to the skills library.
- Author standardized MCP connector blueprints.
- Add verified developer tools, SDKs, or field cases to the catalog.
- Refine existing technical documentation, architecture guides, and safety profiles.
- Report issues, outdated links, or schema inconsistencies.

---

## Submission Guidelines

### 1. Adding a New Dot Skill

Dot Skills live in `docs/skills/<category>/<skill-slug>.md` and are indexed in `data/skills.json`.

When contributing a new skill, ensure your submission includes:
- **Title and Slug**: Clear, descriptive name matching the filename.
- **Category**: One of `engineering`, `research`, `operations`, `sales`, `content`, or `productivity`.
- **Target Persona**: Who uses or delegates this responsibility.
- **Execution Mode**: Explicit permission tier:
  - Autonomous Execution
  - Prompt-Initiated Execution
  - Supervised Execution
  - User Handoff
- **Standing Instruction**: Copy-pasteable system prompt written in clear English.
- **Input Parameters & Output Format**: Structured specification of arguments and expected deliverables.
- **Tool Dependencies**: List of required MCP connectors or ChatGPT plugins.
- **Safety Boundary**: Explicit prohibited actions or escalation triggers.

### 2. Adding a New MCP Connector

Connectors live in `docs/connectors/<category>/<connector-slug>.md` and are indexed in `data/connectors.json`.

Every connector submission must include:
- Connector name, vendor, and protocol (e.g. MCP over stdio or SSE).
- Read-only versus write-action permission classifications.
- Authentication method (OAuth 2.0, API token, environment variable).
- Available tool endpoints, argument schemas, and return formats.
- Safe rollback or rate limit considerations.

### 3. Adding Curated Resources or Tools

When suggesting new tools, repositories, or articles:
- Verify that the resource is directly relevant to OpenAI Dots, persistent agent execution, or MCP tool calling.
- Add the entry to both the appropriate section in `README.md` and the corresponding category in `data/catalog.json`.
- Keep descriptions concise, factual, and neutral. Avoid promotional or marketing language.
- Ensure all hyperlinks are active and point to canonical sources.

### 4. Improving Safety Policies or Documentation

Safety is a core priority of this repository. When proposing adjustments to safety rules or governance profiles:
- Specify the threat model or failure mode being addressed (e.g. prompt injection, privilege escalation, credential exfiltration).
- Provide practical verification steps or test cases.

---

## Quality and Formatting Standards

To ensure consistency across the entire repository, please adhere to these rules:

1. **Language**: All documentation, comments, schemas, and prompts must be in English.
2. **Typography**: Do not use unicode em dashes or double dashes in documentation. Use standard hyphens with spaces (` - `).
3. **Clean Visuals**: Avoid decorative emojis or icons in headings, bullet points, and tables. Keep the design clean and developer-focused.
4. **Markdown Formatting**: Use standard GitHub Flavored Markdown with clean tables, code blocks, and valid internal file links.
5. **No Broken Links**: Verify all relative file paths and external URLs before submitting.

---

## Pull Request Process

1. **Fork the Repository**: Create your own fork of `0x-Shashi/awesome-dots`.
2. **Create a Feature Branch**:
   ```bash
   git checkout -b feature/add-skill-my-new-skill
   ```
3. **Make Your Changes**: Adhere to the formatting standards described above.
4. **Validate Your Files**:
   - Verify that JSON files in `data/` are valid JSON.
   - Ensure new markdown files link correctly from their respective indexes.
5. **Commit with Clear Messages**:
   ```bash
   git commit -m "Add Linear bug triager skill to engineering library"
   ```
6. **Push and Open a Pull Request**: Submit your pull request against the `main` branch with a concise summary of what was added or improved.

---

## License and Attribution

By submitting a contribution to this repository, you agree that your contribution will be licensed under the MIT License as described in [LICENSE](LICENSE). All contributions remain open source and freely accessible to the community.
