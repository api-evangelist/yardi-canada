# Yardi Canada

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Yardi Canada Ltd. is the Canadian subsidiary of Yardi Systems, Inc. (Goleta, California), opened in Mississauga in 1998 and now headquartered in Toronto with regional offices in Saskatoon and Vancouver and roughly 500 staff. It sells, implements and supports the Yardi property and investment management stack in Canada — Voyager, Breeze Premier, RentCafe, Home IQ, Matrix and Pulse — across residential, commercial, affordable, senior living and investment portfolios, and its Canadian footprint grew by acquisition: Point2 Technologies in Saskatoon in 2010, an EnerNOC division in Vancouver in 2016, and Planimetron in Toronto in 2022. It sits on the systems-of-record rung of the value chain rather than the listing or land-registration rung — it is the ledger and operating platform a landlord or asset manager runs on, not a portal like REALTOR.ca and not a registry operator like Teranet. Its API posture, stated honestly, is licensed-access-only and partner-gated. There is no public developer portal: developer., developers., api. and docs. hosts do not resolve on either yardi.ca or yardi.com, and the primary Canadian domain yardi.ca — registered to Yardi Systems, Inc. since 2003 — resolves to 104.156.161.80 but serves no web content at all (TCP 443 and 80 both time out). Real interfaces exist, but only behind the Interface Partnership Program: an application, a signed Data Exchange Agreement per interface type, a company at least two years old with three or more active Voyager clients, and an annual per-interface fee. RESO is absent entirely — Yardi appears nowhere in the RESO certification directory — which is the expected result for a Canadian property management vendor, because Canadian residential listings move through CREA's DDF and REALTOR.ca rather than through RESO-certified MLS endpoints. Two public, machine-readable surfaces do exist and neither of them is REST. Yardi ships a first-party MCP server — the Yardi Virtuoso Connector, listed on the Anthropic connector directory and served from mcp.virtuoso.ai — whose OAuth 2.1 authorization contract (RFC 8414 and RFC 9728 metadata, PKCE, dynamic client registration) is published anonymously even though its tool list is not. And status.yardi.com runs a full Atlassian Statuspage with a public JSON API across 134 components in 16 product groups, seven of which carry an explicit Canada component — the only anonymous, machine-readable signal of Yardi Canada's production service health.

**Areas:** Real Estate · Canada · Property Management · Rentals · Commercial Real Estate · PropTech · Multifamily · Affordable Housing · Senior Living · Investment Management · Tenancy · Payments

## Yardi Canada on APIs.io

Everything profiled for Yardi Canada is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/yardi-canada/](https://apis.io/providers/yardi-canada/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Yardi Voyager Standard Interfaces](https://apis.io/apis/yardi-canada/yardi-voyager-standard-interfaces/) — The documented family of Voyager web-service interfaces that Yardi Canada clients and their vendors integrate against — Collections, Commercial,…
- [RentCafe API](https://apis.io/apis/yardi-canada/rentcafe-api/) — The RentCafe marketing, leasing and resident-services API, used by Yardi Canada's multifamily clients and their vendors. Yardi's published RentCafe API…
- [Yardi Virtuoso Connector (MCP)](https://apis.io/apis/yardi-canada/yardi-virtuoso-connector-mcp/) — Yardi's first-party Model Context Protocol server, announced in early access on 2025-09-10 and described as available now in Virtuoso Enterprise on…
- [Yardi Canada Components API](https://apis.io/apis/yardi-canada/yardi-canada-components-api/) — Per-product and per-region service components
- [Yardi Canada Incidents API](https://apis.io/apis/yardi-canada/yardi-canada-incidents-api/) — Unplanned service incidents and their updates
- [Yardi Canada Maintenance API](https://apis.io/apis/yardi-canada/yardi-canada-maintenance-api/) — Scheduled maintenance windows
- [Yardi Canada Status API](https://apis.io/apis/yardi-canada/yardi-canada-status-api/) — Rolled-up page status

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Yardi Virtuoso](https://apis.io/servers/yardi-canada/yardi-virtuoso/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Yardi Canada Agentic Access](https://apis.io/agentic-access/yardi-canada/yardi-canada-agentic-access/)

#### Collections (1)

Postman and Open Collection request collections.

- [Yardi Systems Status API](https://apis.io/collections/yardi-canada/open-yardi-canada-status/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Yardi Canada Status Overlay](https://apis.io/overlays/yardi-canada/yardi-canada-status-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Yardi Canada Authentication](https://apis.io/security/yardi-canada/yardi-canada-authentication/)
- [Yardi Canada Domain Security](https://apis.io/security/yardi-canada/yardi-canada-domain-security/)
- [Yardi Canada Trust Center](https://apis.io/security/yardi-canada/yardi-canada-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Yardi Canada Scopes](https://apis.io/scopes/yardi-canada/yardi-canada-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.yardibreeze.ca/)
- [Documentation](https://www.yardi.com/services/interfaces/standard-interface-options/)
- [Support](https://www.yardi.com/company/technical-support/)
- [Blog](https://www.yardibreeze.ca/blog/)
- [Compliance](https://www.yardi.com/company/cloud-security/)
- [Terms of service](https://resources.yardi.com/legal/rc-api-tou/)
- [Privacy policy](https://resources.yardi.com/legal/privacy-statement/)
- [GitHub](https://github.com/YardiSystems)
- [Status](https://status.yardi.com/)

## API Evangelist rating

**Kin Score 55.7** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 60.8 |
| Contract quality | 45.8 |
| Contract governance | 18.2 |
| Operational transparency | 34.2 |
| Developer ergonomics | 42.3 |
| Access clarity | 100.0 |

**Agent readiness 48.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | na |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | na |
| Error Semantics | — |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 40.0** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/yardi-canada/](https://apis.io/providers/yardi-canada/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Yardi Canada: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/yardi-canada/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
