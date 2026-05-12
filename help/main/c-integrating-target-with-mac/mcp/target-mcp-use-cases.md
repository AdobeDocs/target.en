---
solution: Target
product: target
title: Adobe Target MCP server — use cases and walkthroughs
description: Explore common use cases and step-by-step prompt walkthroughs for the Adobe Target MCP server.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
---
# [!DNL Adobe Target] MCP server — use cases and walkthroughs {#target-mcp-use-cases}


>[!AVAILABILITY]
>
>The [!DNL Adobe Target] MCP server is available to all customers in **Public Beta**. It is currently supported in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor**, and **ChatGPT**.


This page shows you what you can accomplish with the [!DNL Adobe Target] MCP server using natural-language prompts, from quick lookups to multi-step activity management tasks.

>[!IMPORTANT]
>
>The Model Context Protocol (MCP) is an emerging open-source standard and may present security or reliability risks. Adobe MCP server integrations and related documentation are provided "as is," without warranties of any kind.
>
>Connecting MCP clients or servers to Adobe products is a customer-elected configuration, and customers are responsible for evaluating the security and suitability of any MCP integration. Adobe is not responsible for issues arising from misconfiguration, misuse of the MCP, vulnerabilities in third-party implementations, or unintended actions performed through MCP-enabled workflows.
>
>To reduce risk, Adobe encourages testing integrations in a sandbox environment prior to productive use and carefully reviewing and validating all MCP-initiated actions and responses before confirming or relying on them.

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

## Use case walkthroughs {#mcp-use-case-walkthroughs}

The following walkthroughs show how to complete common tasks using natural-language prompts with the [!DNL Adobe Target] MCP server.

+++Creating an A/B test

**Prompt:**
"Create an A/B test called 'Homepage Hero Image Test' with two experiences: 'Control' showing the current hero and 'Variant' showing a new summer-themed hero image. Target the homepage mbox."

The AI assistant uses the `create_ab_activity` tool to create the activity with the configuration you described. The tool returns the new activity ID and a confirmation of the created experiences.

+++

+++Checking activity performance

**Prompt:**
"Show me the performance metrics for my 'Checkout Flow Optimization' activity over the last 30 days."

The AI assistant uses `get_ab_performance_report` or `get_xt_performance_report` (depending on activity type) to retrieve conversion rates, visitor counts, and other metrics for the specified time window.

+++

+++Managing offers

**Prompt:**
"Create an HTML offer called 'Summer Sale Banner' with a promotional banner that says '20% off all summer items'."

The AI assistant uses the `create_target_offer` tool to create the offer with your specified HTML content and returns a confirmation with the new offer ID.

+++

+++Building an audience

**Prompt:**
"Create an audience called 'Mobile Visitors from California' that targets users on mobile devices located in California."

The AI assistant uses the `create_target_audience` tool with the appropriate targeting rules derived from your description.

+++

+++Generating QA preview links

**Prompt:**
"Generate preview URLs for activity 12345 so I can test each experience."

The AI assistant uses the `preview_activity` tool to generate clickable URLs that bypass audience targeting, letting you view each experience directly in your browser.

+++

+++Creating an Experience Targeting activity

**Prompt:**
"Create an Experience Targeting activity called 'Geo Personalization' that shows different hero banners to visitors from different regions."

The AI assistant uses `create_xt_activity` to build the activity with audience-based experience mapping according to the regions you describe.

+++

+++Scheduling an activity

**Prompt:**
"Update the schedule for activity 12345 to start on May 1st and end on May 31st."

The AI assistant uses the `update_activity_schedule` tool to apply the new start and end dates to the activity.

+++

## Related resources {#mcp-use-cases-related}

* [Overview](target-mcp.md)
* [Get started](target-mcp-get-started.md)
* [MCP server tools reference](target-mcp-tools-reference.md)
* [Model Context Protocol documentation](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Admin API reference](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
