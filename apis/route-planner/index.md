# Multi-Stop Route Planner

Delivery drivers waste time on unsequenced stops. Manually ordering dozens of drops rarely produces a sensible route and ignores traffic and time windows.

Multi-Stop Route Planner sequences a set of stops to minimise drive time while respecting time windows. A call to POST /routes/plan with { "stops": [{ "lat": 51.5, "lon": -0.12, "window": "10:00-12:00" }] } returns { "order": [0, 3, 1], "etaMinutes": 85, "totalKm": 62 }.

Limits: it optimises against the network and windows provided and does not account for live traffic or vehicle load. Results are a suggestion, not a dispatch.

This is a proposed design and is not implemented.

Stop indices in the returned order reference the positions in the submitted list, so clients can map results back to their own stop records. The estimate assumes steady traffic conditions.

A typical caller is a delivery app that orders a driver's drops for the day. The plan is a suggestion to be re-run as stops change rather than a fixed dispatch.
