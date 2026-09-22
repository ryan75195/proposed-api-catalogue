# EPC Rating Lookup by Postcode API

Property and letting software needs an energy certificate rating for a single address, but single-property lookup is portal-only and bulk data needs an account. The Energy Performance Certificate Register lets you search a single property through a web portal, and bulk CSV/API access requires a GOV.UK One Login account.

EPC Rating Lookup by Postcode API returns the registered energy certificate for a single address. A call to GET /ratings?postcode=... returns { "rating": "C", "score": 68, "certificateNumber": "1234-5678-9012-3456-7890", "address": "1 High Street, Bristol" }.

Limits: it reflects the certificate as registered and does not verify that an EPC exists, and the rating shown may be outdated if the property has not had a recent assessment. It is not an energy-efficiency audit.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Look up by postcode or by certificate number. The response carries the current rating band, the energy efficiency score, and the registered certificate details, which is what letting software needs before listing or tenancy paperwork.