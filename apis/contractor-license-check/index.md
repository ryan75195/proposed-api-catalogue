# Verify Contractor License Status by State API

Verify a contractor's license is active before hiring; every state board publishes data differently, mostly as hard-to-query portals. There is no unified API, so checking a license means visiting each board's site.

Verify Contractor License Status by State API lets you send a contractor name or license number plus state and get back active status, license class, and expiry from state board records. A call to `GET /licenses?license_number=ABC123&state=TX` returns `{ "license": "ABC123", "status": "active", "expires": "2027-01-31" }`.

Limits: it is informational and reflects the state board records it has been loaded with. It does not guarantee a contractor is fit to work and should not be treated as an endorsement or certification of competence.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each result carries the license class, current status and expiry date so callers can quickly see whether a contractor is current. The state is returned in the response to confirm which board the record came from.

A typical caller is a homeowner or platform screening a contractor before engaging them. The check helps confirm currency but does not verify work quality or insurance.