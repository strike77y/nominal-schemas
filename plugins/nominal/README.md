# Nominal Lighting plugin

Public agent instructions and the [Nominal Lighting](https://nominal.lighting) remote MCP connection. This plugin contains no private application code, user collections, or credentials.

**Remote MCP:** https://nominal.lighting/mcp/public

**Live NOMF v0.3 JSON Schema:** https://nominal.lighting/schemas/nomf/v0.3.json

Agents constructing full NOMFs should call the `get_nomf_schema` tool or read `nominal://schema/nomf/v0.3` for the current schema. These retrieve the live source, not a copy packaged with the skill.

## Claude / Cowork / Claude Desktop

Choose **Customize → Connectors → Add → Custom → Web**, enter **Nominal** and `https://nominal.lighting/mcp/public`, select **No sign in** if available, review requested permissions, and enable the connector.

## Claude Code

Install from this public GitHub marketplace:

```text
/plugin marketplace add strike77y/nominal-schemas
/plugin install nominal-lighting@nominal-lighting-plugins
```

Installation requires user approval. No special AI version of a bundle link is needed.

## Technical behavior

For an existing bundle, use `get_bundle_outline` first, `get_fixture_fact` for narrow technical claims, and `get_fixture_assets` for linked documents. Leave unknown values unknown. Before generating complete NOMFs, retrieve the live schema; source-backed contributions are subject to separate verification. Publishing new bundles requires user approval; existing shared codes do not provide edit authority.
