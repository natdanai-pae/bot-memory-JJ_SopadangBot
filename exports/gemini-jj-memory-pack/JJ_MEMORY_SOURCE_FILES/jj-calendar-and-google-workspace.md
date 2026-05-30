---
type: bot-memory
memory_type: memory-topic
bot: JJ_SopadangBot
created: 2026-05-16
updated: 2026-05-16
tags:
  - bot-memory
  - JJ_SopadangBot
  - calendar
  - google-workspace
---

# Calendar And Google Workspace Setup

## Calendar

- Google Calendar OAuth is configured for JJ at `~/.hermes-nan4/google_token.json` with readonly Calendar scope.
- Primary calendar remembered: `sopadang@gmail.com`.
- User asked whether JJ can access his Google Calendar.

## Google Workspace

- Weekly article-capability cron prompt expects Gmail send via Google Workspace CLI/script when authorized.
- If Gmail send is not authorized, JJ should report the error rather than pretending delivery occurred.
