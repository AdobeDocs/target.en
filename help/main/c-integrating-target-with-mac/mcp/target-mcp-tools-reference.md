---
solution: Target
product: target
title: Adobe Target MCP server tools reference
description: Complete parameter reference for all 39 public tools exposed by the Adobe Target MCP server.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
hide: true
---
# [!DNL Adobe Target] MCP server tools reference {#target-mcp-tools-reference}

>[!BEGINSHADEBOX]

Table of contents:

* [Work with MCP clients](target-mcp.md)
* **[MCP server tools reference](target-mcp-tools-reference.md)**

>[!ENDSHADEBOX]

This page is a complete reference for all public tools exposed by the [!DNL Adobe Target] MCP server. For each tool you'll find a description, parameter details, return value, and an example natural-language prompt. For setup instructions and use cases, see [Work with MCP clients](target-mcp.md).

>[!NOTE]
>
>Read tools are available to all connected users with **Observer** role or higher; write tools require **Editor** or **Approver** role.

>[!IMPORTANT]
>
>The Model Context Protocol (MCP) is an emerging open-source standard and may present security or reliability risks. Adobe MCP server integrations and related documentation are provided "as is," without warranties of any kind.
>
>Connecting MCP clients or servers to Adobe products is a customer-elected configuration, and customers are responsible for evaluating the security and suitability of any MCP integration. Adobe is not responsible for issues arising from misconfiguration, misuse of the MCP, vulnerabilities in third-party implementations, or unintended actions performed through MCP-enabled workflows.
>
>To reduce risk, Adobe encourages testing integrations in a sandbox environment prior to productive use and carefully reviewing and validating all MCP-initiated actions and responses before confirming or relying on them.

## Activity tools {#tools-activities}

+++List activities

**Tool:** `list_target_activities`

List [!DNL Adobe Target] activities with server-side filtering and sorting.

Retrieves a paginated list of activities. All filters are applied server-side by the [!DNL Target] Admin API. The server returns at most 200 activities per page.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `limit` | integer | No | Maximum number of activities to return (server max: 200) |
| `offset` | integer | No | Number of activities to skip for pagination |
| `sort_by` | string | No | Field to sort by. Prefix with `-` for descending order (e.g., `-modifiedAt`). Options: `id`, `name`, `state`, `priority`, `startsAt`, `endsAt`, `lifetimeStart`, `lifetimeEnd`, `createdAt`, `createdBy`, `modifiedAt`, `modifiedBy`, `type`, `thirdPartyId` |
| `state` | string | No | Filter by activity state: `approved` (live/active), `deactivated` (inactive), `paused`, `saved` (draft) |
| `activity_type` | string | No | Filter by type: `ab` (A/B Test), `xt` (Experience Targeting), `abt` (Automated Personalization) |
| `name_contains` | string | No | Filter activities whose name contains this string (case-insensitive) |
| `starts_after` | string | No | ISO 8601 date — activities starting after this date |
| `starts_before` | string | No | ISO 8601 date — activities starting before this date |
| `modified_after` | string | No | ISO 8601 date — activities modified after this date |
| `ends_after` | string | No | ISO 8601 date — activities ending after this date |
| `ends_before` | string | No | ISO 8601 date — activities ending before this date |
| `workspace` | string | No | Filter by workspace ID |
| `segment_id` | string | No | Filter by audience segment ID |
| `profile_attribute_id` | string | No | Filter by profile attribute ID |
| `priority` | integer | No | Filter by exact priority value (0–999) |
| `mbox` | string | No | Filter by mbox/location name |
| `offer_id` | string | No | Filter by offer ID |
| `view_id` | string | No | Filter by SPA view ID |

**Returns:** JSON object with `activities` (list of objects including `id`, `name`, `state`, `type`, `priority`, `modifiedAt`, `startsAt`, `endsAt`) and `total` (total count, may exceed the returned page size).

**Example prompt:** "List all active A/B tests sorted by most recently modified."

+++

+++Get an A/B activity

