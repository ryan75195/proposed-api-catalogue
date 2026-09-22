# Mobile Coverage Lookup by Postcode API

Apps that depend on connectivity want mobile and 5G coverage for a location, but Ofcom only offers a manual postcode checker with no API. There is no programmatic postcode lookup, so developers cannot answer connectivity questions in code.

Mobile Coverage Lookup by Postcode API lets you send a postcode and get back mobile coverage and network availability for that area. A call to `GET /coverage?postcode=SW1A1AA` returns `{ "postcode": "SW1A1AA", "networks": [{ "name": "Example Mobile", "4g": true, "5g": true }] }`.

Limits: coverage is an estimate based on modelled data, not a field measurement, and can differ indoors or at the edge of a cell. It does not guarantee service levels, speeds or availability in practice.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each network entry reports indoor and outdoor availability for 3G, 4G and 5G so callers can compare operators at a glance. The postcode is returned in the response to confirm the lookup.

A typical caller is a connectivity-dependent app checking whether a location has usable coverage before relying on it. The estimate helps triage but does not replace a real-world check.