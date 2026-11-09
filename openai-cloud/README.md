# Cabinet-X remote MCP submission package

Uses https://cabinetx.app/api/sales-mcp with OAuth 2.0, public-client DCR and PKCE S256. The connected account selects scopes; design writes also require a human-approved selected project/design. Existing sales-only grants do not gain design access.

No local software is required. The remote integration does not send messages, sign, charge, access source code or bypass editing leases. Project/customer data returned by tools is shared with the selected AI provider; only requested sales notes and normal design changes are persisted in Cabinet-X. See https://cabinetx.app/privacy/ and https://cabinetx.app/mcp/. Support: hello@cabinetx.app.

Status: prepared for portal validation, not submitted or approved. Review-case metadata describes intended observable results; the submitted reviewer account must run these cases before review. Dedicated reviewer credentials and the required walkthrough recording must be provided privately through the portal, never in this repository. Prior project evidence includes real ChatGPT remote edits; this package still requires clean-install and platform-specific acceptance.
