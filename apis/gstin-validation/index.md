# India GST Number GSTIN Validation API

Indian e-commerce and invoicing apps must verify 15-character GSTIN numbers, but the government GSTN portal has no friendly public API, so platforms re-implement regex and lookup logic. This risks accepting invalid or blacklisted tax numbers.

India GST Number GSTIN Validation API checks a 15-character GSTIN. A call to GET /validate?gstin=27AAPFU4258B1ZV returns { "valid": true, "gstin": "27AAPFU4258B1ZV", "legalName": "Example Traders Pvt Ltd", "stateCode": "27", "status": "ACTIVE", "registrationDate": "2021-04-01" }.

Limits: it reports registration and format validity, not tax liability or compliance standing. The India GSTN portal is not scriptable, and third-party aggregators gate access behind GSP onboarding; this API does not fetch every registration detail the portal holds.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each response carries the legal name, state code and registration status so callers can match a GSTIN to a registered entity. It does not verify the identity of the person making the request or authorise a transaction.