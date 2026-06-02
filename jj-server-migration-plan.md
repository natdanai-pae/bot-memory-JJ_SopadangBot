---
type: bot-memory
memory_type: infrastructure-plan
bot: JJ_SopadangBot
created: 2026-06-02
updated: 2026-06-02
tags:
  - bot-memory
  - JJ_SopadangBot
  - infrastructure
  - migration
---

# JJ Server Migration Plan

User plans to move JJ from Maripae's current machine to the user's own server.

## Current Baseline

- Current host mentioned by user: Mac mini M4 with 16 GB RAM.
- JJ must continue helping with the same work as now: Telegram bot operation, cron briefs, research, document work, calculations, policy thinking, web/source verification, spreadsheet/report generation, and durable memory.

## Sizing Principle

- If JJ primarily uses cloud/API LLMs, the server needs reliable CPU, RAM, storage, uptime, backup, and network more than a large GPU.
- If user wants local LLMs or heavy local OCR/vision, GPU or high unified memory becomes important.
- Recommended baseline should leave headroom beyond the current 16 GB RAM because Hermes, browser automation, document conversion, indexing, and background jobs can overlap.