**Tool:** `get_ab_activity`

Get detailed information about an A/B activity.

Retrieves the full configuration of a specific A/B test, including experiences, locations, metrics, and targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the A/B activity |

**Returns:** Full activity details including metadata (name, state, priority, dates), experiences, locations and offers, goals and metrics, and targeting rules.

**Example prompt:** "Get details for A/B activity 12345."

+++

+++Get an Experience Targeting activity

**Tool:** `get_xt_activity`

Get detailed information about an Experience Targeting (XT) activity.

Retrieves the full configuration of a specific XT activity, including audience-experience mappings, locations, and metrics.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity |

**Returns:** Full activity details including metadata, experiences with audience mappings, locations and offers, and goals and metrics.

**Example prompt:** "Get details for Experience Targeting activity 12345."

+++

+++Get an Automated Personalization activity

**Tool:** `get_abt_activity`

Get detailed information about an Automated Personalization (AP) activity.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the AP activity |

**Returns:** Full activity details including metadata, experiences, locations, and algorithmic settings.

**Example prompt:** "Get details for Auto-Personalization activity 12345."

+++

+++Create an A/B activity

**Tool:** `create_ab_activity`

Create a new A/B test activity.

Creates a new A/B test with the specified configuration including experiences, offers, and targeting.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `audiences` | array | No | Target audience configurations |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an A/B test called 'Homepage Hero Test' with two experiences testing different hero images on the homepage-hero mbox."

+++

+++Create an Experience Targeting activity

**Tool:** `create_xt_activity`

Create a new Experience Targeting (XT) activity.

Creates an XT activity that delivers different experiences to different audiences based on targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations with audience mappings |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an Experience Targeting activity called 'Geo Personalization' that shows different content to visitors from different regions."

+++

+++Update an A/B activity

**Tool:** `update_ab_activity`

Update an existing A/B activity.

Uses a read-modify-write pattern: fetches the current state, merges your changes, validates, and sends the update.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity to update |
| `activity` | object | Yes | Fields to update (name, priority, experiences, locations, goals, etc.) |

**Returns:** The updated activity object.

**Example prompt:** "Update activity 12345 to change the traffic allocation to 70/30."

+++

+++Update an Experience Targeting activity

**Tool:** `update_xt_activity`

Update an existing Experience Targeting activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update XT activity 12345 to add a new experience for mobile visitors."

+++

+++Update an Automated Personalization activity

**Tool:** `update_abt_activity`

Update an existing Automated Personalization activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the AP activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update Auto-Personalization activity 12345 to change the optimization goal."

+++

+++Update activity schedule

**Tool:** `update_activity_schedule`

Update activity start and end dates.

Updates the schedule for an activity without modifying other settings.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `activity_type` | string | Yes | Type of activity: `ab`, `xt`, or `abt` |
| `starts_at` | string | No | New start date (ISO 8601) |
| `ends_at` | string | No | New end date (ISO 8601) |

**Returns:** Confirmation of the schedule update.

**Example prompt:** "Update the schedule for A/B activity 12345 to run from May 1st to May 31st."

+++

+++Change activity state

**Tool:** `update_activity_state`

Change activity state (activate, deactivate, or pause).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `state` | string | Yes | New state: `approved` (live/active), `deactivated` (inactive), `paused`, or `saved` (draft) |

**Returns:** The updated activity state.

**Example prompt:** "Activate activity 12345" or "Pause the Homepage Hero Test."

+++

+++Rename an activity

**Tool:** `update_activity_name`

Rename an activity.

Updates only the name without modifying the full configuration.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `name` | string | Yes | New activity name |

**Returns:** The updated activity object.

**Example prompt:** "Rename activity 12345 to 'Summer Campaign Hero Test'."

+++

+++Change activity priority

**Tool:** `update_activity_priority`

Change activity priority.

Higher-priority activities take precedence when multiple activities target the same location.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `priority` | integer | Yes | New priority value (0–999; higher = higher priority) |

