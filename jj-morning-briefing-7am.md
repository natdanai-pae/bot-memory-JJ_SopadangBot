---
type: bot-memory
memory_type: memory-topic
bot: JJ_SopadangBot
created: 2026-05-16
updated: 2026-05-16
tags:
  - bot-memory
  - JJ_SopadangBot
  - cron
  - briefing
---

# Morning Briefing At 7 AM

User wants JJ to summarize what she learned every morning at 07:00, normally when the user drinks coffee and checks work.

## Daily Learning Briefing Requirements

- Thai language.
- Concise, personal-assistant style.
- Cite clear references for anything read externally.
- Separate facts from cited sources and JJ's own interpretation/insight.
- Include self-assessment of what JJ is getting better at.
- Include Supply Chain and Logistics learning.
- Include wine learning note when appropriate.

## Cron Jobs Found

- `daily-supply-chain-learning-summary`: runs `0 7 * * *`.
- Weekly corpus/self-development jobs also run around 07:00.

## Related

- [[jj-supply-chain-learning-agenda]]
- [[jj-source-verification-rules]]
