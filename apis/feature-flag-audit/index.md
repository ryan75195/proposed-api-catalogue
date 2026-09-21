# Feature Flag Audit

Feature flags accumulate and nobody knows which are stale, what their blast radius is, or who last touched them. Old flags become a maintenance hazard.

Feature Flag Audit scans registered flags and reports their state: rollout percentage, last modification, and how long since activation. A call to GET /flags?staleOlderThanDays=90 returns { "flags": [{ "name": "new-checkout", "rollout": 0.0, "modified": "2025-01-02" }], "count": 1 }.

Limits: it can only audit flags it has been told about via the register endpoint; it does not introspect application code.

This is a proposed design and is not implemented.

Staleness is judged by last modification, so a flag that was merely re-referenced but never changed can still be flagged. The register endpoint is intended to be called by CI whenever a flag is defined.

A typical caller is a weekly report that surfaces flags a team can retire. The service is meant to feed a cleanup review rather than make the deletion decision itself.
