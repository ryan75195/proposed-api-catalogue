# City and Community Events Calendar API

Pull upcoming city and community events (parades, festivals, council meetings); municipal sites rarely expose an API, forcing scraping. Developers who need events from local government calendars usually end up writing scrapers that break whenever a site changes.

City and Community Events Calendar API aggregates events from local government calendars into one query. A call to GET /events?city=bristol&from=2026-10-01&to=2026-10-31 returns { "city": "bristol", "events": [{ "name": "Harbourside Festival", "start": "2026-10-11T10:00:00Z", "venue": "Harbourside", "description": "Street food and live music." }] }.

Limits: it covers city and community calendars, not ticketed commercial events. Eventbrite handles paid commercial listings, and Google Calendar embeds need per-city manual aggregation; this API provides no unified source for private or unlisted events.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each event carries a name, start and end time, venue and description, with the source council attributed so callers can trace provenance. Events may be cancelled or rescheduled by the publishing council after indexing.