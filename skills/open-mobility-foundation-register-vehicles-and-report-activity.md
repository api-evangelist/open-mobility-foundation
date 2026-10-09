---
generated: '2026-10-09'
method: generated
name: open-mobility-foundation-register-vehicles-and-report-activity
description: Register vehicles with a city Agency API and push events, telemetry and trips
api: openapi/open-mobility-foundation-mds-agency-openapi.yml
operations:
- post-vehicles
- put-vehicles
- get-vehicles-status
- post-events
- post-telemetry
- post-trips
source: Grounded in openapi/open-mobility-foundation-mds-agency-openapi.yml (from github.com/openmobilityfoundation/mds-openapi,
  MDS 2.0); every operationId verified verbatim.
---

# Register vehicles with a city Agency API and push events, telemetry and trips

1. `post-vehicles` — register vehicles for use in the agency's jurisdiction (`409` = already registered; use `put-vehicles` to update).
2. `post-events` — send vehicle state change events for multiple vehicles.
3. `post-telemetry` — send telemetry in batches for any number of vehicles.
4. `post-trips` — send updates about one or more trips.
5. `get-vehicles-status` — read back the agency's view of vehicle status.

Rules: bearer token issued by the agency. POSTs are not declared idempotent in the spec; on `400`/`404` inspect the per-item failures before resending, and do not blindly replay a whole batch.
