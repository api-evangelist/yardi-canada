# Yardi Canada (yardi-canada)

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

Yardi Canada Ltd. is the Canadian subsidiary of Yardi Systems, Inc. (Goleta, California), opened in Mississauga in 1998 and now headquartered in Toronto with regional offices in Saskatoon and Vancouver and roughly 500 staff. It sells, implements and supports the Yardi property and investment management stack in Canada — Voyager, Breeze Premier, RentCafe, Home IQ, Matrix and Pulse — across residential, commercial, affordable, senior living and investment portfolios, and its Canadian footprint grew by acquisition: Point2 Technologies in Saskatoon in 2010, an EnerNOC division in Vancouver in 2016, and Planimetron in Toronto in 2022. It sits on the systems-of-record rung of the value chain rather than the listing or land-registration rung — it is the ledger and operating platform a landlord or asset manager runs on, not a portal like REALTOR.ca and not a registry operator like Teranet. Its API posture, stated honestly, is licensed-access-only and partner-gated. There is no public developer portal: `developer.`, `developers.`, `api.` and `docs.` hosts do not resolve on either `yardi.ca` or `yardi.com`, and the primary Canadian domain `yardi.ca` — registered to Yardi Systems, Inc. since 2003 — resolves to 104.156.161.80 but serves no web content at all (TCP 443 and 80 both time out). Real interfaces exist, but only behind the Interface Partnership Program: an application, a signed Data Exchange Agreement per interface type, a company at least two years old with three or more active Voyager clients, and an annual per-interface fee. RESO is absent entirely — Yardi appears nowhere in the RESO certification directory — which is the expected result for a Canadian property management vendor, because Canadian residential listings move through CREA's DDF and REALTOR.ca rather than through RESO-certified MLS endpoints.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/yardi-canada/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/yardi-canada/refs/heads/main/apis.yml)

## Tags

- Real Estate
- Canada
- Property Management
- Rentals
- Commercial Real Estate
- PropTech
- Multifamily
- Affordable Housing
- Senior Living
- Investment Management
- Tenancy
- Payments

## Timestamps

- **Created:** 2026-07-26
- **Modified:** 2026-07-26

## APIs

Two real, documented interface programs are listed — and neither is reachable without a signed commercial agreement. Both are listed **without a base URL**, because Yardi publishes none and the commonly-cited `api.yardi.com` host does not resolve (NXDOMAIN).

### Yardi Voyager Standard Interfaces

The documented family of Voyager web-service interfaces that Yardi Canada clients and their vendors integrate against — Collections, Commercial, Construction, Internet Listing Service (ILS) and Guest Card, Maintenance, Master Data, Payables, Receivables, Renters Insurance, Revenue, Screening, and Senior Living EHR/eMAR. Several are described by Yardi as MITS-based or MITS-compliant; the Commercial interface is described as built on the OSCRE standard. The contracting party is Yardi Systems, Inc.; Yardi Canada Ltd. is the Canadian delivery and support entity. No base URL, endpoint list, WSDL, OpenAPI or OData `$metadata` document is published anywhere public.

