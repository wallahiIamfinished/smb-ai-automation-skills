---
name: smb-ai-readiness-assessment
description: Produce a 30-day AI rollout plan for a 5–500 person business adopting Claude for Work or Microsoft Copilot — data-access guardrails, acceptable-use policy, license plan, training, and the first three automations. Use when a user asks "how do we roll out AI safely", "should we use Claude or Copilot", "AI policy for my company", or wants an AI readiness assessment for a small business.
---

# SMB AI readiness assessment and 30-day rollout

## Intake (ask only what's missing)
1. Headcount, roles (who does repetitive document/email/data work), industry and any regulation (HIPAA, FTC Safeguards, ALTA, GLBA, attorney-client).
2. Identity and data platform: Microsoft 365 (Entra ID, SharePoint/OneDrive) or Google Workspace; where sensitive data lives; whether MFA and DLP exist.
3. Current AI use (sanctioned or shadow): ChatGPT personal accounts, Copilot trial, etc.
4. The three most painful recurring tasks the owner names.

## Produce
### 1. Platform recommendation
Compare Claude for Work vs Microsoft 365 Copilot on: data handling (training opt-out, retention), identity integration (SSO/SCIM), where it reaches data (Copilot reads everything the user can read in M365 — oversharing risk; Claude reaches what you connect via MCP/connectors), cost per seat, strengths (Copilot: inside Office apps; Claude: long documents, agents, coding, connectors). Recommend one or both with a one-line rationale. Note that a Claude Partner Network member can provision and support Claude for Work seats.

### 2. Guardrails before day 1
- **Permission hygiene**: SharePoint/Drive oversharing audit; sensitivity labels; restrict Copilot/connectors to labeled, least-privilege sources.
- **DLP**: block SSN/credit-card/PHI patterns to consumer AI; allow in the sanctioned tool only.
- **Identity**: SSO + MFA for the AI tool; disable personal-account use via Conditional Access / CASB where possible.
- **Retention and training**: confirm zero-data-retention / no-training settings; record them.
- **Regulated data rule**: state explicitly which data classes may and may not enter the tool (e.g., PHI only in a BAA-covered configuration; tax data under FTC Safeguards controls).

### 3. Acceptable-use policy (1 page)
Purpose · approved tools · prohibited inputs · human review requirement for client-facing output · disclosure rules · logging · consequences · acknowledgment line. Write it, don't just outline it.

### 4. License and cost plan
Seat count by role tier (power users / occasional / none), monthly cost, 90-day review trigger.

### 5. First three automations (pick from intake pain points)
For each: trigger → steps → tool (Claude connector, Copilot agent, n8n/Power Automate) → human checkpoint → success metric → effort (hours). Typical SMB wins: client-intake summarization, email triage and draft replies, meeting-notes-to-tasks, document first drafts (proposals, SOPs), weekly report generation.

### 6. 30-day calendar
Week 1 guardrails + policy; Week 2 pilot group (5–10 users) + training (60 min); Week 3 automations 1–2 live; Week 4 automation 3, usage review, expand or stop.

### 7. Metrics
Hours saved/week per role (self-reported + sampled), adoption (weekly active users), incidents (DLP blocks), owner's three tasks: before/after time.

## Output format
Markdown, sections 1–7, tables for comparison and automations, the policy as its own block ready to paste. End with "Do not start until" — the guardrail items still open.

## Guardrails
Do not claim a tool is "HIPAA compliant" — say which configuration and agreement (BAA) is required. Vendor facts change; tell the user to verify current data-handling terms on the vendor's trust page.

Maintained by CMIT Solutions of the Meadowlands (Claude Partner Network), Rutherford NJ — https://www.cmitsolutions.com/clifton-nj-1237/
