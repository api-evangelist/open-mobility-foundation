---
generated: '2026-10-09'
method: generated
name: open-mobility-foundation-discover-policy-requirements
description: Read an agency MDS requirements document and active policies
api: openapi/open-mobility-foundation-mds-policy-openapi.yml
operations:
- get-requirements
- get-policies
- get-policies-policy_id
- get-policies.json
source: Grounded in openapi/open-mobility-foundation-mds-policy-openapi.yml (from github.com/openmobilityfoundation/mds-openapi,
  MDS 2.0); every operationId verified verbatim.
---

# Read an agency MDS requirements document and active policies

1. `get-requirements` — enumerate which MDS/CDS/GBFS APIs, endpoints and fields the agency requires from providers.
2. `get-policies` — list policy documents, optionally bounded by `start_date` / `end_date`.
3. `get-policies-policy_id` — fetch one policy by id.
4. `get-policies.json` — flat-file alternative for agencies that publish a static policies document.

Rules: the spec declares no securityScheme for Policy; the agency decides whether it is public. Geography ids referenced by rules resolve via the MDS Geography API (`get-geographies-geography_id` in the Geography spec).
