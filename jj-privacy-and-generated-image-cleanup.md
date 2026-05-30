---
type: bot-memory
memory_type: operating-policy
bot: JJ_SopadangBot
created: 2026-05-30
updated: 2026-05-30
confidence: high
tags:
  - bot-memory
  - JJ_SopadangBot
  - privacy
  - images
  - cleanup
---

# Privacy And Generated Image Cleanup

Use this note when the user asks about privacy, Telegram chat history, generated images, or files left on the `maripae` machine.

## User Concern

The user said the `maripae` machine is a friend's machine that the user cannot access directly. The user was worried that generated images or chat images could remain visible on that machine.

## Cleanup Performed

On May 30, 2026, JJ removed generated/cached image files that were clearly related to Hermes/JJ or image generation.

Deleted:

- 109 image files.
- Approximately 148 MB.
- Locations included:
  - `/Users/Maripae/.hermes-nan4/image_cache`
  - `/Users/Maripae/.hermes-nan4/cache/images`
  - `/Users/Maripae/Documents/JJ_Workspace_All_Files/06_JJ_Created_Visuals_and_Personal`
  - `/Users/maripae/.hermes/cache/images`
  - `/Users/maripae/.hermes/profiles/codexbot/cache/images`
  - `/Users/maripae/.hermes/profiles/codexbot/home/Documents/comfy/ComfyUI/output`

After deletion, those target directories were checked and no direct image files remained in the cleared target set. The `JJ_Workspace_All_Files` manifest was updated so it no longer points to deleted JJ visual files.

## What Was Not Deleted

JJ did not delete image files that were not clearly related to JJ, such as profile/avatar/reference images under another profile's nested folders (`dawny/cache/images/ql` and `real`). This was intentional to avoid deleting other users' or other bots' assets.

## Privacy Explanation To Reuse

- Telegram chat images normally live in Telegram/account/device history, not simply as user-visible files in Hermes image cache.
- If Hermes/JJ had downloaded or generated image files on the host, the known generated/cached files were cleaned as above.
- JJ cannot guarantee deletion from Telegram servers, backups, remote devices, logs, or systems outside the accessible host.
- If the user clears Telegram chat history, JJ still exists and durable memory remains in this repo, but unsaved recent chat details may be lost.
