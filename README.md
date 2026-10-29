# Clickup

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ClickUp is a work management platform — tasks, Lists, Folders, Spaces, Docs, Chat, Goals, time tracking, dashboards and automations in one Workspace. It ships a public REST API in two concurrent versions: v2 (138 operations, the broad surface) and v3 (35 operations, Chat, Docs, attachments, audit logs and ACLs), both published as first-party OpenAPI documents and advertised through an RFC 9727 api-catalog at developer.clickup.com. Authentication is a single Authorization header carrying either a personal token or an OAuth 2.0 access token authorized per Workspace; there are no OAuth scopes. Webhooks are HMAC-SHA256 signed. ClickUp also runs a remote MCP server at mcp.clickup.com with its own OAuth authorization server, PKCE and dynamic client registration, exposing 48 documented tools. Rate limits are per token and set by the Workspace plan. There is no sandbox, no idempotency mechanism and no published deprecation policy.

**Areas:** Project Management · Work Management · Productivity · Collaboration · Task · Documents · Chat · Time Tracking · MCP

## Clickup on APIs.io

Everything profiled for Clickup is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/clickup/](https://apis.io/providers/clickup/)** — or go straight to one of the APIs or properties below.

### APIs (34)

- [clickup Authorization API](https://apis.io/apis/clickup/clickup-authorization-api/) — Operations for retrieving authenticated user information.
- [clickup Comments API](https://apis.io/apis/clickup/clickup-comments-api/) — Operations for managing comments on tasks, views, and lists.
- [clickup Custom Fields API](https://apis.io/apis/clickup/clickup-custom-fields-api/) — Operations for retrieving custom field definitions and setting custom field values on tasks.
- [clickup Folders API](https://apis.io/apis/clickup/clickup-folders-api/) — Operations for managing Folders within ClickUp Spaces.
- [clickup Goals API](https://apis.io/apis/clickup/clickup-goals-api/) — Operations for managing Goals and Key Results within a ClickUp Workspace.
- [clickup Lists API](https://apis.io/apis/clickup/clickup-lists-api/) — Operations for managing Lists within ClickUp Spaces and Folders.
- [clickup Spaces API](https://apis.io/apis/clickup/clickup-spaces-api/) — Operations for managing Spaces within a ClickUp Workspace.
- [clickup Tasks API](https://apis.io/apis/clickup/clickup-tasks-api/) — Operations for creating, retrieving, updating, and deleting tasks within ClickUp lists and workspaces.
- [clickup Teams API](https://apis.io/apis/clickup/clickup-teams-api/) — Operations for retrieving Workspace (team) information and membership.
- [clickup Time Tracking API](https://apis.io/apis/clickup/clickup-time-tracking-api/) — Operations for managing time entries and timers within a ClickUp Workspace.
- [clickup Views API](https://apis.io/apis/clickup/clickup-views-api/) — Operations for managing views at various levels of the ClickUp hierarchy.
- [clickup Webhooks API](https://apis.io/apis/clickup/clickup-webhooks-api/) — Operations for creating, retrieving, updating, and deleting webhook subscriptions.
- [Clickup O Auth API](https://apis.io/apis/clickup/clickup-oauth-api/) — Operations for OAuth 2.0 authentication and token management.
- [Clickup Acls API](https://apis.io/apis/clickup/clickup-acls-api/) — Acls API
- [Clickup Attachments API](https://apis.io/apis/clickup/clickup-attachments-api/) — The Attachments API from Clickup — 2 operation(s) for attachments.
- [Clickup Audit Logs API](https://apis.io/apis/clickup/clickup-audit-logs-api/) — The Audit Logs API from Clickup — 1 operation(s) for audit logs.
- [Clickup Auditlogs API](https://apis.io/apis/clickup/clickup-auditlogs-api/) — Auditlogs API
- [Clickup Chat API](https://apis.io/apis/clickup/clickup-chat-api/) — Chat API
- [Clickup Chat (Experimental) API](https://apis.io/apis/clickup/clickup-chat-experimental-api/) — The Chat (Experimental) API from Clickup — 1 operation(s) for chat (experimental).
- [Clickup Custom Task Types API](https://apis.io/apis/clickup/clickup-custom-task-types-api/) — The Custom Task Types API from Clickup — 1 operation(s) for custom task types.
- [Clickup Docs API](https://apis.io/apis/clickup/clickup-docs-api/) — Docs API
- [Clickup Guests API](https://apis.io/apis/clickup/clickup-guests-api/) — The Guests API from Clickup — 5 operation(s) for guests.
- [Clickup Members API](https://apis.io/apis/clickup/clickup-members-api/) — The Members API from Clickup — 2 operation(s) for members.
- [Clickup Privacy and access API](https://apis.io/apis/clickup/clickup-privacy-and-access-api/) — The Privacy and access API from Clickup — 1 operation(s) for privacy and access.
- [Clickup Roles API](https://apis.io/apis/clickup/clickup-roles-api/) — The Roles API from Clickup — 1 operation(s) for roles.
- [Clickup Shared Hierarchy API](https://apis.io/apis/clickup/clickup-shared-hierarchy-api/) — The Shared Hierarchy API from Clickup — 1 operation(s) for shared hierarchy.
- [Clickup Tags API](https://apis.io/apis/clickup/clickup-tags-api/) — The Tags API from Clickup — 3 operation(s) for tags.
- [Clickup Task Checklists API](https://apis.io/apis/clickup/clickup-task-checklists-api/) — The Task Checklists API from Clickup — 4 operation(s) for task checklists.
- [Clickup Task Relationships API](https://apis.io/apis/clickup/clickup-task-relationships-api/) — The Task Relationships API from Clickup — 2 operation(s) for task relationships.
- [Clickup Templates API](https://apis.io/apis/clickup/clickup-templates-api/) — The Templates API from Clickup — 3 operation(s) for templates.
- [Clickup Time Tracking (Legacy) API](https://apis.io/apis/clickup/clickup-time-tracking-legacy-api/) — The Time Tracking (Legacy) API from Clickup — 2 operation(s) for time tracking (legacy).
- [Clickup User Groups API](https://apis.io/apis/clickup/clickup-user-groups-api/) — The User Groups API from Clickup — 3 operation(s) for user groups.
- [Clickup Users API](https://apis.io/apis/clickup/clickup-users-api/) — The Users API from Clickup — 2 operation(s) for users.
- [Clickup Workspaces API](https://apis.io/apis/clickup/clickup-workspaces-api/) — The Workspaces API from Clickup — 3 operation(s) for workspaces.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [ClickUp Webhooks Events](https://apis.io/asyncapis/clickup/clickup-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/webhook](https://apis.io/channels/clickup/webhook/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/clickup/](https://apis.io/graphqls/clickup/clickup-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [clickup](https://apis.io/servers/clickup/clickup/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Clickup Agentic Access](https://apis.io/agentic-access/clickup/clickup-agentic-access/)

#### JSON Schema (41)

The data models the API reads and writes.

- [AuthorizedUser](https://apis.io/schemas/clickup/clickup-authorizeduser/)
- [Comment](https://apis.io/schemas/clickup/clickup-comment/)
- [CreateCommentRequest](https://apis.io/schemas/clickup/clickup-createcommentrequest/)
- [CreateFolderRequest](https://apis.io/schemas/clickup/clickup-createfolderrequest/)
- [CreateGoalRequest](https://apis.io/schemas/clickup/clickup-creategoalrequest/)
- [CreateKeyResultRequest](https://apis.io/schemas/clickup/clickup-createkeyresultrequest/)
- [CreateListRequest](https://apis.io/schemas/clickup/clickup-createlistrequest/)
- [CreateSpaceRequest](https://apis.io/schemas/clickup/clickup-createspacerequest/)
- [CreateTaskRequest](https://apis.io/schemas/clickup/clickup-createtaskrequest/)
- [CreateTimeEntryRequest](https://apis.io/schemas/clickup/clickup-createtimeentryrequest/)
- [CreateWebhookRequest](https://apis.io/schemas/clickup/clickup-createwebhookrequest/)
- [CustomField](https://apis.io/schemas/clickup/clickup-customfield/)
- [CustomFieldDefinition](https://apis.io/schemas/clickup/clickup-customfielddefinition/)
- [Folder](https://apis.io/schemas/clickup/clickup-folder/)
- [Goal](https://apis.io/schemas/clickup/clickup-goal/)
- [GoalFolder](https://apis.io/schemas/clickup/clickup-goalfolder/)
- [KeyResult](https://apis.io/schemas/clickup/clickup-keyresult/)
- [List](https://apis.io/schemas/clickup/clickup-list/)
- [Member](https://apis.io/schemas/clickup/clickup-member/)
- [Priority](https://apis.io/schemas/clickup/clickup-priority/)
- [Space](https://apis.io/schemas/clickup/clickup-space/)
- [Status](https://apis.io/schemas/clickup/clickup-status/)
- [Tag](https://apis.io/schemas/clickup/clickup-tag/)
- [ClickUp Task](https://apis.io/schemas/clickup/clickup-task/)
- [Team](https://apis.io/schemas/clickup/clickup-team/)
- …and 16 more published on APIs.io

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Clickup Structure](https://apis.io/json-structure/clickup/clickup-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Clickup Context](https://apis.io/jsonld/clickup/clickup-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Clickup Domain Vocabulary](https://apis.io/vocabularies/clickup/clickup-vocabulary/)

#### Collections (25)

Postman and Open Collection request collections.

- [ClickUp Comments Authorization API](https://apis.io/collections/clickup/open-clickup-authorization-api/)
- [ClickUp Comments API](https://apis.io/collections/clickup/open-clickup-comments/)
- [ClickUp Authorization Comments API](https://apis.io/collections/clickup/open-clickup-comments-api/)
- [ClickUp Custom Fields API](https://apis.io/collections/clickup/open-clickup-custom-fields/)
- [ClickUp Comments Authorization Custom Fields API](https://apis.io/collections/clickup/open-clickup-custom-fields-api/)
- [ClickUp Folders API](https://apis.io/collections/clickup/open-clickup-folders/)
- [ClickUp Comments Authorization Folders API](https://apis.io/collections/clickup/open-clickup-folders-api/)
- [ClickUp Goals API](https://apis.io/collections/clickup/open-clickup-goals/)
- [ClickUp Comments Authorization Goals API](https://apis.io/collections/clickup/open-clickup-goals-api/)
- [ClickUp Lists API](https://apis.io/collections/clickup/open-clickup-lists/)
- [ClickUp Comments Authorization Lists API](https://apis.io/collections/clickup/open-clickup-lists-api/)
- [ClickUp OAuth API](https://apis.io/collections/clickup/open-clickup-oauth/)
- [ClickUp Comments Authorization OAuth API](https://apis.io/collections/clickup/open-clickup-oauth-api/)
- [ClickUp Spaces API](https://apis.io/collections/clickup/open-clickup-spaces/)
- [ClickUp Comments Authorization Spaces API](https://apis.io/collections/clickup/open-clickup-spaces-api/)
- [ClickUp Tasks API](https://apis.io/collections/clickup/open-clickup-tasks/)
- [ClickUp Comments Authorization Tasks API](https://apis.io/collections/clickup/open-clickup-tasks-api/)
- [ClickUp Teams (Workspaces) API](https://apis.io/collections/clickup/open-clickup-teams/)
- [ClickUp Comments Authorization Teams API](https://apis.io/collections/clickup/open-clickup-teams-api/)
- [ClickUp Time Tracking API](https://apis.io/collections/clickup/open-clickup-time-tracking/)
- [ClickUp Comments Authorization Time Tracking API](https://apis.io/collections/clickup/open-clickup-time-tracking-api/)
- [ClickUp Views API](https://apis.io/collections/clickup/open-clickup-views/)
- [ClickUp Comments Authorization Views API](https://apis.io/collections/clickup/open-clickup-views-api/)
- [ClickUp Webhooks API](https://apis.io/collections/clickup/open-clickup-webhooks/)
- [ClickUp Comments Authorization Webhooks API](https://apis.io/collections/clickup/open-clickup-webhooks-api/)

#### Overlays (36)

OpenAPI overlays, including conversational phrasing for each operation.

- [Clickup Acls Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-acls-api-phrasing-overlay/)
- [Clickup Api V2 Reference Overlay](https://apis.io/overlays/clickup/clickup-api-v2-reference-overlay/)
- [Clickup Attachments Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-attachments-api-phrasing-overlay/)
- [Clickup Audit Logs Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-audit-logs-api-phrasing-overlay/)
- [Clickup Auditlogs Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-auditlogs-api-phrasing-overlay/)
- [Clickup Authorization Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-authorization-api-phrasing-overlay/)
- [Clickup Chat Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-chat-api-phrasing-overlay/)
- [Clickup Chat Experimental Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-chat-experimental-api-phrasing-overlay/)
- [Clickup Comments Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-comments-api-phrasing-overlay/)
- [Clickup Custom Fields Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-custom-fields-api-phrasing-overlay/)
- [Clickup Custom Task Types Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-custom-task-types-api-phrasing-overlay/)
- [Clickup Docs Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-docs-api-phrasing-overlay/)
- [Clickup Folders Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-folders-api-phrasing-overlay/)
- [Clickup Goals Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-goals-api-phrasing-overlay/)
- [Clickup Guests Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-guests-api-phrasing-overlay/)
- [Clickup Lists Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-lists-api-phrasing-overlay/)
- [Clickup Members Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-members-api-phrasing-overlay/)
- [Clickup Oauth Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-oauth-api-phrasing-overlay/)
- [Clickup Privacy And Access Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-privacy-and-access-api-phrasing-overlay/)
- [Clickup Public Api V3 Overlay](https://apis.io/overlays/clickup/clickup-public-api-v3-overlay/)
- [Clickup Roles Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-roles-api-phrasing-overlay/)
- [Clickup Shared Hierarchy Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-shared-hierarchy-api-phrasing-overlay/)
- [Clickup Spaces Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-spaces-api-phrasing-overlay/)
- [Clickup Tags Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-tags-api-phrasing-overlay/)
- [Clickup Task Checklists Api Phrasing Overlay](https://apis.io/overlays/clickup/clickup-task-checklists-api-phrasing-overlay/)
- …and 11 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Clickup — asyncapi rules](https://apis.io/rules/clickup/clickup-asyncapi-spectral-rules/)
- [Clickup — jsonschema rules](https://apis.io/rules/clickup/clickup-jsonschema-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Clickup Authentication](https://apis.io/security/clickup/clickup-authentication/)
- [Clickup Domain Security](https://apis.io/security/clickup/clickup-domain-security/)
- [Clickup Trust Center](https://apis.io/security/clickup/clickup-trust-center/)
- [Clickup Vulnerability Disclosure](https://apis.io/security/clickup/clickup-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Clickup Scopes](https://apis.io/scopes/clickup/clickup-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Clickup Plans Pricing](https://apis.io/plans/clickup/clickup-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Clickup Rate Limits](https://apis.io/rate-limits/clickup/clickup-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Clickup Finops](https://apis.io/finops/clickup/clickup-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.clickup.com/)
- [Documentation](https://developer.clickup.com/docs)
- [Getting started](https://developer.clickup.com/docs/authentication)
- [API reference](https://developer.clickup.com/reference)
- [Pricing](https://clickup.com/pricing)
- [Sign up](https://app.clickup.com/signup)
- [Support](https://help.clickup.com/hc/en-us)
- [Changelog](https://clickup.canny.io/changelog)
- [Blog](https://clickup.com/blog)
- [Security](https://clickup.com/security)
- [Compliance](https://security.clickup.com/)
- [Terms of service](https://clickup.com/terms)
- [Privacy policy](https://clickup.com/terms/privacy)
- [GitHub](https://github.com/clickup)
- [Status](https://status.clickup.com/)

## API Evangelist rating

**Kin Score 70.9** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 63.7 |
| Contract governance | 31.8 |
| Operational transparency | 85.5 |
| Developer ergonomics | 62.5 |
| Access clarity | 78.9 |

**Agent readiness 57.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/clickup/](https://apis.io/providers/clickup/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Clickup: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/clickup/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
