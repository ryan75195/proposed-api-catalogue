# EU VAT Number Validation API

Websites selling to EU businesses must verify VAT numbers, but the official VIES service is slow, SOAP-based, rate-limited, often returns no result and is offline during nightly maintenance, so developers hunt for a dependable wrapper.

EU VAT Number Validation API checks a country code and VAT number against EU records. A call to GET /validate?country_code=DE&vat_number=DE123456789 returns { "valid": true, "country_code": "DE", "vat_number": "DE123456789", "name": "Example GmbH", "address": "Berlin, DE" }.

Limits: validity reflects the registered data returned by EU sources at the time of the request, which can lag real-world changes. It is not a guarantee of current trading status and does not verify non-EU schemes.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each response returns valid as a boolean plus the registered name and address when available. Callers typically surface these fields on a checkout or business onboarding form.