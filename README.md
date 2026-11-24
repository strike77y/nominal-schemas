# Nominal Schemas & Public Agent Integrations

Legacy schema mirror and public integration manifests for [Nominal Lighting](https://nominal.lighting). **The official NOMF schema is published on Nominal Lighting, not served from this GitHub repository.** This repository does not contain the Nominal application, private user bundles, or production credentials.

## Live NOMF JSON Schema

- **Current NOMF v0.6:** [Live JSON Schema](https://nominal.lighting/schemas/nomf/v0.6.json)
- **v0.6 GitHub mirror:** [nomf_family_template_v0.6.json](nomf_family_template_v0.6.json) (not an upstream for production)
- **Historical GitHub mirror:** [nomf_family_template_v0.3.json](nomf_family_template_v0.3.json) (not an upstream for production)
- **Legacy v0.2:** [nomf_family_template_v0.2.json](nomf_family_template_v0.2.json), retained for compatibility
- **REST:** `GET https://nominal.lighting/api/v1/schema`
- **Public MCP:** `get_nomf_schema` (tool) or `nominal://schema/nomf/v0.6` (resource)

Nominal publishes the canonical v0.6 schema as part of the deployed website. REST and MCP read the same deployment asset, with no runtime dependency on GitHub. Changes to this repository do **not** publish a new schema release. Official licensing information: https://nominal.lighting/legal/specification-license.

When authoring or submitting a complete NOMF, agents should fetch the live schema for that task. Do not rely on a copied template stored in an installed skill.

## Nominal agent connections

- **Shared fixture-bundle link:** `https://nominal.lighting/b/CODE`
- **Public remote MCP connector:** `https://nominal.lighting/mcp/public`
- **OpenAPI:** [Nominal Agent API](https://nominal.lighting/openapi.json)
- **Connection guide:** [Claude and ChatGPT setup](https://nominal.lighting/connect)
- **Public plugin:** [Nominal Lighting](plugins/nominal/README.md)
- **MCP Registry metadata:** [server.json](server.json)

### Claude

In Claude, choose **Customize → Connectors → Add custom connector**, enter `https://nominal.lighting/mcp/public`, and choose **No sign in** if offered. Review and enable the connection. Download the current Claude plugin at [Nominal Skills](https://nominal.lighting/skills). The GitHub marketplace manifest in this repository is legacy and may become inaccessible when the repository is private.

### Other agents

The same public connector and read-only REST schema URL work with clients that support MCP or HTTP. Product research and contributed technical findings require manufacturer evidence and remain subject to Nominal's review rules; public bundle publishing requires user authorization. A six-character public shared BOM code permits public reading and editing, but does not transfer ownership.

Installing an agent skill does not itself install or authorize the remote MCP connection.


## Specification licensing

NOMF v0.6 is a proprietary, Nominal-maintained specification. The official published file is at https://nominal.lighting/schemas/nomf/v0.6.json; read the [Nominal Proprietary Specification & Implementation License](https://nominal.lighting/legal/specification-license). The currently published license is NPSIL 1.0, effective November 18, 2026.
