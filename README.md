# ClickUp (clickup)
ClickUp is a comprehensive project management and productivity platform that brings tasks, docs, goals, and collaboration into a single workspace. Their developer platform offers a REST API that enables programmatic access to workspaces, tasks, spaces, lists, time tracking, custom fields, and real-time webhooks for building integrations and automations.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Project Management, Tasks, Productivity, Collaboration, Workspaces

## Timestamps

- **Created:** 2026-03-20
- **Modified:** 2026-03-20

## APIs

### ClickUp Tasks API
The ClickUp Tasks API allows developers to create, read, update, and delete tasks within ClickUp workspaces. Tasks are the core unit of work in ClickUp and can include custom fields, assignees, due dates, tags, priorities, and attachments. The API supports filtering tasks by list, space, or project, and enables bulk operations for managing large numbers of tasks programmatically.

**Human URL:** [https://developer.clickup.com/docs/tasks](https://developer.clickup.com/docs/tasks)


#### Tags:

 - Project Management, Tasks, Productivity, Collaboration

#### Properties

- [Documentation](https://developer.clickup.com/docs/tasks)

### ClickUp Spaces API
The ClickUp Spaces API provides endpoints for managing Spaces, which are the top-level organizational containers within a ClickUp Workspace. Spaces contain Folders and Lists that organize tasks into logical groupings. Developers can create, update, and delete Spaces, as well as retrieve Space details and configure Space-level settings such as enabled features and statuses.

**Human URL:** [https://developer.clickup.com/reference/get-spaces](https://developer.clickup.com/reference/get-spaces)


#### Tags:

 - Project Management, Workspaces, Organization

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-spaces)

### ClickUp Lists API
The ClickUp Lists API enables developers to manage Lists, which are containers that hold tasks within a Space or Folder. Lists define the workflow statuses available to tasks and serve as the primary grouping mechanism for related work items. The API supports creating, updating, and deleting Lists, as well as retrieving List details and the tasks they contain.

**Human URL:** [https://developer.clickup.com/reference/get-lists](https://developer.clickup.com/reference/get-lists)


#### Tags:

 - Project Management, Lists, Task Organization

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-lists)

### ClickUp Folders API
The ClickUp Folders API provides endpoints for managing Folders, which are optional organizational containers that sit between Spaces and Lists in the ClickUp hierarchy. Folders group related Lists together and can be used to organize projects or workstreams within a Space. Developers can create, update, delete, and retrieve Folders and their associated Lists.

**Human URL:** [https://developer.clickup.com/reference/get-folders](https://developer.clickup.com/reference/get-folders)


#### Tags:

 - Project Management, Folders, Organization

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-folders)

### ClickUp Goals API
The ClickUp Goals API allows developers to create and manage goals within a Workspace. Goals can track progress toward objectives using targets based on numbers, currency, percentages, or task completion. The API supports creating goals, adding key results and targets, updating progress, and retrieving goal details. This is useful for building OKR tracking and reporting integrations.

**Human URL:** [https://developer.clickup.com/reference/get-goals](https://developer.clickup.com/reference/get-goals)


#### Tags:

 - Project Management, Goals, Tracking, OKR

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-goals)

### ClickUp Comments API
The ClickUp Comments API provides endpoints for creating and retrieving comments on tasks, views, and lists. Comments support rich text formatting, mentions, and attachments. Developers can use this API to build integrations that synchronize discussions between ClickUp and other collaboration tools, or to programmatically add status updates and notes to tasks.

**Human URL:** [https://developer.clickup.com/reference/get-task-comments](https://developer.clickup.com/reference/get-task-comments)


#### Tags:

 - Project Management, Comments, Collaboration

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-task-comments)

### ClickUp Teams (Workspaces) API
The ClickUp Teams API provides access to Workspace-level information and membership. In the ClickUp API, Teams correspond to Workspaces, which are the top-level organizational unit. The API allows developers to retrieve a list of Workspaces the authenticated user belongs to, along with member details and roles. This is typically the starting point for navigating the ClickUp hierarchy.

**Human URL:** [https://developer.clickup.com/reference/get-teams](https://developer.clickup.com/reference/get-teams)


#### Tags:

 - Project Management, Teams, Workspaces, Users

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-teams)

### ClickUp Webhooks API
The ClickUp Webhooks API enables developers to subscribe to real-time events within a Workspace. When subscribed events occur, ClickUp sends HTTP POST requests to a specified endpoint URL with event details. Webhooks support events for tasks, lists, folders, spaces, and goals. Each webhook payload is signed with a shared secret for verification, ensuring the event originated from ClickUp.

**Human URL:** [https://developer.clickup.com/docs/webhooks](https://developer.clickup.com/docs/webhooks)


#### Tags:

 - Project Management, Webhooks, Events, Real-Time

#### Properties

- [Documentation](https://developer.clickup.com/docs/webhooks)

### ClickUp Custom Fields API
The ClickUp Custom Fields API allows developers to retrieve available custom fields for a list and set or update custom field values on tasks. Custom fields extend the default task data model with user-defined attributes such as dropdowns, labels, numbers, dates, and relationships. This API is essential for integrations that need to read or write structured metadata beyond the standard task fields.

**Human URL:** [https://developer.clickup.com/reference/get-accessible-custom-fields](https://developer.clickup.com/reference/get-accessible-custom-fields)


#### Tags:

 - Project Management, Custom Fields, Metadata

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-accessible-custom-fields)

### ClickUp Time Tracking API
The ClickUp Time Tracking API provides endpoints for recording and retrieving time entries associated with tasks. Developers can create manual time entries, start and stop timers, and query time entries within date ranges and across team members. This API supports building time reporting dashboards, invoicing integrations, and productivity analysis tools.

**Human URL:** [https://developer.clickup.com/reference/get-time-entries-within-a-date-range](https://developer.clickup.com/reference/get-time-entries-within-a-date-range)


#### Tags:

 - Project Management, Time Tracking, Productivity, Reporting

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-time-entries-within-a-date-range)

### ClickUp Views API
The ClickUp Views API enables developers to create and manage views at the team, space, folder, and list levels. Views define how tasks are displayed and filtered, supporting formats such as list, board, calendar, gantt, and table. The API allows programmatic creation of saved views with specific filters, groupings, and sort configurations.

**Human URL:** [https://developer.clickup.com/reference/get-views](https://developer.clickup.com/reference/get-views)


#### Tags:

 - Project Management, Views, Dashboards

#### Properties

- [Documentation](https://developer.clickup.com/reference/get-views)

### ClickUp OAuth API
The ClickUp OAuth API implements the authorization code grant type, allowing third-party applications to authenticate users and access their ClickUp Workspaces. Workspace owners or admins can create OAuth apps, and users authorize access by granting permissions to specific Workspaces. The API provides endpoints for obtaining authorization codes, exchanging them for access tokens, and retrieving the authenticated user's information.

**Human URL:** [https://developer.clickup.com/docs/authentication](https://developer.clickup.com/docs/authentication)


#### Tags:

 - Project Management, Authentication, OAuth, Authorization

#### Properties

- [Documentation](https://developer.clickup.com/docs/authentication)

## Common Properties

- [Developer Portal](https://developer.clickup.com)
- [API Reference](https://developer.clickup.com/reference)
- [Authentication](https://developer.clickup.com/docs/authentication)
- [Webhooks](https://developer.clickup.com/docs/webhooks)
- [Website](https://clickup.com)
- [Blog](https://clickup.com/blog)
- [PrivacyPolicy](https://clickup.com/privacy)
- [TermsOfService](https://clickup.com/terms)
- [Support](https://help.clickup.com)
- [Login](https://app.clickup.com)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
