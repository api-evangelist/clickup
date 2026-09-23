---
name: Subscribe to ClickUp webhooks
description: Register a ClickUp webhook against the right hierarchy level, verify the HMAC signature on delivery, and keep the subscription healthy.
api: openapi/clickup-api-v2-reference-openapi.json
operations: [GetAuthorizedTeams, CreateWebhook, GetWebhooks, UpdateWebhook, DeleteWebhook]
generated: '2026-09-17'
method: generated
source: openapi/clickup-api-v2-reference-openapi.json + https://developer.clickup.com/docs/webhooks
---

# Subscribe to ClickUp webhooks

## 1. Register

`CreateWebhook` — `POST /v2/team/{team_id}/webhook` with `endpoint` (an HTTPS URL you control) and
`events` (an array, or `"*"` for every event). Scope it by adding ONE of `space_id`, `folder_id`,
`list_id` or `task_id`: only one location per hierarchy level is allowed per webhook, and the most
specific location wins.

The response contains the webhook `id` and — once only — the shared `secret`. Store the secret; you
cannot read it back.

`OAUTH_171` on create means a webhook with this event/location combination already exists. Call
`GetWebhooks` (`GET /v2/team/{team_id}/webhook`) and reuse or `UpdateWebhook` it rather than retrying.

## 2. Verify every delivery

Each POST carries `X-Signature`: an HMAC-SHA256 of the raw request body keyed with that webhook's
secret. Compute over the RAW bytes before JSON parsing and compare in constant time. Reject mismatches —
ClickUp does not send from dedicated IP addresses, so the signature is the only proof of origin.

## 3. Handle the payload

The body carries the event name, the webhook id, and a `history_items` array describing what changed.
Payload shapes per level are documented under the Space/Folder/List/Task webhook payload pages. Respond
2xx quickly and process asynchronously.

## 4. Keep it alive

A webhook has a health status. Repeated delivery failures degrade it, and a webhook created by a user
who is later deactivated stays registered but stops firing — ClickUp re-checks that the creating user is
still in the relevant hierarchy before each trigger. Poll `GetWebhooks` to read health, `UpdateWebhook`
to change endpoint/events/status, `DeleteWebhook` to remove.

## Testing

The provider recommends https://smee.io/ for receiving events during development. There is no sandbox:
webhooks fire from the live Workspace the token belongs to.
