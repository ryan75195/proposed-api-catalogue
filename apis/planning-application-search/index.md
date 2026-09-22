# Planning Application Search by Postcode API

Developers and buyers want planning applications near an address, but each council exposes them only through its own web portal with no unified API. Hundreds of separate council web portals exist with no single programmatic register across authorities.

The Planning Application Search by Postcode API takes a postcode and returns local planning applications with status, description and decision dates. A call to GET /applications?postcode=... returns { "applications": [{ "reference": "24/01234/FUL", "description": "Erection of rear extension", "status": "under-consideration", "decision_date": null }], "council": "Bristol" }.

Limits: it aggregates what individual councils publish and does not guarantee a complete or definitive planning history; applicants should confirm details with the relevant authority.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each application carries a reference, a short description of the proposal, its current status and the decision date where one exists, so a caller can track nearby planning activity for a purchase or development decision.