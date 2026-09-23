---
name: Create and track a ClickUp task
description: Create a task in a List, set its Custom Fields, comment on it, and track time against it using the ClickUp public API v2.
api: openapi/clickup-api-v2-reference-openapi.json
operations: [GetAuthorizedTeams, GetSpaces, GetFolders, GetLists, GetFolderlessLists, CreateTask, GetTask, GetAccessibleCustomFields, SetCustomFieldValue, CreateTaskComment, StartatimeEntry, StopatimeEntry, UpdateTask, DeleteTask]
generated: '2026-09-17'
method: generated
source: openapi/clickup-api-v2-reference-openapi.json + conventions/clickup-conventions.yml
---

# Create and track a ClickUp task

Base URL `https://api.clickup.com/api`. Send `Authorization: pk_...` for a personal token, or
`Authorization: Bearer {access_token}` for OAuth. Always send `Content-Type: application/json` —
form-encoded bodies are not fully supported.

## 1. Resolve the target List

You cannot create a task without a `list_id`, and ids are not guessable. Walk the hierarchy:

1. `GetAuthorizedTeams` — `GET /v2/team` returns the Workspaces this token can see. In v2 a "team" IS a
   Workspace; keep its `id` as `team_id`.
2. `GetSpaces` — `GET /v2/team/{team_id}/space`.
3. `GetFolders` — `GET /v2/space/{space_id}/folder`, then `GetLists` — `GET /v2/folder/{folder_id}/list`.
4. Lists can also hang directly off a Space: `GetFolderlessLists` — `GET /v2/space/{space_id}/list`.
   Check both or you will miss half the Lists.

## 2. Create the task

`CreateTask` — `POST /v2/list/{list_id}/task` with at least `name`. Optional: `description`,
`assignees` (user ids), `status` (must be a status that exists in that List), `priority`, `due_date`
(Unix ms), `tags`.

**There is no idempotency key.** A retried `CreateTask` creates a SECOND task. If a call times out,
call `GetTasks` on the List and match on name before retrying.

## 3. Set Custom Fields

Custom Fields are a separate write. `GetAccessibleCustomFields` — `GET /v2/list/{list_id}/field` — to
resolve a field name to its `field_id` and type, then `SetCustomFieldValue` —
`POST /v2/task/{task_id}/field/{field_id}` with `{"value": ...}` shaped for that field's type.

A 400 here usually means the field is not applicable to the task's custom task type. Fields scoped to a
task type carry an `applied_objects` array whose `object_id` must match the task's `custom_item_id`.
Undo with `RemoveCustomFieldValue` (`DELETE` on the same path).

## 4. Comment

`CreateTaskComment` — `POST /v2/task/{task_id}/comment` with `comment_text`, optional `assignee` and
`notify_all`. Reading back is paginated by keyset, not page number: `GetTaskComments` returns the 25
most recent, and older pages need `start` AND `start_id` together, taken from the last comment returned.

## 5. Track time

`StartatimeEntry` — `POST /v2/team/{team_Id}/time_entries/start` with the `tid` (task id).
`Getrunningtimeentry` — `GET /v2/team/{team_id}/time_entries/current` — tells you whether a timer is
already running for this user; start a second one and the first is stopped for you.
`StopatimeEntry` — `POST /v2/team/{team_id}/time_entries/stop`.
For after-the-fact logging use `Createatimeentry` with `start` and `duration`.

## 6. Reverse what you did

`UpdateTask` edits, `DeleteTask` removes. There is NO restore operation in the API — a deleted task
goes to the Workspace Trash, which the public API does not expose. Confirm with the user before calling
`DeleteTask` or `mergeTasks`; neither has an API-side undo.

## Errors and limits

Errors come back as `{"err": "...", "ECODE": "..."}` — not RFC 9457 problem+json. Rate limits are per
token and per plan (100/min up to Business, 1,000/min Business Plus, 10,000/min Enterprise); on 429 read
`X-RateLimit-Reset` (Unix timestamp) and wait. See `errors/clickup-error-codes.yml` and
`rate-limits/clickup-rate-limits.yml`.
