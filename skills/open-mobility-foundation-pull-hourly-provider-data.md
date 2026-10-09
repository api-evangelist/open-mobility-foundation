---
generated: '2026-10-09'
method: generated
name: open-mobility-foundation-pull-hourly-provider-data
description: Pull hourly trips, telemetry and events from an MDS Provider API
api: openapi/open-mobility-foundation-mds-provider-openapi.yml
operations:
- get-vehicles-status
- get-trips-end_time
- get-telemetry-telemetry_time
- get-events-historical-event_time
- get-events-recent-start_time-end_time
source: Grounded in openapi/open-mobility-foundation-mds-provider-openapi.yml (from github.com/openmobilityfoundation/mds-openapi,
  MDS 2.0); every operationId verified verbatim.
---

# Pull hourly trips, telemetry and events from an MDS Provider API

1. `get-vehicles-status` — snapshot the fleet's current vehicle status records.
2. `get-trips-end_time` — pass required `end_time` (an hour) to get all trips ending within that hour.
3. `get-telemetry-telemetry_time` — pass required `telemetry_time` (an hour) for that hour's telemetry.
4. `get-events-historical-event_time` — pass required `event_time` (an hour) for historical status changes.
5. `get-events-recent-start_time-end_time` — for near-real-time, pass `start_time` and `end_time`; only events at most two weeks old are served.

Rules: bearer token issued by the operator (`bearer` securityScheme). Trips and historical events may answer `202` (hour not yet processed) — retry that hour later; `404` means no data for the hour. All are GET and safe to retry.
