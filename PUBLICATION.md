# Public distribution checklist

- [x] Public GitHub plugin package: \`plugins/nominal/\`
- [x] Public Claude Code marketplace manifest: \`.claude-plugin/marketplace.json\`
- [x] Public remote MCP registry metadata: \`server.json\`
- [x] Existing live MCP endpoint: \`https://nominal.lighting/mcp\`
- [ ] Test actual Claude connector connection from an individual Claude account
- [ ] Submit Nominal to https://claude.ai/directory/manage as a single MCP or MCP + skill plugin
- [ ] Pass Claude directory review; get verified install/listing URL
- [ ] Publish \`server.json\` with authenticated \`mcp-publisher\` from this public repository
- [ ] Confirm public listing and an unrelated Claude account can discover Nominal by name
- [ ] Verify behavior when a fresh Claude session encounters ONLY a normal Nominal bundle URL and no connection

No user-facing "AI version" of a bundle URL or secondary sharing workflow exists. A public folder cannot override the privacy of a private GitHub repository, so this repository is the public distribution home. Public listings can improve discoverability but cannot guarantee that a disconnected model prompts installation just from seeing a URL.
