# ClickUp GraphQL

## Overview

ClickUp does not offer a native public GraphQL API. The platform exposes its functionality exclusively through a REST API (v2) available at `https://api.clickup.com/api/v2`. There is no publicly documented GraphQL endpoint.

## Schema Type

**Conceptual Data Model** — The schema in `clickup-schema.graphql` is a comprehensive conceptual GraphQL schema derived from the ClickUp REST API surface. It is intended for tooling, catalog enrichment, code generation, and integration design purposes rather than direct execution against a live GraphQL endpoint.

## REST API Endpoint

```
https://api.clickup.com/api/v2
```

## Documentation

- Developer Docs: https://developer.clickup.com/docs/tasks
- API Reference: https://developer.clickup.com/reference
- Authentication: https://developer.clickup.com/docs/authentication
- Webhooks: https://developer.clickup.com/docs/webhooks

## Core Resource Hierarchy

ClickUp organizes work in a strict hierarchy:

```
Workspace (Team)
  └── Space
        └── Folder (optional)
              └── List
                    └── Task
                          └── Subtask
```

## Notes

The conceptual GraphQL schema covers all primary resource types exposed by the ClickUp REST API, including Tasks, Lists, Folders, Spaces, Workspaces, Users, Comments, Attachments, Checklists, Custom Fields, Time Tracking, Goals, Views, Webhooks, and Automations. Query and mutation fields map directly to documented REST endpoints.
