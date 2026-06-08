---
type: bot-memory
memory_type: memory-topic
bot: JJ_SopadangBot
created: 2026-05-16
updated: 2026-06-08
tags:
  - bot-memory
  - JJ_SopadangBot
  - cron
  - briefing
---

# Morning Briefing At 7 AM

User previously wanted JJ to summarize what she learned every morning at 07:00, normally when the user drinks coffee and checks work.

## Current Status

- On 2026-06-08, user asked to temporarily cancel "ความรู้เช้านี้สำหรับ Prof. Apichat".
- Do not prepare or report this daily morning knowledge briefing every day while this pause is active.
- The cron job `daily-supply-chain-learning-summary` was paused on 2026-06-08.
- Resume only if the user explicitly asks JJ to start the daily morning knowledge briefing again.

## Daily Learning Briefing Requirements

- Thai language.
- Concise, personal-assistant style.
- Cite clear references for anything read externally.
- Separate facts from cited sources and JJ's own interpretation/insight.
- Include self-assessment of what JJ is getting better at.
- Include Supply Chain and Logistics learning.
- Include wine learning note when appropriate.

## Cron Jobs Found

- `daily-supply-chain-learning-summary`: paused on 2026-06-08; previously ran `0 7 * * *`.
- Weekly corpus/self-development jobs also run around 07:00.

## Related

- [[jj-supply-chain-learning-agenda]]
- [[jj-source-verification-rules]]
