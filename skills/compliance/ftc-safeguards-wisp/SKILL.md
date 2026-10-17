---
name: ftc-safeguards-wisp
description: Draft a Written Information Security Program (WISP) for a CPA, tax preparer, bookkeeper, mortgage broker or other non-bank financial institution covered by the FTC Safeguards Rule (16 CFR Part 314). Use when a user asks for a WISP, a Safeguards Rule plan, an IRS Publication 4557 / Form W-12 data security plan, or "what do I need to be compliant with the FTC Safeguards Rule".
---

# FTC Safeguards WISP drafter

## When to use
The user runs or advises a firm that handles customer financial information and is subject to the Safeguards Rule: CPA and tax firms, bookkeepers, payroll providers, mortgage brokers, auto dealers that finance, collection agencies, financial advisors not covered by the SEC. PTIN holders must attest to having a data security plan on Form W-12.

## Intake (ask only what is missing)
1. Firm name, state, number of employees, number of client records held.
2. Where customer data lives: tax software (name), cloud drive, email, paper, local server, portal.
3. Whether the firm has fewer than 5,000 consumers' records (triggers the small-firm exemptions in 314.6).
4. Who will be the Qualified Individual (314.4(a)) — an employee or an outside provider.
5. Current controls: MFA, encryption at rest/in transit, EDR, backups, vendor list, training, incident response plan.

## Produce
A WISP in this order, each section mapped to the rule citation. Write in plain language, present tense, firm name filled in.

1. **Purpose and scope** — 314.3; define "customer information" and systems in scope.
2. **Qualified Individual** — 314.4(a); name, authority, reporting line, use of a service provider if applicable.
3. **Risk assessment** — 314.4(b); written, criteria for evaluating risk, how it is reviewed (at least annually). Include a starter risk table with 8–12 rows: lost laptop, phishing, ransomware, insider misuse, vendor breach, improper disposal, unpatched software, weak passwords, unencrypted email, physical theft.
4. **Safeguards** — 314.4(c)(1)–(8), one subsection each:
   - access controls and least privilege
   - data and system inventory
   - encryption in transit and at rest (or compensating controls approved by the QI)
   - secure development / application assessment (usually "not applicable; we use vendor software; vendor review below")
   - multi-factor authentication for anyone accessing customer information
   - secure disposal within two years of last use unless retention required
   - change management
   - monitoring and logging of authorized-user activity
5. **Testing and monitoring** — 314.4(d); continuous monitoring OR annual penetration test + vulnerability assessment every six months.
6. **Training** — 314.4(e); annual security awareness, QI training.
7. **Service providers** — 314.4(f); selection, contract clauses, periodic assessment. Include a vendor register template (name, data accessed, contract clause y/n, last review).
8. **Program evaluation and adjustment** — 314.4(g).
9. **Incident response plan** — 314.4(h); goals, roles, communications, remediation, documentation, post-incident review. Include the FTC notification requirement: notify the FTC within 30 days of discovering a "notification event" affecting 500+ consumers (314.4(j), effective May 2024). Include state breach-notification reference for the firm's state.
10. **Board / owner reporting** — 314.4(i); annual written report.
11. **Appendices** — asset inventory table, vendor register, training log, annual review log, acknowledgment page.

## Small-firm exemptions (314.6)
If the firm maintains information on fewer than 5,000 consumers, sections 3 (written risk assessment), 5 (continuous monitoring/pen test), 9 (written incident response plan) and 10 (annual report) are not required by rule. Still recommend them; mark them "recommended, not required for firms under 5,000 consumers".

## Output format
Markdown with H2 per section, citations in parentheses, tables for registers. End with a "Next 30 days" action list of the controls the intake showed as missing, ordered by risk.

## Guardrails
State clearly that this is a draft for review, not legal advice. Do not invent facts about the firm; leave placeholders in brackets. If the user is in New Jersey, mention the NJ Identity Theft Prevention Act breach-notification duty (N.J.S.A. 56:8-163).

Maintained by CMIT Solutions of the Meadowlands, Rutherford NJ — https://www.cmitsolutions.com/clifton-nj-1237/
