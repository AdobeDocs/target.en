---
solution: Target
product: target
title: Work with MCP clients
description: Learn how to connect Adobe Target to MCP clients using the MCP server
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
---
# Work with MCP clients {#target-mcp}

>[!AVAILABILITY]
>
>The [!DNL Adobe Target] MCP server is currently available in **Claude Web**, **Claude Desktop**, and **Claude Code**. Support for additional MCP-compatible applications will be added in future releases.

The [!DNL Adobe Target] MCP integration lets you inspect, analyze, and manage A/B tests, personalization activities, and Recommendations criteria directly from Claude. Turn [!DNL Target]'s read and write APIs into plain-language workflows — audit your experiment portfolio, review performance reports, manage audiences and offers, and take governed actions without navigating the UI or writing API calls. This page explains how the integration works, what you can do with it, and how to get started.

## What is the Model Context Protocol? {#mcp-overview}

Marketing and optimization teams increasingly rely on chat-based applications and developer tools — such as Anthropic Claude, OpenAI ChatGPT, Cursor, and Microsoft Copilot Studio — to streamline their day-to-day work. These applications support the **Model Context Protocol (MCP)**, an open standard that lets applications expose back-end tools to large language models (LLMs) in a uniform way.

[!DNL Adobe Target] now provides an MCP server that surfaces experimentation, personalization, and recommendations operations directly inside any MCP-compatible application. [!DNL Adobe Target] acts as the decisioning and execution layer while the AI assistant handles reasoning and explanation — giving teams faster access to optimization insights without navigating multiple product screens or writing queries against the [!DNL Adobe Target] REST API.

## Key capabilities {#mcp-capabilities}

The [!DNL Adobe Target] MCP server provides both read and write access to activities, audiences, offers, recommendations, and implementation configuration. With the integration, you can:

* **Inspect and audit experiments** - Get status, performance, change history, and QA preview links for any activity without navigating the UI.
* **Analyze results** - Retrieve performance, revenue, and A4T reports for A/B, XT, AP, and Auto-Target activities.
* **Manage activities** - Create, update, and activate A/B and XT activities; adjust traffic splits, variants, schedules, and priorities.
* **Manage audiences and offers** - List, inspect, and create audiences, HTML offers, and JSON offers.
* **Explore Recommendations criteria** - List and inspect criteria and cart-based algorithms.
* **Audit implementation** - Review at.js settings, response tokens, and per-entity revision history.

>[!NOTE]
>
>Write operations (create, update, activate, deactivate) include safety annotations. No changes are executed without explicit user confirmation.

## Available tools {#mcp-tools}

The [!DNL Adobe Target] MCP server exposes 52 tools. Read tools are available to all connected users with View permissions; write tools require Editor or Approver role.

### Activity tools - read

| Tool | Description |
|---|---|
| `list_target_activities` | List activities with server-side filtering by state, type, name, date, priority, mbox, and workspace |
| `list_all_target_activities` | Fetch all activities matching filters, auto-paginating through results |
| `get_ab_activity` | Get full details of a specific A/B activity |
| `get_xt_activity` | Get full details of a specific Experience Targeting (XT) activity |
| `get_abt_activity` | Get full details of a specific Automated Personalization (AP) activity |

### Activity tools - write

| Tool | Description |
|---|---|
| `create_ab_activity` | Create a new A/B test activity |
| `create_xt_activity` | Create a new Experience Targeting (XT) activity |
| `create_activity_from_modifications` | Create an XT activity from JavaScript modifications |
| `update_ab_activity` | Update an existing A/B activity |
| `update_xt_activity` | Update an existing XT activity |
| `update_abt_activity` | Update an existing Automated Personalization activity |
| `update_activity_state` | Activate, deactivate, pause, or archive an activity |
| `update_activity_schedule` | Update start and end dates for an activity |
| `update_activity_priority` | Update the priority of an activity |
| `update_activity_name` | Rename an activity |
| `add_activity_variant` | Add a new variant (experience) to an activity |
| `update_traffic_split` | Update traffic allocation across variants |
| `update_variant_offer` | Change the offer or VEC modifications for a variant |
| `remove_activity_variant` | Remove a variant from an activity |

