---
generated: '2026-10-09'
method: generated
name: open-mobility-foundation-query-mobility-metrics
description: Discover and query aggregated MDS metrics
api: openapi/open-mobility-foundation-mds-metrics-openapi.yml
operations:
- get-metrics
- post-metrics
source: Grounded in openapi/open-mobility-foundation-mds-metrics-openapi.yml (from github.com/openmobilityfoundation/mds-openapi,
  MDS 2.0); every operationId verified verbatim.
---

# Discover and query aggregated MDS metrics

1. `get-metrics` — discovery: the supported metrics, times, intervals, dimensions and filters.
2. `post-metrics` — query metrics using only names, intervals and dimensions returned by discovery.

Rules: bearer token per the `bearer` securityScheme. `400` means an unsupported metric/dimension/filter combination — re-check discovery.
