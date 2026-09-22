# Building Permit Data by City and Date API

Get building permit records for lead gen; data is public but buried in inconsistent city open-data portals. There is no unified query, so pulling permits means wrestling each city's separate portal.

Building Permit Data by City and Date API lets you send a city and date range and get back permits with address, permit type, project value, and contractor identity. A call to `GET /permits?city=austin&start=2025-01-01&end=2025-01-31` returns `{ "permits": [{ "address": "100 Main St", "type": "residential", "value": 250000 }] }`.

Limits: it is informational and reflects only the city records it has been loaded with. Coverage and field completeness vary by jurisdiction, and some cities may not yet be indexed.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each permit carries the address, permit type, project value and contractor identity so callers can identify new work in an area. The date range makes it easy to watch for fresh permits as they are issued.

A typical caller is a business generating leads from new construction or renovation. The feed helps surface opportunities but does not guarantee permit accuracy or completeness for every city.