### Offer tools

| Tool | Description |
|---|---|
| `list_target_offers` | List offers with server-side filtering and sorting |
| `list_all_target_offers` | Fetch all offers matching filters, auto-paginating |
| `get_target_offer` | Get details of a specific offer |
| `create_target_offer` | Create a new HTML offer |
| `create_target_json_offer` | Create a new JSON offer |
| `update_target_offer` | Update an existing HTML offer |

### Audience tools

| Tool | Description |
|---|---|
| `list_target_audiences` | List audiences with server-side filtering and sorting |
| `create_target_audience` | Create an audience with optional targeting rules |

### Mbox and location tools

| Tool | Description |
|---|---|
| `list_target_mboxes` | List mboxes with filtering and sorting |
| `list_all_target_mboxes` | Fetch all mboxes matching filters, auto-paginating |
| `get_target_mbox` | Get details of a specific mbox by name |
| `list_target_mbox_profile_attributes` | List all profile attributes associated with mboxes |

### Properties

| Tool | Description |
|---|---|
| `list_target_properties` | List all Target properties |

### Reporting and insights tools

| Tool | Description |
|---|---|
| `get_ab_performance_report` | Get performance report for an A/B, Auto-Allocate, or Auto-Target activity |
| `get_ab_orders_report` | Get orders and revenue report for an A/B or Auto-Target activity |
| `get_xt_performance_report` | Get performance report for an XT activity |
| `get_xt_orders_report` | Get orders and revenue report for an XT activity |
| `get_apt_performance_report` | Get performance report for an AP or Auto-Target activity |
| `get_activity_insights` | Search for an activity by name and get detailed performance insights |
| `get_a4t_report` | Get Analytics for Target (A4T) report for an activity |

### Recommendations tools

| Tool | Description |
|---|---|
| `list_target_criteria` | List all Recommendations criteria |
| `get_target_criteria` | Get details of a specific Recommendations criteria |
| `update_target_criteria_cart` | Update a Recommendations Cart-based criteria |

### Implementation and configuration tools

| Tool | Description |
|---|---|
| `get_atjs_settings` | Get AT.js settings and configuration |
| `get_atjs_versions` | Get available AT.js versions |
| `list_target_response_tokens` | List all response tokens in your Target tenant |
| `create_target_response_token` | Create a new custom response token |

### Audit and revision tools

| Tool | Description |
|---|---|
| `get_target_revisions` | Get audit log for a resource type, filtered by author |
| `get_target_entity_revisions` | Get all revisions of a specific entity by ID |

### Utilities

| Tool | Description |
|---|---|
| `preview_activity` | Generate QA preview URLs for a Target activity |
| `create_page_delivery_segment` | Create a page delivery segment for VEC activity targeting |
| `list_target_templates` | List available MCP resources and templates |
| `debug_token_info` | Inspect the current OAuth token scopes and claims |

## Use cases {#mcp-use-cases}

The following examples show how to interact with the [!DNL Adobe Target] MCP server using natural language:

| Goal | Example prompt |
|---|---|
| **Experiment status audit** | "What A/B tests are currently active on the homepage? Show me status, traffic allocation, and how long each has been running." |
| **Performance review** | "Show me all active tests that have reached statistical significance — which experiences are winning?" |
| **Revenue analysis** | "Get the orders and revenue report for activity AT4821 and summarize which experience is driving the most revenue per visitor." |
| **A4T reporting** | "Pull the A4T report for my checkout optimization test and summarize the Analytics-side conversion data." |
| **Activity management** | "Pause activity 98765 and update the priority of activity 11111 to 200." |
| **Activity insights** | "Get insights for my 'Summer Sale Banner' test — what does performance look like and are there any anomalies?" |
| **Audience management** | "List all audiences targeting mobile users and show me which activities they're associated with." |
| **QA and preview** | "Generate QA preview URLs for activity 12345 so I can review all variants before activating." |
| **Recommendations review** | "List all Recommendations criteria configured in this account and summarize the algorithm types in use." |
| **Implementation audit** | "What version of at.js is configured, and what response tokens are currently active?" |
| **Change audit** | "Show me all changes made to activity 98765 in the last 30 days and who made them." |

