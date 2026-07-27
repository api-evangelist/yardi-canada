---
name: Watch Yardi Canada maintenance windows
description: Find upcoming, active and recent scheduled maintenance windows affecting the Yardi Canada region, so integrations and batch jobs can be scheduled around them.
api: openapi/yardi-canada-status-openapi.yml
operations: [listUpcomingScheduledMaintenances, listActiveScheduledMaintenances, listScheduledMaintenances]
auth: none
generated: '2026-07-26'
method: generated
---

# Watch Yardi Canada maintenance windows

Yardi gives partners no advance-notice API, no webhook and no deprecation calendar.
The status page's scheduled-maintenance feed is the only public advance warning a
Canadian integrator gets — and Yardi does name Canadian windows explicitly, e.g.
`Maintenance - Canada Region - Thursday April 23 - 11:00pm EDT`.

## Prerequisites

None. Anonymous `GET` against `https://status.yardi.com/api/v2`.

## Steps

1. **Is a window running right now?** Call `listActiveScheduledMaintenances`
   (`GET /scheduled-maintenances/active.json`). An empty array means nothing is in
   progress. If non-empty, read `name`, `scheduled_for`, `scheduled_until` and the
   latest `incident_updates` entry.

2. **What is coming?** Call `listUpcomingScheduledMaintenances`
   (`GET /scheduled-maintenances/upcoming.json`). Sort by `scheduled_for`. Treat any
   entry whose `name` contains `Canada` — or whose `components` array includes a
   component named `Canada` — as in scope for a Yardi Canada client.

3. **What is the pattern?** Call `listScheduledMaintenances`
   (`GET /scheduled-maintenances.json`) for the recent window (50 items observed) and
   group by region keyword in `name` to show cadence. This is how to answer "how often
   does Yardi take the Canada region down, and when?" — Yardi publishes no maintenance
   policy, so the observed history is the only evidence.

4. **Convert times deliberately.** `scheduled_for` and `scheduled_until` are UTC
   (`Etc/UTC` per `page.time_zone`), but the human `name` is written in local time
   (EDT/EST/Pacific). When they disagree, trust the timestamps and say so.

## Conventions that matter here

- Maintenance objects share the `Incident` shape and add `scheduled_for` /
  `scheduled_until`; `incident_updates` carries the running commentary for both.
- Region is not a field. It is expressed in the free-text `name` and via the
  `components` array — always corroborate with `components` rather than string
  matching alone.
- No pagination, no query filters, no rate-limit headers (see
  `conventions/yardi-canada-conventions.yml`).

## Follow-on

Nothing in this feed announces API or interface changes. For product change
communication see `changelog/yardi-canada-changelog.yml`; for the absence of a
deprecation policy see `lifecycle/yardi-canada-lifecycle.yml`.
