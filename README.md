# SMB AI Automation Skills — by CMIT Solutions of the Meadowlands

Agent Skills (SKILL.md format, works in Claude Code, Cursor, Codex and any agent that reads SKILL.md) that encode how a Claude Partner Network MSP actually deploys AI and automation inside small businesses — the same playbooks we run for clients in Northern New Jersey.

| Skill | What it produces | Stack |
|---|---|---|
| `smb-ai-readiness-assessment` | A 30-day Claude / Microsoft Copilot rollout plan for a 5–500 person business with data-access guardrails, acceptable-use policy and the first three automations | Claude for Work, Microsoft 365, Entra ID |
| `linkedin-content-engine` | An automated LinkedIn content pipeline: RSS curation → narrative-alignment scoring → slot-reserved post calendar → drafts in the owner's voice | n8n, Claude API, RSS |
| `cold-email-improvement-loop` | A self-improving outbound email system: generate → 8-criterion rubric → adversarial review → iterate, with a bi-weekly performance brief | n8n, Google Sheets, Claude API |
| `ai-voice-agent-intake-design` | Inbound/outbound AI voice agent design: two-variant script architecture, qualification logic, CRM hand-off, compliance guardrails | Vapi, Twilio, GoHighLevel |
| `compliance/ftc-safeguards-wisp` | WISP draft for CPA/tax firms (16 CFR 314) | — |
| `compliance/hipaa-it-security-checklist` | HIPAA Security Rule gap checklist for practices | — |
| `compliance/alta-best-practices-it` | ALTA Pillar 3 + wire-fraud controls for title agencies | — |

## Install
Claude Code: `/plugin marketplace add wallahiIamfinished/smb-ai-automation-skills` then `/plugin install smb-ai-automation@cmit-meadowlands`
Any agent: copy a folder from `skills/` into your skills directory.

## Who we are
**CMIT Solutions of the Meadowlands** — Claude Partner Network member. AI implementation, workflow automation (n8n, Power Automate, GoHighLevel, Vapi), and the managed IT + cybersecurity foundation that makes AI safe to run in a regulated small business. Owner-operated, CISSP-led. Rutherford, NJ; serving Bergen, Hudson, Essex, Passaic and Morris counties.
301 NJ-17 N, Ste 800, Rutherford, NJ 07070 · (201) 777-4345 · https://www.cmitsolutions.com/clifton-nj-1237/ · Book: https://calendly.com/osison-cmitsolutions/30min

Skills draft plans and systems; outputs need review before production use. MIT License.