- **Human URL:** [https://www.yardi.com/services/interfaces/standard-interface-options/](https://www.yardi.com/services/interfaces/standard-interface-options/)

#### Properties

- [Documentation](https://www.yardi.com/services/interfaces/standard-interface-options/)
- [Getting Started](https://www.yardi.com/company/become-an-interface-partner/)
- [Partners](https://www.yardi.com/company/become-an-interface-partner/)

### RentCafe API

The RentCafe marketing, leasing and resident-services API, used by Yardi Canada's multifamily clients and their vendors. Yardi's published RentCafe API Terms of Use names concrete operations in its Schedule A — `getapartmentavailability`, `getfloorplans`, `getunitpricingdetails`, `getpropertydetails`, `getamenities`, `getofficehours`, `createlead`, `getavailableslots` and `createappointment` — and states that use "is by way of that certain RentCafe API Access Agreement between you and Yardi Systems, Inc." Access is restricted to vendors serving "Common Clients", credentials are described only as an access token, and the vendor may not pass Common Client Data to third parties. `https://www.rentcafe.com/api/` no longer serves documentation.

- **Human URL:** [https://resources.yardi.com/legal/rc-api-tou/](https://resources.yardi.com/legal/rc-api-tou/)

#### Properties

- [Terms of Service](https://resources.yardi.com/legal/rc-api-tou/)
- [Getting Started](https://www.yardi.com/company/become-an-interface-partner/)
- [Documentation](https://www.yardi.com/products/rentcafe/)

See [review.yml](review.yml) for the full probe log, RESO posture, access gate, open-data assessment and auth model.

## Sector Posture

| Fact | Finding |
| --- | --- |
| Home market | Canada |
| Tier | Property management |
| RESO posture | No RESO reference found — the full RESO certification directory contains zero Yardi, Point2 or RentCafe entries; Canadian RESO certification sits with the boards (ITSO, Vancouver Island REB, Victoria REB) |
| RESO certified | No |
| Access gate | `partner-only` — Interface Partnership Program application, a Data Exchange Agreement per interface type, 2+ years in business, 3+ active Voyager clients, annual per-interface fee; the RentCafe API additionally requires a RentCafe API Access Agreement and confines use to "Common Clients" |
| Open data | No — Yardi Matrix and Canadian rent research are subscription products; Canada's open counterweight is weak because land registration is privatised (Teranet) and listings sit with a single national co-operative (CREA DDF) |
| Auth model | Opaque access token issued under contract; no scheme documented, and no OpenID Connect discovery document is served on `www.yardi.com` or `www.yardibreeze.ca` (both 404) |
| Machine-readable public surface | **Corrected 2026-07-26** — two exist, and neither is REST-with-a-portal: an official first-party MCP server (`https://mcp.virtuoso.ai`, with anonymous RFC 8414 / RFC 9728 OAuth metadata) and a public status API (`https://status.yardi.com/api/v2`, 8 unauthenticated endpoints). Still no OpenAPI published by Yardi, no OData `$metadata`, no AsyncAPI, no GraphQL, no SDK, no CLI, no Postman collection, no webhooks |
| Primary domain | `yardi.ca` resolves to 104.156.161.80 but serves nothing; the live Canadian site is `www.yardibreeze.ca` |

## Common Properties

- [Website](https://www.yardibreeze.ca/)
- [Website](https://www.yardi.com/)
- [About](https://www.yardi.com/blog/global/yardi-canada-ltd-celebrates-25-years/37395.html)
- [Partners](https://www.yardi.com/company/become-an-interface-partner/)
- [Documentation](https://www.yardi.com/services/interfaces/standard-interface-options/)
- [Terms of Service](https://resources.yardi.com/legal/rc-api-tou/)
- [Solutions](https://info.yardi.com/asset-management-software-for-canada)
- [GitHub Organization](https://github.com/YardiSystems)
- [LinkedIn](https://www.linkedin.com/company/yardi)

## Maintainers

- Kin Lane — kin@apievangelist.com

## Enrichment round 2 (2026-07-26)

Round 1 recorded "no machine-readable contract to capture". Probing the hosts round 1
never reached corrected that in two places. The access gate is unchanged — the Voyager
Standard Interfaces and the RentCafe API are still partner-only with no published
contract — but Yardi's public surface is not empty.

### Yardi ships an official MCP server

The **Yardi Virtuoso Connector** is listed on the Anthropic connector directory
([claude.com/connectors/yardi-virtuoso](https://claude.com/connectors/yardi-virtuoso))
and served from `https://mcp.virtuoso.ai`. Announced in early access 2025-09-10 and as
available-now in Virtuoso Enterprise 2026-06-16, declared **Read & Write**, with
published capabilities for portfolio performance, financial data and NOI comparison,
work order management, invoice review and approval, quarterly business review and
budget forecasting.

Its authorization contract is anonymous and genuinely machine-readable — RFC 9728
protected-resource metadata and RFC 8414 authorization-server metadata, both saved
verbatim in [`well-known/`](well-known/): OAuth 2.1 authorization code, PKCE `S256`,
refresh tokens, dynamic client registration, scopes `openid profile email
offline_access`. Those scopes carry identity only; Yardi states data access follows the
caller's existing Yardi user permissions.

**No tool names are recorded in this repository.** Anonymous `tools/list` is blocked by
Cloudflare (HTML 403 on `/mcp`, `/sse`, `/v1/mcp`, `/api/mcp`, `/mcp/v1` and `/`), and
the connector's technical documentation returns HTTP 401. Tool lists published by
third-party MCP directories were deliberately not copied in.

### A public, Canada-sliced status API

`https://status.yardi.com` is a full Atlassian Statuspage whose eight JSON endpoints
Yardi documents itself at [status.yardi.com/api](https://status.yardi.com/api). All
eight return HTTP 200 anonymously. The page carries **134 components in 16 product
groups**, and seven of those groups expose an explicit **Canada** component — Voyager7s,
Voyager8, Breeze, Elevate, Investor Portal, Resident Screening and Yardi EHR Interfaces.
Canadian events are named outright ("Issue impacting Yardi Voyager users in the Canada
region", 2026-07-17; "Maintenance - Canada Region - Thursday April 23 - 11:00pm EDT").
That makes it the only anonymous, machine-readable read on Yardi Canada's production
service health, and [`openapi/yardi-canada-status-openapi.yml`](openapi/yardi-canada-status-openapi.yml)
was derived from Yardi's own published endpoint list plus the verified live responses.

### Artifacts added this round

| Artifact | What it records |
| --- | --- |
| [`openapi/`](openapi/) | The status API, 8 operations, derived from the published endpoint list + verified 200s |
| [`overlays/`](overlays/) | API Evangelist annotations over that spec, including the Canadian component filter |
| [`mcp/`](mcp/) | The Virtuoso Connector profile, and a tool crosswalk recording that the MCP and REST surfaces do not overlap at all (binding rate 0.0) |
| [`well-known/`](well-known/) | Two real OAuth discovery documents, plus every miss across five hosts |
| [`authentication/`](authentication/) · [`scopes/`](scopes/) | Three coexisting auth regimes; the four published OAuth scopes |
| [`conformance/`](conformance/) | PCI, SSAE 18 / SOC 1 + SOC 2, SOX, HIPAA, CSA STAR Level 2, FIPS 140-2; MCP authorization, RFC 8414, RFC 9728, PKCE, DCR; no RESO, no OData, no RFC 9457 |
| [`security/`](security/) | The Cloud Security page as trust surface; TLS/HSTS/DNS probes across five hosts (no DNSSEC, no CAA, no DMARC on `yardibreeze.ca`) |
| [`lifecycle/`](lifecycle/) · [`changelog/`](changelog/) | Status page detail and Canadian incident history; seasonal Breeze Premier release posts; no deprecation policy, no SLA, no API changelog |
| [`conventions/`](conventions/) · [`data-model/`](data-model/) | What is knowable per surface (idempotency is genuinely absent); the status entity graph and how to resolve the Canadian slice |
| [`packages/`](packages/) | Zero official SDKs; two community clients, one a SOAP client that corroborates the interface style |
| [`sandbox/`](sandbox/) | A real vendor sandbox that no developer can reach |
| [`skills/`](skills/) | Three agent skills grounded in verified operationIds and verified OAuth metadata |
| [`llms/`](llms/) | A generated llms.txt — Yardi's `robots.txt` allows `/llms.txt` for AI crawlers, but that file 404s |

See [review.yml](review.yml) `enrichmentRound2` for the full probe log.
