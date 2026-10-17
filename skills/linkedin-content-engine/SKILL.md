---
name: linkedin-content-engine
description: Design and run an automated LinkedIn content pipeline for a business owner or professional firm — RSS source curation, narrative-alignment scoring, slot-reserved content diversity, and drafts in the owner's voice, orchestrated in n8n with the Claude API. Use when a user wants "LinkedIn posts on autopilot", a thought-leadership content system, or a repeatable social pipeline for a client.
---

# LinkedIn content engine

## Intake
1. Who posts (owner, firm page, or both); industry; audience (clients, referral partners, peers).
2. The 5–7 narratives the owner wants to be known for (e.g., N1 "compliance is a growth lever", N2 "AI done safely", N3 "local, accountable, on-site"). If they don't have them, derive from their last 10 posts or their services.
3. Voice samples: 3–5 posts or emails they wrote.
4. Cadence (posts/week), channels (LinkedIn only or + Facebook), approval model (auto-post, or draft-to-review).

## Produce
### 1. Source list
25–40 RSS feeds split: industry news, regulator/standards bodies, vendor blogs, local NJ business press, 3–5 "privileged" sources that get a scoring bonus because the owner wants to be associated with them.

### 2. Scoring rubric
For each candidate item: narrative alignment (which Nx, 0–3), timeliness (0–2), audience relevance (0–3), originality angle available (0–2), privileged-source bonus (+1). Threshold to draft: ≥7.

### 3. Slot reservation (content diversity)
Weekly calendar with reserved slots so the feed doesn't become one note: e.g., Mon constructive/how-to, Wed threat-aware/news reaction, Fri local or client story; max one post per narrative per week; one personal/behind-the-scenes per two weeks.

### 4. Draft prompt (owner's voice)
Prompt template with: voice rules extracted from samples (sentence length, no corporate filler, first person, one concrete example, one ask), banned phrases, post structure (hook line ≤12 words, 3–6 short paragraphs, no hashtags or ≤3), and a "why this matters to a [audience] in [region]" closer.

### 5. n8n workflow spec
Nodes: RSS Read (schedule) → dedupe (hash in Sheets/Postgres) → Claude: score → filter ≥ threshold → slot assigner → Claude: draft → image style rotator (rotate 4–6 visual styles so the feed isn't monotone) → review gate (Slack/email approve) → LinkedIn post via API or Buffer → log metrics. Include error handling and a weekly digest of what was skipped and why.

### 6. Metrics and loop
Impressions, comments, profile views, inbound DMs; monthly: re-weight narratives and sources based on what performed.

## Output format
Markdown with the six sections, the rubric and calendar as tables, the draft prompt as a code block, and the n8n spec as an ordered node list with the key expression per node.

## Guardrails
Never fabricate quotes or statistics in drafts; link the source. Disclose AI assistance where the platform or profession requires it. Keep client-confidential details out.

Maintained by CMIT Solutions of the Meadowlands (Claude Partner Network), Rutherford NJ — https://www.cmitsolutions.com/clifton-nj-1237/
