# Visa Requirements by Nationality API

Does a traveller from this country need a visa for that destination? Travellers piece together visa rules from forum posts and stale pages, and a structured lookup by nationality and destination would give a clear first answer.

Visa Requirements by Nationality API returns the visa requirement for a nationality travelling to a destination. A call to GET /requirements?nationality=...&destination=... returns { "requirement": "visa-on-arrival", "durationDays": 30, "sourceDate": "2026-07-01" }.

Limits: it reflects rules as last published and is not an immigration decision or a guarantee at the border; rules change and require official confirmation.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The requirement reflects rules as last published on the source date and is not an official border decision. Nationals may also face additional rules that a simple lookup cannot capture.

A typical caller is a travel planning site presenting a first answer before the traveller confirms with an embassy. It reduces obvious mismatches, not edge cases.

The source date lets a traveller know how old the rule is before relying on it for planning.
