# Research and Knowledge Production Use Cases

End-to-end research workflows automating continuous beat tracking, academic literature synthesis, and data intelligence via OpenAI Dots.

## 1. Continuous Industry Beat and Competitor Watch

* Connected Apps: Exa, Consensus, Google Drive, and Notion.
* Trigger: Scheduled daily or weekly morning interval.
* Execution Protocol:
  1. Discovery (Autonomous): Dot monitors a curated list of competitor websites, changelogs, patent filings, and engineering publications via neural web search.
  2. Fact Verification (Autonomous): Dot cross-references claims across primary sources, clearly separating verified product releases from speculative rumors.
  3. Brief Compilation (Prompt-Initiated): Dot produces a dated executive digest highlighting key technological moves, architectural changes, and strategic implications.
* Governance Boundary: Operating purely in read-only retrieval mode without authenticating behind third-party paywalls.

## 2. Citation-Backed Literature Brief

* Connected Apps: Consensus, SciSpace, and Zotero.
* Trigger: Research question prompt or scheduled literature scan.
* Execution Protocol:
  1. Ingestion (Autonomous): Dot identifies relevant peer-reviewed studies across designated scientific journals.
  2. Synthesis (Autonomous): Dot compares experimental methodologies, sample sizes, and empirical findings.
  3. Citation Formatting (Prompt-Initiated): Dot formats references into Zotero and writes a concise literature brief with linked paper identifiers and methodology caveats.
* Governance Boundary: The Dot flags conflicting evidence and marks speculative claims for human researcher review.

## 3. Spreadsheet Data Analysis and Findings Brief

* Connected Apps: Data, Google Drive, and Airtable.
* Trigger: Upload of a new performance dataset or recurring month-end review.
* Execution Protocol:
  1. Data Parsing (Autonomous): Dot reads tabular data and executes statistical Python analysis inside the cloud sandbox.
  2. Trend Detection (Autonomous): Dot calculates month-over-month variances, cohort retention metrics, and outlier data points.
  3. Executive Summary (Prompt-Initiated): Dot produces an executive briefing containing summary tables, chart exports, and highlighted anomalies.
* Governance Boundary: Read-only data processing; any proposed changes to database records require explicit user confirmation.
