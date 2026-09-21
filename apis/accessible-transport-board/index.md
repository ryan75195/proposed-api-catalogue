# Accessible Transport Boarding

Arriving at a stop only to find the next vehicle cannot lower or the platform has no step-free access is a common frustration for mobility aid users.

Accessible Transport Boarding reports the boarding accessibility of the next departures at a stop. A call to GET /stops/{id}/boarding returns { "next": [{ "line": "9", "departs": "14:05", "boarding": "low-floor" }] }.

Limits: boarding features are as reported by operators and can change per vehicle; absence of a feature flag does not guarantee availability.

This is a proposed design and is not implemented.

Boarding features are as reported by operators and can vary between vehicles on the same line. A missing feature flag does not guarantee that a vehicle is inaccessible.

A typical caller is a transit app showing boarding access before a user commits to a departure. The report reduces the chance of being caught at an inaccessible stop.

The list is limited to the next few departures so the response stays small and fast to render.
