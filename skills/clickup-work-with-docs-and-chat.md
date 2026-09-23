---
name: Work with ClickUp Docs and Chat (API v3)
description: Search and author Docs and pages, and read or post Chat messages, on the ClickUp Public API v3.
api: openapi/clickup-public-api-v3-openapi.json
operations: [searchDocsPublic, createDocPublic, getDocPublic, getDocPageListingPublic, getDocPagesPublic, createPagePublic, getPagePublic, editPagePublic, getChatChannels, getChatMessages, createChatMessage, createReplyMessage, createChatReaction, getSubtypes]
generated: '2026-09-17'
method: generated
source: openapi/clickup-public-api-v3-openapi.json + https://developer.clickup.com/docs/chat
---

# Work with ClickUp Docs and Chat (API v3)

Docs and Chat exist ONLY on v3. Base `https://api.clickup.com/api/v3`, same `Authorization` header as
v2. In v3 the Workspace id is `workspace_id`, not `team_id`.

## Docs

- `searchDocsPublic` — `GET /workspaces/{workspace_id}/docs`. Cursor-paginated: pass `cursor` and
  `limit`, follow `next_cursor` until it is absent. This is NOT the v2 `page` idiom.
- `createDocPublic` — `POST /workspaces/{workspace_id}/docs`.
- `getDocPageListingPublic` — the Doc's table of contents (page tree) — then `getDocPagesPublic` for
  content, or `getPagePublic` for one page.
- `createPagePublic` / `editPagePublic` to author. Content is markdown; some ClickUp elements do not
  round-trip through markdown (see the Docs API limitation page), so never treat an edit as lossless —
  read the page back after writing.

## Chat

- `getChatChannels` — `GET /workspaces/{workspace_id}/chat/channels`, cursor-paginated.
- `createChatChannel`, `createLocationChatChannel` (attached to a Space/Folder/List) and
  `createDirectMessageChatChannel` create channels.
- `getChatMessages` reads a channel; `createChatMessage` posts. For a `post`-type message you must first
  call `getSubtypes` — subtype ids are per-Workspace and cannot be hard-coded.
- `createReplyMessage` threads under a message; `createChatReaction` adds an emoji reaction by lower-case
  name.

## Reversal

`deleteChatMessage`, `deleteChatChannel` and `deleteChatReaction` exist and take effect immediately;
there is no undo and no retention window published. Docs have no delete operation in the public
contract at all.

## Errors

Same `{"err","ECODE"}` envelope as v2; the same per-token rate limits apply.
