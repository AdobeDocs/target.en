---
keywords: Adobe Target;Coworker;AI;skills;experimentation;Recommendations
title: Coworker skills for Adobe Target
description: Learn about the Coworker skills available for Adobe Target, including activity discovery, test creation, analysis, audience composition, and Recommendations troubleshooting.
feature: Overview
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
---

# Coworker skills for Adobe Target {#coworker-skills}

>[!BEGINSHADEBOX]

**On this page:** Discover the Coworker skills available for Adobe Target, including skills for exploring activities and audiences, creating and configuring tests, analyzing performance, composing audiences, and managing Recommendations.

>[!ENDSHADEBOX]

Coworker skills help Adobe Target practitioners use natural language to explore their testing and personalization programs, create and configure activities, analyze results, and resolve delivery issues. Describe what you want to do in Coworker Chat, then review the returned recommendations, configuration, or analysis before taking action.

[!DNL Adobe Target] MCP tools and Coworker are documented separately and provide different capabilities:

* [Target MCP](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md) documents the individual tools exposed by the direct MCP server, including their supported activity types, parameters, permissions, and read or write scope. 
* [Coworker](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/overview#target-activities-and-audiences) provides a separate natural-language orchestration layer that can combine capabilities and apply additional workflows.

The following table is a high-level comparison of related capabilities.

| Capability | Target MCP | Coworker |
| --- | --- | --- |
| List running experiments, audiences, offers, or recently changed items | Yes | Yes |
| Create an Automated Personalization activity | No | No |
| Create a Target audience | Yes | Yes |
| Create a Target VEC activity, Experience Targeting activity, or A/B test | Yes | Yes |
| Create a Target Recommendations activity | Yes | Yes |
| Create an HTML or JSON offer in Target | Yes | Yes |
| Use an AEM Content Fragment in a Target activity | No | Yes |
| Recommend what is working and what to test next | No or generic advice | Yes |


## Target plugin

The following skills are available under the **Target** plugin:

* **Target Browse**

  Provides read-only discovery, inspection, and counting of Target entities, including activities, audiences, offers, and related configuration.

    >[!BEGINSHADEBOX]
    
    *Example prompts:*
    
    * "List my active activities."
    * "How many activities are currently running?"
    * "Show me the audiences and offers used by this activity."
    
    >[!ENDSHADEBOX]

* **Target Activity Verdict**

  Determines whether an activity is ready to ship, should wait for more data, should stop, or needs a fix, using significance calculations and configuration checks.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Should I ship this test?"
  * "Is this activity ready to stop?"
  * "Does the current activity configuration have any issues?"
    
  >[!ENDSHADEBOX]

* **Target Design**

  Creates and configures activities and offers, generates QA URLs, and authors or optimizes offer content.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Create an A/B test for the homepage."
  * "Create an offer for the returning visitor experience."
  * "Generate a QA URL for this activity."
    
  >[!ENDSHADEBOX]

* **Target VEC**

  Creates and edits Visual Experience Composer activities and their page-delivery audiences.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Create a VEC A/B test for the homepage."
  * "Edit the hero headline in my VEC activity."
  * "Create a page-delivery audience for this VEC activity."
    
  >[!ENDSHADEBOX]

* **Target Setup**

  Guides complete A/B, Experience Targeting, or Visual Experience Composer activity creation, including prerequisites, scheduling, QA, and activation.

    >[!BEGINSHADEBOX]
    
    *Example prompts:*
    
    * "Help me create my first test."
    * "What do I need before I create an Experience Targeting activity?"
    * "Walk me through scheduling, QA, and activating this activity."
    
    >[!ENDSHADEBOX]

* **Target Intelligence**

  Audits Target programs for risks, collisions, misconfigurations, hygiene issues, and quick wins.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Audit my Target activities."
  * "Find collisions or configuration risks across my activities."
  * "What quick wins can improve the hygiene of my Target program?"
    
  >[!ENDSHADEBOX]

* **Target Strategist**

  Analyzes historical Target data for winning patterns and recommends future tests.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "What should I test next based on past results?"
  * "What patterns appear in my highest-performing tests?"
  * "Recommend a follow-up test based on this activity's results."
    
  >[!ENDSHADEBOX]

* **Target Test Calculator**

  Plans A/B/n sample size, duration, and detectable lift for conversion and revenue metrics, with Bonferroni correction for multiple comparisons.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "What sample size do I need?"
  * "How long should I run this A/B test to detect a 5% lift?"
  * "What detectable lift can I measure with this traffic?"
    
  >[!ENDSHADEBOX]

* **Target Portfolio Report**

  Provides read-only, program-wide performance rollups and activity trend and momentum analysis.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Which are my top and worst tests?"
  * "Show me performance trends across my activities."
  * "Which activities have gained or lost momentum recently?"
    
  >[!ENDSHADEBOX]

* **Target Audience Composer**

  Creates or edits Target-native audiences from natural-language descriptions or explicit rules.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Create an audience for returning mobile visitors."
  * "Edit this audience to include visitors from organic search."
  * "Create a Target audience for visitors who viewed the pricing page."
    
  >[!ENDSHADEBOX]

* **Target Recommendations**

  Manages and works with Target Recommendations activities and configurations.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Create a Recommendations activity."
  * "Show me my Recommendations activities and configurations."
  * "Update the settings for this Recommendations activity."
    
  >[!ENDSHADEBOX]

* **Target Recommendations Diagnose**

  Diagnoses Recommendations delivery, configuration, catalog, and feed issues.

  >[!BEGINSHADEBOX]
    
  *Example prompts:*
    
  * "Why aren't my recommendations appearing?"
  * "Diagnose the feed and catalog configuration for this Recommendations activity."
  * "Are delivery or configuration issues affecting my recommendations?"
    
  >[!ENDSHADEBOX]
