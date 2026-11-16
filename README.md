# Nominal Schemas & Public Agent Integrations

Public JSON Schemas and agent connection manifests for [Nominal Lighting](https://nominal.lighting). This repository does not contain the Nominal application, private user bundles, or production credentials.

## Live NOMF JSON Schema

- **Current NOMF v0.3:** [Live JSON Schema](https://nominal.lighting/schemas/nomf/v0.3.json)
- **Current GitHub source:** [nomf_family_template_v0.3.json](nomf_family_template_v0.3.json)
- **Legacy v0.2:** [nomf_family_template_v0.2.json](nomf_family_template_v0.2.json), retained for compatibility
- **REST:** `GET https://nominal.lighting/api/v1/schema`
- **Public MCP:** `get_nomf_schema` (tool) or `nominal://schema/nomf/v0.3` (resource)

The Nominal endpoints fetch the current v0.3 schema from this repository's **main** branch on every request rather than serving a deployed copy. Changes to the GitHub file are available to agents without rebuilding the website. If the source is unavailable, the endpoints return an error rather than silently serving an older schema.

When authoring or submitting a complete NOMF, agents should fetch the live schema for that task. Do not rely on a copied template stored in an installed skill.

## Nominal agent connections

- **Shared fixture-bundle link:** `https://nominal.lighting/b/CODE`
- **Public remote MCP connector:** `https://nominal.lighting/mcp/public`
- **OpenAPI:** [Nominal Agent API](https://nominal.lighting/openapi.json)
- **Connection guide:** [Claude and ChatGPT setup](https://nominal.lighting/connect)
- **Public plugin:** [Nominal Lighting](plugins/nominal/README.md)
- **MCP Registry metadata:** [server.json](server.json)

### Claude

In Claude, choose **Customize → Connectors → Add custom connector**, enter `https://nominal.lighting/mcp/public`, and choose **No sign in** if offered. Review and enable the connection. Claude Code can use the marketplace manifest at [.claude-plugin/marketplace.json](.claude-plugin/marketplace.json).

### Other agents

The same public connector and read-only REST schema URL work with clients that support MCP or HTTP. Product research and contributed technical findings require manufacturer evidence and remain subject to Nominal's review rules; public bundle publishing requires user authorization. A public shared code provides read access only, not ownership.

Installing an agent skill does not itself install or authorize the remote MCP connection.
