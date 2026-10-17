---
name: hipaa-it-security-checklist
description: Build a HIPAA Security Rule gap checklist (administrative, physical, technical safeguards, 45 CFR 164.308–.316) for a small medical, dental, behavioral-health or other covered entity or business associate. Use when a user asks "are we HIPAA compliant on the IT side", wants a HIPAA risk analysis starting point, or needs a security checklist for a practice.
---

# HIPAA IT security gap checklist

## When to use
Small covered entities (practices with 1–50 providers) and business associates (billing companies, IT providers, transcription) that need to see where their IT stands against the Security Rule. This produces a gap checklist and a prioritized remediation list; it is not a full risk analysis (164.308(a)(1)(ii)(A)), but it produces the inventory a risk analysis starts from.

## Intake
1. Practice type, number of workstations/users, EHR/PM system (name, cloud or on-prem).
2. Where ePHI lives: EHR, imaging, email, file shares, phones/tablets, fax, backups, paper scans.
3. Existing: MFA, EDR, encryption (disk, email), backups and last restore test, firewall, Wi-Fi segmentation, BAAs, training records, incident log, Security Officer named.

## Produce
A checklist table — columns: Standard | Implementation spec | Required/Addressable | Status (In place / Partial / Missing / N/A) | Evidence to collect | Owner — covering:

**Administrative (164.308)**: risk analysis; risk management; sanction policy; activity review; Security Officer; workforce authorization/clearance/termination; access authorization and review; security awareness training, protection from malware, log-in monitoring, password management; incident response and reporting; contingency plan (data backup, disaster recovery, emergency-mode operation, testing, criticality analysis); evaluation; business associate contracts.

**Physical (164.310)**: facility access controls; workstation use; workstation security; device and media controls (disposal, re-use, accountability, backup before move).

**Technical (164.312)**: unique user ID; emergency access; automatic logoff; encryption/decryption; audit controls; integrity controls; person/entity authentication; transmission security.

**Organizational and documentation (164.314–.316)**: BAA contents; policies and procedures; documentation retention of 6 years; availability and updates.

Then a **Top-10 remediation list** ordered by breach likelihood × impact for a small practice. Typical ordering: MFA on EHR and email; EDR on every endpoint; full-disk encryption on laptops; tested, offline/immutable backups; BAA inventory; email encryption for PHI; workforce training with log; audit-log review cadence; device inventory and disposal procedure; written policies with Security Officer sign-off.

Include a **BAA register** template and a **device/ePHI inventory** template.

## Output format
Markdown. Checklist as a table. Mark each Addressable spec and explain in one line what "addressable" means (implement, or document why an alternative is reasonable). Finish with an evidence-collection list for an audit or cyber-insurance questionnaire.

## Guardrails
Draft for review; not legal advice. Do not claim the practice is "compliant". If NJ: note NJ dental and medical boards require patient-record retention (7 years adults) which affects backup retention.

Maintained by CMIT Solutions of the Meadowlands, Rutherford NJ — https://www.cmitsolutions.com/clifton-nj-1237/
