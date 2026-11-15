# Public distribution checklist

- [x] Public GitHub plugin package: \`plugins/nominal/\`
- [x] Public Claude Code marketplace manifest: \`.claude-plugin/marketplace.json\`
- [x] Public remote MCP registry metadata: \`server.json\`
- [x] Existing live MCP endpoint: \`https://nominal.lighting/mcp/public\`
- [ ] Test actual Claude connector connection from an individual Claude account
- [ ] Submit Nominal to https://claude.ai/directory/manage as a single MCP or MCP + skill plugin
- [ ] Pass Claude directory review; get verified install/listing URL
- [ ] Publish \`server.json\` with authenticated \`mcp-publisher\` from this public repository
- [ ] Confirm public listing and an unrelated Claude account can discover Nominal by name
- [ ] Verify behavior when a fresh Claude session encounters ONLY a normal Nominal bundle URL and no connection

No user-facing "AI version" of a bundle URL or secondary sharing workflow exists. A public folder cannot override the privacy of a private GitHub repository, so this repository is the public distribution home. Public listings can improve discoverability but cannot guarantee that a disconnected model prompts installation just from seeing a URL.

## First submission: curated Claude MCP connector

1. Open https://claude.ai/directory/manage with a paid Claude account; Submit new → MCP connector.
2. Server: `https://nominal.lighting/mcp/public` (stable public read-only subset), not the full research/owner endpoint `/mcp`.
3. Display name: **Nominal Lighting**. Suggested category: **Productivity**; secondary: **Other** if needed.
4. Description: **Read lighting fixture schedules, manufacturer product identities, saved configurations, verified technical facts, and linked specification, photometry and Revit files directly from shared Nominal bundles.**
5. Public documentation: https://nominal.lighting/connect
6. Authentication: **No sign in** for this strictly public, read-only connector.
7. Current public tools: get_bundle_outline, get_fixture_fact, get_fixture_evidence, get_fixture_assets, get_shared_bundle, search_catalog, get_product, get_product_capabilities, get_product_performance, get_product_assets.
8. Test the connector in an actual Claude chat with sample share code `7QY7IF`, including a fact that remains unavailable when not supported by NOMF. Do not declare tests completed until client access is confirmed.
9. **Missing before submission:** user-approved privacy policy URL (currently 404 on /privacy), verified support contact, logo/icon, provider/account owner information, and testing each tool. Do not invent these or claim acceptance.
10. Submit the connector; after approval, submit the plugin bundle if skills + MCP are desired. Both can coexist and be associated in Claude's directory.
