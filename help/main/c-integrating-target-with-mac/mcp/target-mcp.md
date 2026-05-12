---
solution: Target
product: target
title: Adobe Target MCP server overview
description: Learn what the Adobe Target MCP server is, its key capabilities, and how it connects to your AI assistant.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
---
# [!DNL Adobe Target] MCP server {#target-mcp}


The [!DNL Adobe Target] MCP integration lets you inspect, analyze, and manage A/B tests, personalization activities, and Recommendations criteria directly from your AI assistant. Turn [!DNL Target]'s read and write APIs into plain-language workflows — audit your experiment portfolio, review performance reports, manage audiences and offers, and take governed actions without navigating the UI or writing API calls.

>[!AVAILABILITY]
>
>The [!DNL Adobe Target] MCP server is available to all customers in **Public Beta**. It is currently supported in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor**, and **ChatGPT**. Support for additional MCP-compatible applications will be added in future releases.


## What is the Model Context Protocol? {#mcp-overview}

Marketing and optimization teams increasingly rely on chat-based applications and developer tools — such as Anthropic Claude, OpenAI ChatGPT, Cursor, and Microsoft Copilot Studio — to streamline their day-to-day work. These applications support the **Model Context Protocol (MCP)**, an open standard that lets applications expose back-end tools to large language models (LLMs) in a uniform way.

[!DNL Adobe Target] now provides an MCP server that surfaces experimentation, personalization, and recommendations operations directly inside any MCP-compatible application. [!DNL Adobe Target] acts as the decisioning and execution layer while the AI assistant handles reasoning and explanation — giving teams faster access to optimization insights without navigating multiple product screens or writing queries against the [!DNL Adobe Target] REST API.


>[!IMPORTANT]
>
>The Model Context Protocol (MCP) is an emerging open-source standard and may present security or reliability risks. Adobe MCP server integrations and related documentation are provided "as is," without warranties of any kind.
>
>Connecting MCP clients or servers to Adobe products is a customer-elected configuration, and customers are responsible for evaluating the security and suitability of any MCP integration. Adobe is not responsible for issues arising from misconfiguration, misuse of the MCP, vulnerabilities in third-party implementations, or unintended actions performed through MCP-enabled workflows.
>
>To reduce risk, Adobe encourages testing integrations in a sandbox environment prior to productive use and carefully reviewing and validating all MCP-initiated actions and responses before confirming or relying on them.

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

The [!DNL Adobe Target] MCP server exposes 52 tools across 10 categories — from activity management and reporting to audience creation and QA previews. For the complete parameter reference, see [MCP server tools reference](target-mcp-tools-reference.md).

To explore what you can do with the [!DNL Adobe Target] MCP server — including step-by-step prompt walkthroughs — see [Use cases and walkthroughs](target-mcp-use-cases.md).

To connect the [!DNL Adobe Target] MCP server to your AI assistant — including prerequisites, client-specific configuration, and troubleshooting — see [Get started](target-mcp-get-started.md).

## Frequently asked questions {#mcp-faq}

+++Which MCP clients are supported?

The [!DNL Adobe Target] MCP server is currently available for **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor**, and **ChatGPT**. Support for additional MCP-compatible applications may be added in future releases.
+++

+++What [!DNL Adobe Target] objects can I access via MCP?

You can access activities (A/B, XT, AP), audiences, offers, properties, mboxes, Recommendations criteria, response tokens, at.js configuration, A4T reports, and entity revision history. Read and write operations are both supported across 52 tools — write operations require the appropriate role and explicit confirmation.
+++

+++Can the MCP server create or modify activities?

Yes. In addition to read operations, the server exposes write operations that let you create activities, pause them, update priorities, adjust traffic splits, and more. Write operations follow the same permission model as the [!DNL Adobe Target] UI — you need the appropriate role to make changes, and no action is executed without explicit user confirmation.
+++

+++Do I need developer access to use the MCP server?

No. The MCP server is designed for both marketing and technical personas. Marketers can interact with it using natural language prompts in any supported MCP client, while developers can use it in tools like Claude Code or Cursor.
+++

+++Is my [!DNL Adobe Target] data sent to the MCP client provider?

When you submit a prompt, the MCP client may send relevant context (including [!DNL Adobe Target] data returned by the MCP server) to its model for processing. Review the privacy and data-handling policies of your MCP client provider before connecting to production data. Adobe's data handling is governed by the [Adobe Privacy Policy](https://www.adobe.com/privacy.html) and [Data Protection Terms](https://www.adobe.com/go/dpt-ww).
+++

+++Can write operations cause unintended changes to live activities?

Write tools include safety annotations and confirmation gates. Before any state-changing action — such as activating an activity, changing priority, or updating traffic allocation — the server presents a structured confirmation showing the affected object, estimated traffic impact, and a required explicit approval step. No changes are made until confirmed.
+++

+++What permissions do I need in [!DNL Adobe Target]?

At minimum, **Observer** role grants access to all read tools. **Editor** role enables creating activities, audiences, and offers. **Approver** role is required to activate, deactivate, or archive activities. Contact your [!DNL Adobe Target] administrator if you are unsure about your current access level.
+++

+++Can I use the MCP server across multiple Target organizations or properties?

The MCP server scopes operations to the organization associated with your authenticated Adobe IMS credentials. If you have access to multiple properties within that organization, you can query by property using the `list_target_properties` tool and filter subsequent requests accordingly.
+++

## Related resources {#mcp-related}

* [Get started](target-mcp-get-started.md)
* [Use cases and walkthroughs](target-mcp-use-cases.md)
* [MCP server tools reference](target-mcp-tools-reference.md)
* [Model Context Protocol documentation](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Admin API reference](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [Cursor documentation](https://docs.cursor.com/){target="_blank"}
