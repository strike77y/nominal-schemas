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

## Claude Directory submission — full public NOMF capability

1. Continue at https://claude.ai/directory/manage, Submit new → MCP connector, using `https://nominal.lighting/mcp/public`.
2. Name: **Nominal** (directory slug: `nominal-lighting` if not yet submitted). Category: Productivity, Design or Research, as offered.
3. Description: **Nominal connects Claude to architectural lighting product catalogs, manufacturer specifications, configurable NOMF ordering data and shared fixture bundles. It can start staged NOMF knowledge records for missing products, guide evidence-based research, accept sourced additions/corrections for review, and create public fixture bundles when users approve. Claims do not automatically change canonical specifications.**
4. Public documentation: https://nominal.lighting/connect
5. Authentication: **No sign in** for the public contribution endpoint; server-side daily admission limits, source evidence requirements and protected owner review apply.
6. **Capabilities: Read and write.** Three write-capable operations: `bootstrap_nomf_product` (persistent staged record), `submit_nomf_contribution` (pending/disputed claim) and `publish_fixture_bundle` (new publicly accessible bundle). All need user authorization; publishing a new bundle is not editing an existing one.
7. **Tools: 23.** Includes product search, discovery, technical capabilities, ordering configuration, manufacturer product page inspection, bundle facts/collateral, bundle preview/publication, NOMF bootstrap, research work, pending claims/corrections and claim status.
8. **Excluded (8 owner/worker-only tools):** owner review queue, work-item resolution, source verification/attestation, owner review and NOMF compilation preview/publish/rollback. The public connector never approves or publishes an external contribution to the canonical catalog.
9. Test in actual Claude with bundle `7QY7IF`, plus a **user-authorized** sandbox product bootstrapping and cited contribution. Do not submit fabricated evidence or perform live writes just to make a test pass. Ensure data-handling answers reflect stored contributions and publication.
10. Before final review, confirm public privacy policy, real support contact, branding/icon, and accurate content moderation/data policies. Do not claim those prerequisites are complete until verified.

### Review note

The directory wizard may still display the former 10 read-only tools until it refreshes the connection. Do not submit with an incorrect Read only classification. Reconnect or return to the connector setup and re-add the same URL if necessary.

