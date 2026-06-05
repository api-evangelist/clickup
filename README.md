# clickup (clickup)

Work with tasks using the ClickUp API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/apis.yml)

## Timestamps

- **Modified:** 2026-05-19

## APIs

### ClickUp Tasks API

The ClickUp Tasks API allows developers to create, read, update, and delete tasks within ClickUp workspaces. Tasks are the core unit of work in ClickUp and can include custom fields, assignees, due dates, tags, priorities, and attachments. The API supports filtering tasks by list, space, or project, and enables bulk operations for managing large numbers of tasks programmatically.

- **Human URL:** [https://developer.clickup.com/docs/tasks](https://developer.clickup.com/docs/tasks)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Collaboration
- Productivity
- Project Management
- Tasks

#### Properties

- [Documentation](https://developer.clickup.com/docs/tasks)
- [OpenAPI](openapi/clickup-tasks-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-tasks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-tasks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Spaces API

The ClickUp Spaces API provides endpoints for managing Spaces, which are the top-level organizational containers within a ClickUp Workspace. Spaces contain Folders and Lists that organize tasks into logical groupings. Developers can create, update, and delete Spaces, as well as retrieve Space details and configure Space-level settings such as enabled features and statuses.

- **Human URL:** [https://developer.clickup.com/reference/get-spaces](https://developer.clickup.com/reference/get-spaces)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Organization
- Project Management
- Workspaces

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-spaces)
- [OpenAPI](openapi/clickup-spaces-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-spaces.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-spaces.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Lists API

The ClickUp Lists API enables developers to manage Lists, which are containers that hold tasks within a Space or Folder. Lists define the workflow statuses available to tasks and serve as the primary grouping mechanism for related work items. The API supports creating, updating, and deleting Lists, as well as retrieving List details and the tasks they contain.

- **Human URL:** [https://developer.clickup.com/reference/get-lists](https://developer.clickup.com/reference/get-lists)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Lists
- Project Management
- Task Organization

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-lists)
- [OpenAPI](openapi/clickup-lists-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-lists.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-lists.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Folders API

The ClickUp Folders API provides endpoints for managing Folders, which are optional organizational containers that sit between Spaces and Lists in the ClickUp hierarchy. Folders group related Lists together and can be used to organize projects or workstreams within a Space. Developers can create, update, delete, and retrieve Folders and their associated Lists.

- **Human URL:** [https://developer.clickup.com/reference/get-folders](https://developer.clickup.com/reference/get-folders)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Folders
- Organization
- Project Management

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-folders)
- [OpenAPI](openapi/clickup-folders-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-folders.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-folders.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Goals API

The ClickUp Goals API allows developers to create and manage goals within a Workspace. Goals can track progress toward objectives using targets based on numbers, currency, percentages, or task completion. The API supports creating goals, adding key results and targets, updating progress, and retrieving goal details. This is useful for building OKR tracking and reporting integrations.

- **Human URL:** [https://developer.clickup.com/reference/get-goals](https://developer.clickup.com/reference/get-goals)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Goals
- OKR
- Project Management
- Tracking

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-goals)
- [OpenAPI](openapi/clickup-goals-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-goals.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-goals.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Comments API

The ClickUp Comments API provides endpoints for creating and retrieving comments on tasks, views, and lists. Comments support rich text formatting, mentions, and attachments. Developers can use this API to build integrations that synchronize discussions between ClickUp and other collaboration tools, or to programmatically add status updates and notes to tasks.

- **Human URL:** [https://developer.clickup.com/reference/get-task-comments](https://developer.clickup.com/reference/get-task-comments)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Collaboration
- Comments
- Project Management

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-task-comments)
- [OpenAPI](openapi/clickup-comments-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-comments.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-comments.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Teams (Workspaces) API

The ClickUp Teams API provides access to Workspace-level information and membership. In the ClickUp API, Teams correspond to Workspaces, which are the top-level organizational unit. The API allows developers to retrieve a list of Workspaces the authenticated user belongs to, along with member details and roles. This is typically the starting point for navigating the ClickUp hierarchy.

- **Human URL:** [https://developer.clickup.com/reference/get-teams](https://developer.clickup.com/reference/get-teams)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Project Management
- Teams
- Users
- Workspaces

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-teams)
- [OpenAPI](openapi/clickup-teams-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-teams.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-teams.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Webhooks API

The ClickUp Webhooks API enables developers to subscribe to real-time events within a Workspace. When subscribed events occur, ClickUp sends HTTP POST requests to a specified endpoint URL with event details. Webhooks support events for tasks, lists, folders, spaces, and goals. Each webhook payload is signed with a shared secret for verification, ensuring the event originated from ClickUp.

- **Human URL:** [https://developer.clickup.com/docs/webhooks](https://developer.clickup.com/docs/webhooks)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Events
- Project Management
- Real-Time
- Webhooks

#### Properties

- [Documentation](https://developer.clickup.com/docs/webhooks)
- [OpenAPI](openapi/clickup-webhooks-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-webhooks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-webhooks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/clickup-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### ClickUp Custom Fields API

The ClickUp Custom Fields API allows developers to retrieve available custom fields for a list and set or update custom field values on tasks. Custom fields extend the default task data model with user-defined attributes such as dropdowns, labels, numbers, dates, and relationships. This API is essential for integrations that need to read or write structured metadata beyond the standard task fields.

- **Human URL:** [https://developer.clickup.com/reference/get-accessible-custom-fields](https://developer.clickup.com/reference/get-accessible-custom-fields)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Custom Fields
- Metadata
- Project Management

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-accessible-custom-fields)
- [OpenAPI](openapi/clickup-custom-fields-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-custom-fields.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-custom-fields.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Time Tracking API

The ClickUp Time Tracking API provides endpoints for recording and retrieving time entries associated with tasks. Developers can create manual time entries, start and stop timers, and query time entries within date ranges and across team members. This API supports building time reporting dashboards, invoicing integrations, and productivity analysis tools.

- **Human URL:** [https://developer.clickup.com/reference/get-time-entries-within-a-date-range](https://developer.clickup.com/reference/get-time-entries-within-a-date-range)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Productivity
- Project Management
- Reporting
- Time Tracking

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-time-entries-within-a-date-range)
- [OpenAPI](openapi/clickup-time-tracking-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-time-tracking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-time-tracking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp Views API

The ClickUp Views API enables developers to create and manage views at the team, space, folder, and list levels. Views define how tasks are displayed and filtered, supporting formats such as list, board, calendar, gantt, and table. The API allows programmatic creation of saved views with specific filters, groupings, and sort configurations.

- **Human URL:** [https://developer.clickup.com/reference/get-views](https://developer.clickup.com/reference/get-views)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Dashboards
- Project Management
- Views

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-views)
- [OpenAPI](openapi/clickup-views-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-views.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-views.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClickUp OAuth API

The ClickUp OAuth API implements the authorization code grant type, allowing third-party applications to authenticate users and access their ClickUp Workspaces. Workspace owners or admins can create OAuth apps, and users authorize access by granting permissions to specific Workspaces. The API provides endpoints for obtaining authorization codes, exchanging them for access tokens, and retrieving the authenticated user's information.

- **Human URL:** [https://developer.clickup.com/docs/authentication](https://developer.clickup.com/docs/authentication)
- **Base URL:** `https://api.clickup.com`

#### Tags

- Authentication
- Authorization
- OAuth
- Project Management

#### Properties

- [Documentation](https://developer.clickup.com/docs/authentication)
- [OpenAPI](openapi/clickup-oauth-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clickup-oauth.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clickup-oauth.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/clickup)
- [LinkedIn](https://www.linkedin.com/company/clickup-app)
- [JSON-LD](json-ld/clickup-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/clickup-task-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/clickup-webhook-payload-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Features](undefined)
- [L L Ms Txt](https://developer.clickup.com/llms.txt)
