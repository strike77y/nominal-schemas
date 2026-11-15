# Nominal Lighting plugin

Public source for the **Nominal Lighting** Claude plugin and remote MCP connector.

**MCP endpoint:** https://nominal.lighting/mcp

This plugin contains the lightweight instructions and remote MCP connection metadata, not Nominal's private application code or any user bundle data.

## Claude / Cowork / Claude Desktop

To add the public remote MCP directly, use **Customize → Connectors → Add → Custom → Web**, set the name to **Nominal**, URL to **https://nominal.lighting/mcp**, choose **No sign in** (for public access), review the requested tools, and enable it in the conversation. The client must be able to reach the endpoint from Anthropic's cloud.

To request inclusion in Claude's directory, the owner submits this plugin or the single MCP endpoint using [Claude's submission portal](https://claude.ai/directory/manage). A directory listing requires approval; the presence of this repository is **not** a listing.

## Claude Code

Install from this public GitHub marketplace:

\`\`\`text
/plugin marketplace add strike77y/nominal-schemas
/plugin install nominal-lighting@nominal-lighting-plugins
\`\`\`

A user must approve marketplace/plugin installation. No special bundle link is needed after installation.

## Registry

The public [server.json](../../server.json) is prepared for the MCP Registry. Publication requires authenticated GitHub namespace ownership, e.g. \`mcp-publisher login github\` and \`mcp-publisher publish server.json\` in this repository. No registry listing is claimed until the publish command succeeds.

## Technical behavior

Use \`get_bundle_outline\` first for a share code, \`get_fixture_fact\` for a narrow technical claim and \`get_fixture_assets\` for selected source files. Unknown values stay unknown. Publishing a new bundle requires user approval; existing shared codes do not grant editing authority.
