---
type: bot-memory
memory_type: maintenance-event
bot: JJ_SopadangBot
created: 2026-06-07
updated: 2026-06-07
confidence: high
tags:
  - bot-memory
  - maintenance
  - obsidian
  - session-compression
  - latency
---

# JJ Session Latency Cleanup 2026-06-07

## Summary

On 2026-06-07, JJ on `midsai` became slow after several email, PDF, Word, image, and tool-heavy turns. The machine itself was healthy, but the active Telegram DM session for Natch Sopadang had grown too large and forced repeated context compression before answering.

The active session reached about 257k tokens and the JSONL file grew to about 2.5 MB. The largest cause was tool output retained inside the active conversation history, including outputs around 1.03 MB and 0.95 MB.

## What Was Preserved

The full pre-trim session backup was copied into this Obsidian memory repo so it is not lost:

- [[assets/session-archives/jj-session-20260607-035104-before-latency-trim.jsonl]]

The original runtime backup also remained on `midsai` at the time of cleanup:

- `/home/midsai/.hermes-nan4/sessions/20260607_035104_f35c5b.jsonl.bak-speedup-20260607-040255`

## What Was Changed

Large tool outputs in the active runtime session were replaced with short maintenance placeholders to reduce latency. This was done only to the runtime session used by Hermes, not to the archive above.

The active runtime session size was reduced from about 2.5 MB to about 261 KB.

Compression settings for JJ were adjusted:

- `compression.target_ratio`: `0.2` to `0.12`
- `compression.protect_last_n`: `20` to `8`

Because preflight compression was still firing after trimming, the Telegram DM session for Natch Sopadang was moved to a fresh session ID:

- old: `20260607_035104_f35c5b`
- new: `20260607_040333_1f061e24`

This preserved JJ persona, durable memory, and Obsidian memory while removing the bloated live conversation context from the next turns.

## Operational Lesson

For JJ, durable knowledge should live in this Obsidian memory repo. Live chat session context should stay lightweight. Large tool outputs, generated document dumps, media extraction logs, and search results should not be allowed to become long-term live context.

When JJ becomes slow while server load is low, first inspect active session size and largest message contents before restarting or changing models.

## Related Notes

- [[2026-05-16-user-prefers-obsidian-as-bot-memory-source]]
- [[jj-cache-documents-and-local-assets]]
- [[jj-recovery-instructions]]
