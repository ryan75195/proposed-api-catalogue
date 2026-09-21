# Parcel Tracking Timeline

Tracking numbers surface only the latest event, hiding the scan history that customers and support agents need to answer where-is-it.

Parcel Tracking Timeline returns the full scan history for a tracking number with timestamps and locations. A call to GET /parcels/{tracking}/timeline returns { "events": [{ "at": "2026-09-20T08:00:00Z", "event": "depot-scan", "location": "BH11" }], "current": "in-transit" }.

Limits: it shows only events fed to it by a carrier integration and does not generate or predict events. No tracking number is real.

This is a proposed design and is not implemented.

Event types follow a small controlled vocabulary so clients can render icons consistently. Unknown events are passed through with their raw label rather than being dropped.

A typical caller is a customer service agent pasting a tracking number into a lookup. The full timeline answers where-is-it questions that a single latest event cannot.

A carrier integration is expected to push scan events in near real time for the timeline to stay current.
