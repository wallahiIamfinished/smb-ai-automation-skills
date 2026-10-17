---
name: cold-email-improvement-loop
description: Build a self-improving outbound email system — generate, score against an 8-criterion rubric, adversarial review by a skeptical-buyer persona, iterate, send via a sequencer, and feed reply data back in a bi-weekly performance brief. Orchestrated in n8n with Google Sheets and the Claude API. Use when a user wants cold email that gets better on its own, a rubric for outbound copy, or an outbound system for a B2B service firm.
---

# Cold email recursive improvement loop

## Intake
1. Offer, ICP (industry, size, role), region, proof points (results, certifications, partnerships).
2. List source and size (ZoomInfo/Apollo export, scraped signals), sequencer in use (Instantly, Smartlead, GHL), sending domains and warm-up status.
3. Compliance constraints: CAN-SPAM, industry rules, do-not-contact lists.

## Produce
### 1. Rubric (8 criteria, 0–3 each, threshold 18/24)
Relevance to a named trigger · one clear problem · specific proof (number, name, or partnership) · single low-friction ask · ≤90 words · no jargon or hype words · reads like a person wrote it · subject line ≤5 words and not clickbait.

### 2. Generation prompt
Inputs: ICP row (company, role, trigger signal), offer, proof points, voice rules. Output: subject + body + one-line "why this trigger".

### 3. Adversarial review prompt
Persona: skeptical operations manager at the target company who gets 40 cold emails a day. Asks: "Why me, why now, what's the catch, what would make me reply?" Returns a verdict (delete / skim / reply) and the single change most likely to flip it.

### 4. Loop
generate → rubric score → if < threshold, revise with rubric feedback (max 3 passes) → adversarial review → if "delete", revise once more → approved copy to Sheets → sequencer sends → replies and bounces written back.

### 5. n8n spec
Trigger (new Sheet rows) → Claude generate → Claude score → IF → Claude revise → Claude adversarial → IF → append to Approved sheet → sequencer API → webhook for replies → classify reply (interested / not now / wrong person / unsubscribe) → bi-weekly cron: performance brief.

### 6. Bi-weekly performance brief
Per variant: sent, open (if tracked), reply, positive reply, meeting; top 3 triggers by positive-reply rate; rubric criteria most correlated with replies; proposed rubric weight changes; three new angles to test.

## Output format
Markdown: rubric table, both prompts as code blocks, loop as a numbered list, n8n node list, brief template.

## Guardrails
Honor unsubscribes immediately; no deceptive subject lines; never invent proof points — leave bracketed placeholders for the user to fill. Recommend ≤50 sends/day/domain and warmed domains.

Maintained by CMIT Solutions of the Meadowlands (Claude Partner Network), Rutherford NJ — https://www.cmitsolutions.com/clifton-nj-1237/