**Returns:** The updated activity object.

**Example prompt:** "Set the priority of activity 12345 to 100."

+++

+++Add a variant to an activity

**Tool:** `add_activity_variant`

Add a new experience/variant to an activity.

Handles all structural coordination including creating options, mapping to locations, and rebalancing traffic.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name for the new experience/variant |
| `offer_id` | integer | No | (Form-based) Existing offer ID to use |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `traffic_percentage` | integer | No | Traffic % for the new variant (1–99). If omitted, traffic is rebalanced evenly |
| `audience_id` | integer | No | Audience ID for the variant (XT activities) |
| `modifications` | array | No | (VEC) List of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Add a new variant called 'Holiday Theme' to A/B activity 12345 using offer 67890."

+++

+++Update traffic split

**Tool:** `update_traffic_split`

Update traffic allocation across variants.

The percentages must sum to exactly 100.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab` or `abt` (XT not supported — audience-targeted) |
| `splits` | object | Yes | Dictionary mapping experience name to percentage. Must include all experiences and sum to 100 |

**Returns:** The updated activity object.

**Example prompt:** "Change the traffic split for activity 12345 to 70% Control and 30% Variant A."

+++

+++Change a variant's offer

**Tool:** `update_variant_offer`

Change the offer for a specific variant.

Works for both form-based activities (using `offer_id`) and VEC activities (using `modifications`).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to update |
| `offer_id` | integer | No | (Form-based) New offer ID |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `modifications` | array | No | (VEC) New list of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Update the 'Variant A' experience in activity 12345 to use offer 99999."

+++

+++Remove a variant from an activity

**Tool:** `remove_activity_variant`

Remove an experience/variant from an activity.

Removes the experience, cleans up orphaned options, and rebalances traffic evenly across remaining variants.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to remove |

**Returns:** The updated activity object.

**Example prompt:** "Remove the 'Test Variant' experience from A/B activity 12345."

+++

## Offer tools {#tools-offers}

+++List offers

**Tool:** `list_target_offers`

List all offers in your [!DNL Target] tenant.

Retrieves a paginated list of content offers with optional filtering.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `limit` | integer | No | Maximum number of offers to return |
| `offset` | integer | No | Number of offers to skip for pagination |
| `type` | string | No | Filter by offer type: `content` (HTML), `json`, or `redirect` |
| `name` | string | No | Filter by offer name (partial match) |

**Returns:** JSON object with `offers` (list of objects including `id`, `name`, `type`, `content`, `modifiedAt`) and `total`.

**Example prompt:** "List all JSON offers."

+++

+++Get an offer

**Tool:** `get_target_offer`

Get detailed information about a specific offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `offer_id` | integer | Yes | The unique identifier of the offer |

**Returns:** Full offer details including `id`, `name`, `type`, `content`, `workspace`, and `modifiedAt`.

**Example prompt:** "Get details for offer 67890."

+++

+++Create an HTML offer

**Tool:** `create_target_offer`

Create a new HTML content offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | string | Yes | HTML or text content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create an HTML offer called 'Summer Sale Banner' with a promotional banner."

+++

+++Create a JSON offer

**Tool:** `create_target_json_offer`

Create a new JSON offer for delivering structured data.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | object | Yes | JSON content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create a JSON offer called 'Feature Flags Config' with feature toggle settings."

+++

+++Update an offer

**Tool:** `update_target_offer`

Update an existing offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `offer_id` | integer | Yes | The unique identifier of the offer to update |
| `name` | string | No | Updated offer name |
| `content` | string or object | No | Updated offer content |

**Returns:** The updated offer object.

**Example prompt:** "Update offer 67890 with new promotional content."

+++

## Audience tools {#tools-audiences}

+++List audiences

**Tool:** `list_target_audiences`

List all audiences in your [!DNL Target] tenant.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `limit` | integer | No | Maximum number of audiences to return |
| `offset` | integer | No | Number of audiences to skip for pagination |

**Returns:** JSON object with `audiences` (list of objects including `id`, `name`, `description`, `origin`, `modifiedAt`) and `total`.

**Example prompt:** "List all audiences."

+++

+++Create an audience

**Tool:** `create_target_audience`

Create a new audience with targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the audience |
| `description` | string | No | Description of the audience |
| `targetRule` | object | No | Targeting rules (geo, browser, custom attributes, etc.) |
| `workspace_id` | string | No | Workspace ID for the audience |

**Returns:** The created audience with its assigned ID.

**Example prompt:** "Create an audience called 'Mobile Visitors from California' targeting mobile users in CA."

+++

## Mbox tools {#tools-mboxes}

+++List mboxes

**Tool:** `list_target_mboxes`

List all mboxes in your [!DNL Target] tenant.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `limit` | integer | No | Maximum number of mboxes to return |
| `offset` | integer | No | Number of mboxes to skip for pagination |
| `name` | string | No | Filter by mbox name (partial match) |
| `status` | string | No | Filter by status |

**Returns:** JSON object with `mboxes` (list of objects including `name`, `status`, `lastRequestTime`) and `total`.

**Example prompt:** "List all mboxes containing 'homepage'."

+++

+++Get an mbox

**Tool:** `get_target_mbox`

Get detailed information about a specific mbox.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `mbox_name` | string | Yes | The name of the mbox |

**Returns:** Mbox details including `name`, `status`, and list of activities using the mbox.

**Example prompt:** "Get details for mbox 'homepage-hero'."

+++

+++List mbox profile attributes

**Tool:** `list_target_mbox_profile_attributes`

List all mbox profile attributes available for targeting.

No parameters required.

**Returns:** JSON array of profile attribute objects.

**Example prompt:** "What profile attributes are available for targeting?"

+++

## Property tools {#tools-properties}

+++List properties

**Tool:** `list_target_properties`

List all properties in your [!DNL Target] tenant.

Properties organize activities and control access.

No parameters required.

**Returns:** List of property objects including `id`, `name`, `description`, and `channel`.

**Example prompt:** "List all Target properties."

+++

## Reporting tools {#tools-reporting}

+++Get an A/B performance report

**Tool:** `get_ab_performance_report`

Get a performance report for an A/B activity.

Retrieves conversion rates, lift, and confidence levels.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the A/B activity |
| `report_interval` | string | No | Time period for the report (e.g., `last7days`, `last30days`, or a custom date range) |

**Returns:** Experience-level metrics (visitors, conversions, conversion rate), lift calculations, statistical confidence levels, and revenue metrics (if configured).

**Example prompt:** "Show me the performance report for A/B test 12345 over the last 30 days."

+++

+++Get an A/B orders report

**Tool:** `get_ab_orders_report`

Get an orders/revenue report for an A/B activity.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the A/B activity |
| `report_interval` | string | No | Time period for the report |

**Returns:** Order counts, revenue, and average order value by experience.

**Example prompt:** "Get the orders report for activity 12345."

+++

+++Get an Experience Targeting performance report

**Tool:** `get_xt_performance_report`

Get a performance report for an Experience Targeting activity.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity |
| `report_interval` | string | No | Time period for the report |

**Returns:** Experience-level performance metrics.

**Example prompt:** "Show performance for my Experience Targeting activity 54321."

+++

+++Get an Experience Targeting orders report

**Tool:** `get_xt_orders_report`

Get an orders/revenue report for an Experience Targeting activity.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity |
| `report_interval` | string | No | Time period for the report |

**Returns:** Order metrics by experience.

**Example prompt:** "Get orders data for XT activity 54321."

+++

+++Get a performance report by activity name

**Tool:** `get_activity_report_by_name`

Search for an activity by name and get its performance report.

Useful when you know the activity name but not its ID.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_name` | string | Yes | Name of the activity to search for |
| `report_interval` | string | No | Time period for the report |

