---
name: Check Yardi Canada service health
description: Determine whether the Yardi services a Canadian client depends on — Voyager, Breeze, Elevate, Investor Portal, Resident Screening, EHR Interfaces — are currently healthy, using the only Yardi API callable without a contract.
api: openapi/yardi-canada-status-openapi.yml
operations: [getStatus, listComponents, listUnresolvedIncidents]
auth: none
generated: '2026-07-26'
method: generated
---

# Check Yardi Canada service health

Yardi publishes no developer portal and no API reference, but it does run a full
Atlassian Statuspage at `https://status.yardi.com` with a public, unauthenticated
JSON API — and that page is region-sliced, so a Canadian tenancy's health is
directly readable. This skill answers "is Yardi up for us in Canada right now?"

## Prerequisites

None. Every call below is an anonymous `GET` against
`https://status.yardi.com/api/v2`. Do not send an `Authorization` header; there is
no credential and none is required.

## Steps

1. **Get the rolled-up picture first.** Call `getStatus` (`GET /status.json`). It
   returns `page` and `status`. If `status.indicator` is `none` and
   `status.description` is `All Systems Operational`, nothing is broken globally —
   but this is a whole-page roll-up across every region, so do not stop here when the
   question is specifically about Canada.

2. **Resolve the Canadian components.** Call `listComponents`
   (`GET /components.json`). The response has 134 components. Build a lookup of the
   16 group components (`group == true`) by `id`, then select every component where
   `name == "Canada"` and resolve its `group_id` through that lookup. The seven groups
   that carry a Canada component are Voyager7s, Voyager8, Breeze, Elevate, Investor
   Portal, Resident Screening and Yardi EHR Interfaces. Report each as
   `"<group> / Canada": <status>`.

3. **Check for live incidents.** Call `listUnresolvedIncidents`
   (`GET /incidents/unresolved.json`). An empty `incidents` array is the normal,
   healthy result — say so plainly rather than treating emptiness as an error. For any
   incident returned, read `name`, `impact`, `status` and the newest entry in
   `incident_updates`, and check whether any entry in the incident's `components`
   array is one of the Canadian component ids resolved in step 2.

4. **Answer with the region, not the roll-up.** A `major` incident in `US West` does
   not affect a Canadian tenancy. Name which region the incident touches and say
   explicitly whether Canada is among the affected components.

## Conventions that matter here

- **No pagination.** No endpoint accepts `page`, `limit`, `cursor` or `offset`;
  collection endpoints return a fixed recent window (50 items on `incidents.json`).
  Do not attempt to page for older history — it is not reachable through this API.
- **Filtering is by path, not query.** Use `incidents/unresolved.json` rather than
  filtering `incidents.json` client-side when you only want live incidents.
- **Ids are opaque and untyped.** Component, incident and page ids are all
  12-character lowercase alphanumerics with no type prefix, so never infer an entity
  type from an id alone — always carry the entity it came from.
- **No rate-limit headers are published.** Poll conservatively; treat this as a
  status page, not a metrics feed.
- **No error contract is published.** Only `200` responses have been observed. Treat
  any non-200 as an availability problem with the status page itself, not as a
  structured API error — there is no `application/problem+json` envelope to parse.

## What this skill cannot do

It cannot read any property, unit, lease, resident or ledger data. Those live behind
the Voyager Standard Interfaces and the RentCafe API, which require acceptance into
the Interface Partnership Program and a signed Data Exchange Agreement per interface
type. If the user wants operational data, route them to
`skills/yardi-canada-connect-virtuoso-mcp.md` or to
`https://www.yardi.com/company/become-an-interface-partner/`.