## Prerequisites {#mcp-prerequisites}

Before connecting the [!DNL Adobe Target] MCP server to your MCP client, ensure the following:

* You have an active [!DNL Adobe Target] license (Adobe Experience Cloud subscription) with an Adobe Experience Platform organization.
* You have a supported MCP-compatible application (currently Claude Web, Claude Desktop, or Claude Code).
* You have [!DNL Adobe Target] permissions configured in Adobe Admin Console:
  * **Observer** role: read-only tools
  * **Editor** role: read + create tools
  * **Approver** role: read + create + activate/deactivate tools

## Connect the [!DNL Adobe Target] MCP server {#mcp-connect}

>[!NOTE]
>
>The MCP server URL is `https://targetmcp.adobe.io/mcp`. Authentication uses OAuth 2.0 with dynamic client registration and PKCE — no static credentials are required.

**To connect from Claude Desktop or Claude Web:**

1. Open your MCP client settings and add a new MCP server.
2. Enter the server URL: `https://targetmcp.adobe.io/mcp`
3. When prompted, complete the Adobe IMS OAuth login with your Adobe Experience Cloud credentials.
4. Once authenticated, all tools are immediately available. Try "List all active Target activities" to verify the connection.

**To connect from Claude Code:**

Add the following to your Claude Code MCP configuration:

```json
{
  "mcpServers": {
    "adobe-target": {
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

Complete the OAuth browser flow when prompted on first use.

## Frequently asked questions {#mcp-faq}

+++Which MCP clients are supported?

The [!DNL Adobe Target] MCP server is currently available for **Claude Web**, **Claude Desktop**, and **Claude Code**. Support for additional MCP-compatible applications may be added in future releases.
+++

+++What [!DNL Adobe Target] objects can I access via MCP?

You can access activities (A/B, XT, AP), audiences, offers, properties, mboxes, Recommendations criteria, response tokens, at.js configuration, A4T reports, and entity revision history. Read and write operations are both supported across 52 tools — write operations require the appropriate role and explicit confirmation.
+++

+++Do I need developer access to use the MCP server?

No. The MCP server is designed for both marketing and technical personas. Marketers can interact with it using natural language prompts in any supported MCP client, while developers can use it in tools like Claude Code or Cursor.
+++

+++Is my [!DNL Adobe Target] data sent to the MCP client provider?

When you submit a prompt, the MCP client may send relevant context (including [!DNL Adobe Target] data returned by the MCP server) to its model for processing. Review the privacy and data-handling policies of your MCP client provider before connecting to production data. Adobe's data handling is governed by the [Adobe Privacy Policy](https://www.adobe.com/privacy.html) and [Data Protection Terms](https://www.adobe.com/go/dpt-ww).
+++

+++Can write operations cause unintended changes to live activities?

Write tools include safety annotations and confirmation gates. Before any state-changing action — such as activating an activity, changing priority, or updating ML model configuration — the server presents a structured confirmation showing the affected object, estimated traffic impact, and a required explicit approval step. No changes are made until confirmed.
+++

+++What permissions do I need in [!DNL Adobe Target]?

At minimum, **Observer** role grants access to all read tools. **Editor** role enables creating activities, audiences, and offers. **Approver** role is required to activate, deactivate, or archive activities. Contact your [!DNL Adobe Target] administrator if you are unsure about your current access level.
+++

+++Can I use the MCP server across multiple Target organizations or properties?

The MCP server scopes operations to the organization associated with your authenticated Adobe IMS credentials. If you have access to multiple properties within that organization, you can query by property using the `list_target_properties` tool and filter subsequent requests accordingly.
+++