**Returns:** Activity details and performance metrics.

**Example prompt:** "Get the performance report for my 'Homepage Hero Test' activity."

+++

## Preview tools {#tools-preview}

+++Preview an activity

**Tool:** `preview_activity`

Generate browser QA preview URLs for a [!DNL Target] activity.

Creates clickable preview links that force specific experiences to display, bypassing audience targeting rules. Works for A/B, XT, and Automated Personalization activities.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The [!DNL Target] activity ID to preview |
| `experience_index` | integer | No | 0-based experience index. If omitted, returns URLs for all experiences |
| `url` | string | No | Page URL for preview. Required for form-based activities. For VEC activities, overrides the authored location if provided |

**Returns:** Activity information (name, type, state), preview URLs for each experience, and experience names and indexes.

**Example prompt:** "Generate preview URLs for activity 12345 so I can test each experience in my browser."

+++

## Response token tools {#tools-response-tokens}

+++List response tokens

**Tool:** `list_target_response_tokens`

List all response tokens in your [!DNL Target] tenant.

Retrieves all configured response tokens, both built-in and custom.

No parameters required.

**Returns:** JSON array of response token objects with `name`, `type`, and `enabled` status.

**Example prompt:** "List all response tokens."

+++

+++Create a response token

**Tool:** `create_target_response_token`

