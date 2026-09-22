# Restaurant Health Inspection Scores by Zip API

Where can I check a restaurant's health inspection grade? Scores are buried in fragmented local government portals, one city at a time. There is no national or zip-level lookup, so consumers cannot compare hygiene at a glance.

Restaurant Health Inspection Scores by Zip API lets you send a restaurant name or zip code and get back the inspection grade, violations, and history pulled from local health department records. A call to `GET /inspections?zip=10001` returns `{ "restaurants": [{ "name": "Example Diner", "grade": "A", "violations": 2 }] }`.

Limits: it is informational, not health advice, and reflects only the local records it has been loaded with. Coverage is inconsistent across jurisdictions and may be missing or out of date for some areas.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each inspection includes a grade, a list of violations, and a history of prior inspections so callers can spot patterns over time. The zip code makes it easy to check every option in an area.

A typical caller is a consumer deciding where to eat or a platform surfacing hygiene as part of a listing. The grade summarises the latest result but does not reflect the current kitchen state.