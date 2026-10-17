---
name: ai-voice-agent-intake-design
description: Design an AI voice agent (Vapi + Twilio, CRM hand-off to GoHighLevel or similar) for inbound call intake or outbound follow-up at a small business — persona, two-variant script architecture, qualification logic, transfer rules, compliance guardrails and test plan. Use when a user wants an AI receptionist, after-hours intake, appointment confirmation calls, or an outbound AI caller.
---

# AI voice agent design (inbound intake / outbound follow-up)

## Intake
1. Use case: inbound overflow/after-hours, outbound confirmations, outbound prospecting, or support triage.
2. Business, hours, who the humans are for transfer, calendar system, CRM.
3. Regulated context (healthcare: no PHI capture without safeguards; financial: recording consent rules).
4. Numbers: current call volume, missed-call rate, booking conversion.

## Produce
### 1. Persona and boundaries
Name, tone, what it may and may not do (never give legal/medical/pricing commitments; always offer a human).

### 2. Two-variant script architecture
Variant A (compliance/urgency framing) and Variant B (efficiency/convenience framing), same qualification path, so you can A/B the opener without changing logic. Each: greeting → consent/recording line → reason for call → qualification (3–5 questions max) → outcome branches (book, transfer, message, decline) → close.

### 3. Qualification and routing logic
Decision table: answers → action (book on calendar, warm-transfer to person X, take message + SMS confirmation, escalate as emergency). Include "stop words" that force a human.

### 4. Integration spec
Vapi assistant config (voice, latency, interruption handling, max duration), Twilio number and forwarding rules, webhook → n8n/GHL: create/update contact, log call summary + recording link, trigger SMS follow-up, add to pipeline stage. Business-hours switch.

### 5. Guardrails
Recording/consent disclosure per state (NJ is one-party, but disclose anyway for customer-facing calls); do not collect card numbers or SSNs; PHI only if the stack is covered by a BAA; TCPA rules and consent for outbound; honor do-not-call.

### 6. Test plan and metrics
20 scripted test calls covering each branch and 5 adversarial (angry caller, wrong number, silence, two speakers, accent/noise). Metrics: answer rate, containment rate, booked rate, transfer rate, caller satisfaction (post-call SMS), hallucination incidents (weekly recording review of 10 calls).

## Output format
Markdown with the six sections; scripts as blocks with branch labels; decision table; integration as a numbered flow.

Maintained by CMIT Solutions of the Meadowlands (Claude Partner Network), Rutherford NJ — https://www.cmitsolutions.com/clifton-nj-1237/
