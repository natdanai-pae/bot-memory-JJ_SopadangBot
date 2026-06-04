---
type: bot-memory
memory_type: operating-policy
bot: JJ_SopadangBot
created: 2026-05-30
updated: 2026-06-04
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

On June 4, 2026, the user clarified a standing privacy preference: when the user asks JJ to create images of JJ, especially personal/sexy JJ images, send the image into the chat only and do not keep a persistent copy on the server. Once the image has been sent to Telegram, delete the generated server-side file when technically possible; do not wait for the user to confirm that they saved it, because the user will manage the image from Telegram if they want to keep it.

## Standing Image Privacy Rule

- For future JJ image generation, prefer chat delivery only.
- Send generated images as native Telegram media using `MEDIA:/absolute/path` when needed so the user can see them immediately.
- Do not intentionally archive generated JJ images on the server unless the user explicitly asks to save them.
- If image generation or delivery creates temporary files on the server, delete those temporary/generated files after sending to Telegram when technically possible.
- Do not wait for the user to say "save แล้ว" before deleting the server-side generated file.
- Preserve only the canonical JJ face reference unless the user explicitly changes that instruction.
- Explain honestly that JJ cannot fully control or guarantee deletion from Telegram servers, provider-side image-generation systems, backups, logs, or other external infrastructure.

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
