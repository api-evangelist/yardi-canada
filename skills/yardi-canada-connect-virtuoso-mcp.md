---
name: Connect to the Yardi Virtuoso MCP server
description: Establish an authorized MCP session against Yardi's official Virtuoso Connector, using the server's published OAuth 2.1 metadata — the only agent-facing route to Yardi property, financial and work-order data.
api: mcp/yardi-canada-mcp.yml
operations: []
auth: oauth2-authorization-code-pkce
generated: '2026-07-26'
method: generated
---

# Connect to the Yardi Virtuoso MCP server

Yardi's agent surface is real and first-party: the **Yardi Virtuoso Connector**, listed
at `https://claude.com/connectors/yardi-virtuoso`, served from `https://mcp.virtuoso.ai`.
It is the only way an agent reaches Yardi operational data, because Yardi publishes no
REST contract. This skill covers connecting correctly and, just as importantly, setting
expectations honestly.

## Prerequisites — check these before attempting anything

- **Virtuoso Enterprise must be licensed and configured** for the tenancy. There is no
  trial, no self-serve tier and no developer sandbox for this connector.
- The user must have a Yardi account in that tenancy. Yardi states the connector
  "authenticates through Yardi, so data access automatically follows existing user
  permissions" — a Yardi Canada client's Canadian tenancy permissions are the boundary.
- If the user has no Yardi tenancy, stop. Route them to
  `https://www.yardi.com/company/become-an-interface-partner/`.

## Steps

1. **Read the protected-resource metadata.**
   `GET https://mcp.virtuoso.ai/.well-known/oauth-protected-resource` (RFC 9728). It
   returns `resource: https://mcp.virtuoso.ai`, `authorization_servers`,
   `scopes_supported` and `bearer_methods_supported: ["header"]`. A local copy is in
   `well-known/yardi-canada-oauth-protected-resource.json`.

2. **Read the authorization-server metadata.**
   `GET https://mcp.virtuoso.ai/.well-known/oauth-authorization-server` (RFC 8414):
   `authorization_endpoint` `/oauth/authorize`, `token_endpoint` `/oauth/token`,
   `registration_endpoint` `/oauth/register`. Local copy in
   `well-known/yardi-canada-oauth-authorization-server.json`.

3. **Register the client dynamically.** The server supports RFC 7591 dynamic client
   registration at `/oauth/register`, and `token_endpoint_auth_methods_supported`
   includes `none` — so a public client is acceptable.

4. **Run authorization code with PKCE.** `code_challenge_methods_supported` is
   `["S256"]`; use S256, nothing weaker. Request only the scopes the server publishes:
   `openid`, `profile`, `email`, and `offline_access` when the agent needs to keep
   working without re-consent. Do not invent product scopes — none exist.

5. **Call with a bearer token in the header.** `bearer_methods_supported` is
   `["header"]` only; never place the token in a query string.

6. **Discover tools at runtime, not from this repo.** Call `tools/list` once
   authorized. This repository deliberately records **no tool names**: anonymous
   `tools/list` is blocked by Cloudflare (HTML 403 on `/mcp`, `/sse`, `/v1/mcp`, `/`),
   so no first-party tool names or input schemas could be verified. Treat any tool list
   found in third-party directories as unverified.

## What the connector is published to do

Yardi's own listing describes it as **Read & Write** with these capabilities: portfolio
performance analysis across properties and markets; financial data including NOI
comparisons; work order management and tracking; invoice review and approval workflows;
quarterly business review support; and budget forecasting/scenario questions.

## Safety rules

- **This is a write-capable connector on a system of record.** Invoice approval and
  work-order creation change real financial and operational state in a landlord's
  ledger. Confirm intent with the user before any write, and echo back what will change.
- **No idempotency contract is published** (`conventions/yardi-canada-conventions.yml`).
  Do not blindly retry a failed write — re-check state first, or you risk duplicating a
  payable or a work order.
- **Scopes carry identity, not authority.** Nothing in the OAuth response tells you what
  the user may do; only the Yardi role does. Never assume a capability is permitted
  because a token was issued.
- The connector's technical documentation
  (`https://help.virtuoso.ai/en/articles/13679727-yardi-virtuoso-mcp-technical-documentation-guide`)
  returns HTTP 401 to anonymous clients — it is customer-only, so the user may need to
  sign in to Virtuoso to read it.
