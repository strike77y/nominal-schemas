# Nominal Schemas & Public Agent Integrations

This public repository holds [Nominal](https://nominal.lighting) lighting data schemas and public connection manifests. The Nominal web application, user collections, production code, and private credentials remain in separate private repositories.

## Nominal Lighting agent connection

**Ordinary fixture-bundle link:** \`https://nominal.lighting/b/7QY7IF\` (a real example collection)

**Remote MCP connector:** \`https://nominal.lighting/mcp/public\`

**Public plugin package and installation instructions:** [Nominal Lighting plugin](plugins/nominal/README.md)

The connector exposes product discovery, evidence-backed NOMF configuration, individual fixture facts and asset links, collection preview, and controlled creation of new public bundles. A read-only shared bundle code never grants edit access.

### Claude

Use **Customize → Connectors → Add → Custom → Web** (wording varies by client), name it "Nominal", enter \`https://nominal.lighting/mcp/public\`, and choose **No sign in** if offered. Approve and enable the connector in the conversation. If the site cannot be fetched, this integration is the alternative—not a second type of bundle link.

For Claude Code plugin marketplace installation, this repository has [.claude-plugin/marketplace.json](.claude-plugin/marketplace.json) and a full plugin at [plugins/nominal](plugins/nominal). That is separate from publication in the Claude-wide directory.

### Other agents

The same server is described by an [official MCP registry server.json](server.json), ready to publish after GitHub namespace authentication, and by [the Nominal OpenAPI document](https://nominal.lighting/openapi.json).

**Important:** Putting a plugin in a public repository does not automatically install it, force Claude to recognize a URL, or grant it network access. Inclusion in Claude's directory requires a separate submission and approval at https://claude.ai/directory/manage . Until directory listing, users must explicitly connect the URL.

For initial Claude Directory submission, use the **read-only** `/mcp/public` endpoint; the existing advanced `/mcp` remains supported separately.
