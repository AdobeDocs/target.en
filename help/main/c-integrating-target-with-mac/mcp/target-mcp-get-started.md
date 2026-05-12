---
solution: Target
product: target
title: Get started with the Adobe Target MCP server
description: Learn how to connect the Adobe Target MCP server to your AI assistant, including prerequisites, client configuration, and troubleshooting.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
---
# Get started with the [!DNL Adobe Target] MCP server {#target-mcp-get-started}

>[!AVAILABILITY]
>
>The [!DNL Adobe Target] MCP server is available to all customers in **Public Beta**. It is currently supported in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor**, and **ChatGPT**.

This page walks you through everything you need to connect the [!DNL Adobe Target] MCP server to your AI assistant and verify your setup.

>[!IMPORTANT]
>
>The Model Context Protocol (MCP) is an emerging open-source standard and may present security or reliability risks. Adobe MCP server integrations and related documentation are provided "as is," without warranties of any kind.
>
>Connecting MCP clients or servers to Adobe products is a customer-elected configuration, and customers are responsible for evaluating the security and suitability of any MCP integration. Adobe is not responsible for issues arising from misconfiguration, misuse of the MCP, vulnerabilities in third-party implementations, or unintended actions performed through MCP-enabled workflows.
>
>To reduce risk, Adobe encourages testing integrations in a sandbox environment prior to productive use and carefully reviewing and validating all MCP-initiated actions and responses before confirming or relying on them.

## Prerequisites {#mcp-prerequisites}

Before connecting the [!DNL Adobe Target] MCP server to your MCP client, ensure the following:

* You have an active [!DNL Adobe Target] license (Adobe Experience Cloud subscription) with an Adobe Experience Platform organization.
* You have a supported MCP-compatible application (currently Claude Web, Claude Desktop, Claude Code, Cursor, or ChatGPT).
* You have [!DNL Adobe Target] permissions configured in Adobe Admin Console:
  * **Observer** role: read-only tools
  * **Editor** role: read + create tools
  * **Approver** role: read + create + activate/deactivate tools

## Connect the [!DNL Adobe Target] MCP server {#mcp-connect}

>[!NOTE]
>
>The [!DNL Adobe Target] MCP server uses OAuth 2.0 for authentication. When you first use a Target MCP tool, you are redirected to Adobe Experience Cloud to log in, select your organization, and grant the requested permissions. No static credentials are required.

**To connect from Claude Desktop or Claude Web:**

1. Open your MCP client settings and add a new MCP server.
1. Enter the server URL: `https://targetmcp.adobe.io/mcp`
1. When prompted, complete the Adobe IMS OAuth login with your Adobe Experience Cloud credentials.
1. Once authenticated, all tools are immediately available. Try "List all active Target activities" to verify the connection.

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

**To connect from Cursor:**

1. Open **Cursor** and navigate to **Settings** → **MCP** → **Add New Global MCP Server**.
1. Add the following configuration:

```json
{
  "mcpServers": {
    "target": {
      "type": "streamable-http",
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

1. Save the configuration. The [!DNL Target] MCP server will appear in your available MCP servers.

>[!TIP]
>
>If activities or data from the wrong organization appear, log out of Adobe Experience Cloud completely, reconnect the MCP server, and carefully select the correct organization during re-authentication.

## Troubleshooting {#mcp-troubleshooting}

+++OAuth flow fails or redirects incorrectly

1. Log out of Adobe Experience Cloud completely.
1. Clear browser cookies for adobe.com domains.
1. Retry the authentication flow.
1. Ensure you select the correct organization when prompted.
+++

+++Activities or data from the wrong organization appear

1. Log out of Adobe Experience Cloud completely.
1. Disconnect and reconnect the MCP server in your client settings.
1. Select the correct organization carefully during re-authentication.
+++

+++A tool returns an error message

1. Verify you have the required permissions in [!DNL Adobe Target] for the operation (see [Prerequisites](#mcp-prerequisites)).
1. Check that the referenced resources — activities, offers, audiences — exist in your organization.
1. Confirm that activity IDs and other identifiers are correct.
+++

+++Cannot connect to the MCP server

1. Verify your internet connection.
1. Check that the MCP server URL is entered correctly in your client configuration.
1. Try removing and re-adding the server in your MCP client settings.
+++

## Security and permissions {#mcp-security}

The [!DNL Adobe Target] MCP server can only access data that your Adobe user account has permission to view or modify. All operations respect your [!DNL Target] role assignments and workspace permissions.

The server requests the following OAuth scopes:

* `AdobeID` — Basic Adobe identity
* `openid` — OpenID Connect authentication
* `additional_info.projectedProductContext` — Tenant discovery
* `read_organizations` — Organization-level operations
* `additional_info.roles` — Role-based access control

OAuth tokens are validated against Adobe IMS on each request, are not stored persistently by the MCP server, and all communication uses HTTPS.

## Related resources {#mcp-get-started-related}

* [Overview](target-mcp.md)
* [Use cases and walkthroughs](target-mcp-use-cases.md)
* [MCP server tools reference](target-mcp-tools-reference.md)
* [Model Context Protocol documentation](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Admin API reference](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
