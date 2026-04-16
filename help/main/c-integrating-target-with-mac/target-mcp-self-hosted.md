---
solution: Target
product: target
title: Self-host the Adobe Target MCP server
description: Learn how to run your own instance of the Adobe Target MCP server using Python, Docker, or a local development environment.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer
level: Experienced
hide: true
---
# Self-host the [!DNL Adobe Target] MCP server {#target-mcp-self-hosted}

>[!BEGINSHADEBOX]

Table of contents:

* [Work with MCP clients](target-mcp.md)
* [MCP server tools reference](target-mcp-tools-reference.md)
* **[Self-host the MCP server](target-mcp-self-hosted.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Self-hosted deployment is intended for developers and advanced users who need full control over the [!DNL Adobe Target] MCP server runtime. For most users, the hosted endpoint (`https://targetmcp.adobe.io/mcp`) is recommended. See [Work with MCP clients](target-mcp.md).

This page explains how to clone, configure, and run your own instance of the [!DNL Adobe Target] MCP server. Self-hosting is useful when you need a local development environment, custom network configuration, or want to contribute to the server codebase.

## Prerequisites {#self-hosted-prereqs}

Before you begin, ensure you have the following:

* **Python 3.13 or later**
* **[uv](https://github.com/astral-sh/uv){target="_blank"}** — fast Python package and project manager

  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

* An active [!DNL Adobe Target] license with Adobe Experience Cloud access
* **Artifactory credentials** (Adobe internal users only) — required to install internal dependencies

## Installation {#self-hosted-install}

**1. Clone the repository:**

```bash
git clone https://github.com/Adobe-TnT/target-mcp.git
cd target-mcp
```

**2. Create and activate a virtual environment:**

```bash
uv venv --python 3.13
source .venv/bin/activate
```

**3. Configure environment variables:**

```bash
cp env.example .env
```

Open `.env` and replace the placeholder values with your credentials and organization settings.

**4. Install dependencies:**

```bash
make uv-install
```

**5. Start the server:**

Choose the mode that matches your use case:

| Mode | Command | Use when |
|---|---|---|
| StreamableHTTP (API server) | `make run-api-server` | Connecting an MCP client over HTTP |
| STDIO (local MCP client) | `make run-mcp-stdio` | Using direct process communication |

## Connect an MCP client to a local server {#self-hosted-connect}

### Cursor

Add the following to your Cursor MCP configuration. Replace the placeholder values with your actual IMS token and organization ID:

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp",
      "headers": {
        "Authorization": "Bearer {IMS_USER_TOKEN}",
        "x-gw-ims-org-id": "{IMS_ORGANIZATION_ID}"
      }
    }
  }
}
```

### Claude Code

Add an entry to your Claude Code MCP configuration file pointing to the local server:

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp"
    }
  }
}
```

>[!NOTE]
>
>When connecting to a local server, authentication headers must be passed manually (as shown in the Cursor example above). The OAuth browser flow is only available with the hosted `https://targetmcp.adobe.io/mcp` endpoint.

## Docker deployment {#self-hosted-docker}

The repository includes a Docker Compose configuration for containerized deployments.

**Run with Docker Compose:**

```bash
make run-dc
```

**Build and run the Docker image directly:**

```bash
make build
make run-docker
```

## API endpoints {#self-hosted-endpoints}

The self-hosted server exposes the following HTTP endpoints:

| Endpoint | Description |
|---|---|
| `/mcp` | MCP protocol endpoint for AI clients |
| `/ping` | Liveness check — returns `"Pong"` |
| `/health` | Health check — returns `{"status": "healthy"}` |
| `/validate` | Input validation endpoint |
| `/authorize` | OAuth authorization endpoint |
| `/token` | OAuth token endpoint |

**Health check example:**

```bash
curl http://localhost:8080/health
# Response: {"status": "healthy"}
```

## Troubleshooting {#self-hosted-troubleshoot}

+++Server fails to start

1. Verify Python 3.13+ is installed: `python --version`
1. Confirm the virtual environment is activated: `source .venv/bin/activate`
1. Check that all environment variables in `.env` are set correctly.
1. Run `make uv-install` again to ensure all dependencies are present.

+++

+++Cannot connect from MCP client

1. Confirm the server is running and the port is accessible: `curl http://localhost:8080/ping`
1. Verify the server URL in your MCP client configuration matches the running server address.
1. For Cursor, ensure the `Authorization` header contains a valid, non-expired IMS token.

+++

+++Dependency installation fails (Adobe internal users)

1. Confirm your Artifactory credentials are configured correctly.
1. Check your network connection to the internal Artifactory instance.
1. Contact your team's DevOps or platform engineering contact for Artifactory access.

+++

## Related resources {#self-hosted-related}

* [Work with MCP clients](target-mcp.md) — hosted endpoint setup and tool reference
* [Model Context Protocol documentation](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Admin API reference](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