Create a new custom response token for collecting additional data in [!DNL Target] responses.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `token_name` | string | Yes | Name of the response token |
| `token_type` | string | Yes | Type of token: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO`, or `CRS` |

**Returns:** The created response token object.

**Example prompt:** "Create a custom response token called 'campaign_id' of type ACTIVITY."

+++

## Revision tools {#tools-revisions}

+++Get the audit log

**Tool:** `get_target_revisions`

Get the audit log for a resource type.

Retrieves changes made to [!DNL Target] resources with optional filtering by author.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `revision_resource_type` | string | Yes | Type of resource: `activity`, `offer`, or `audience` |
| `modified_by` | string | No | Filter by user who made changes |
| `limit` | integer | No | Maximum number of revisions to return |
| `offset` | integer | No | Number of revisions to skip for pagination |

**Returns:** Revision history with timestamps, users, and change descriptions.

**Example prompt:** "Show me the audit log for activity changes."

+++

+++Get revisions for a specific entity

**Tool:** `get_target_entity_revisions`

Get all revisions of a specific entity by ID.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `revision_resource_type` | string | Yes | Type of resource: `activity`, `offer`, or `audience` |
| `entity_id` | integer | Yes | The unique identifier of the entity |

**Returns:** JSON array of all revisions for the specified entity.

**Example prompt:** "Show me all changes made to activity 12345."

+++

## Template tools {#tools-templates}

+++List available templates

**Tool:** `list_target_templates`

List available MCP resources and templates for creating activities and offers.

No parameters required.

**Returns:** JSON object listing available templates and resources.

**Example prompt:** "What templates are available for creating activities?"

+++

## Tools summary {#tools-summary}

| Category | Count | Tools |
|---|---|---|
| Activity | 17 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity`, `create_ab_activity`, `create_xt_activity`, `update_ab_activity`, `update_xt_activity`, `update_abt_activity`, `update_activity_schedule`, `update_activity_state`, `update_activity_name`, `update_activity_priority`, `add_activity_variant`, `update_traffic_split`, `update_variant_offer`, `remove_activity_variant` |
| Offer | 5 | `list_target_offers`, `get_target_offer`, `create_target_offer`, `create_target_json_offer`, `update_target_offer` |
| Audience | 2 | `list_target_audiences`, `create_target_audience` |
| Mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Property | 1 | `list_target_properties` |
| Reporting | 5 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name` |
| Preview | 1 | `preview_activity` |
| Response token | 2 | `list_target_response_tokens`, `create_target_response_token` |
| Revision | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| Template | 1 | `list_target_templates` |
| **Total** | **39** | |

## Related resources {#tools-related}

* [Work with MCP clients](target-mcp.md)
* [[!DNL Adobe Target] Admin API reference](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
