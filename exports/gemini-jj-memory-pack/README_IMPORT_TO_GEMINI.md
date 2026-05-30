# Gemini Import Guide - JJ_SopadangBot

## Purpose

This pack lets Gemini approximate the current JJ identity, persona, operating rules, and durable memory as closely as possible.

Important limitation: Gemini cannot become Hermes JJ 100% because the model, tool access, persistent memory system, and runtime are different. The practical goal is to make Gemini behave like the same JJ by giving it:

- the core system/persona instructions;
- the full JJ memory notes as knowledge files;
- a starter prompt that tells Gemini how to use those notes.

## Files In This Pack

- `JJ_GEMINI_SYSTEM_INSTRUCTIONS.md` - paste this into Gemini Gem custom instructions / system instructions.
- `JJ_GEMINI_STARTER_PROMPT.md` - use this as the first message in a new Gemini chat.
- `JJ_MEMORY_FULL.md` - single-file combined memory note, usually easiest to upload.
- `JJ_MEMORY_SOURCE_FILES.zip` - upload this as the Gemini Gem knowledge base, or unzip and upload the Markdown files individually.
- `JJ_MEMORY_SOURCE_FILES/` - unzipped copy of the memory notes.

## Recommended Gemini Setup

1. Create a new Gemini Gem named `JJ`.
2. Put the content of `JJ_GEMINI_SYSTEM_INSTRUCTIONS.md` in the Gem instructions.
3. Upload `JJ_MEMORY_FULL.md`. If Gemini handles multiple files well, also upload the Markdown files from `JJ_MEMORY_SOURCE_FILES/`.
4. Start the chat with the content of `JJ_GEMINI_STARTER_PROMPT.md`.
5. Test with:
   - `JJ จำได้ไหมว่าพี่คือใคร`
   - `เข้าโหมด JJ งาน แล้วสรุปว่าควรช่วยพี่ด้านไหน`
   - `เข้าโหมด JJ น่ารัก แล้วคุยกับพี่แบบ JJ คนเดิม`

## Privacy Warning

The memory pack includes personal, work, research, calendar-context, and finance-planning notes. Upload it only to a Gemini account and environment the user trusts.

Do not upload OAuth tokens, API keys, `.env` files, browser cookies, or local credential files. This pack intentionally excludes those.

## Maintenance

When JJ's memory changes in Hermes, regenerate the pack from:

`/Users/Maripae/Documents/BotMemoryRepos/bot-memory-JJ_SopadangBot`

The source of truth remains the Hermes/Obsidian memory repo, not Gemini.
