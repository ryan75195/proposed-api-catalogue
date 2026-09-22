# Waste Carrier Registration Check API

Contractors and platforms must verify a waste carrier is registered before hiring, but the register is only searchable via a web form or bulk zip. The Environment Agency's public registers offer a web search form plus a bulk zip download, with no simple per-business REST lookup.

The Waste Carrier Registration Check API takes a company name, registration number or postcode and returns registration tier, status and registered address. A call to GET /carriers?name=... returns { "name": "Green Waste Ltd", "registration_number": "CBD12345", "tier": "upper", "status": "active", "address": "Bristol" }.

Limits: it confirms registration status and tier as held on the register at the time of the lookup, and is not an endorsement of a carrier's practices or a substitute for checking the full register.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each result carries the carrier name, registration number, tier (lower, upper or broker), status and the registered address, so a caller can confirm a carrier is compliant before instructing them to transport waste.