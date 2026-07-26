# Yardi Canada (yardi-canada)

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
| Machine-readable public surface | None — no OpenAPI, no OData `$metadata`, no AsyncAPI, no GraphQL, no SDK, no CLI, no Postman collection, no webhooks |
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
