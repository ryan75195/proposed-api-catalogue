# Incident Brief

On-call engineers spend the first minutes of an incident reconstructing what changed and who is involved. Tooling is scattered across logs, dashboards and chat, so context is slow to assemble.

Incident Brief accepts a service name and time window and returns a compact timeline of correlated signals: deploys, config changes, error-rate spikes and recent code merges. A call to GET /incidents?service=checkout&since=2h yields { "events": [{ "at": "...", "type": "deploy", "summary": "cart-service 1.4.2" }], "suspects": ["cart-service"] }.

Limits: it aggregates whatever sources you wire in and makes no root-cause claim. Correlation is heuristic; it surfaces candidates, not diagnoses.

This is a proposed design and is not implemented. No live endpoint exists.

The brief is meant to be the first thing an on-call engineer reads before touching a dashboard. Events are deduplicated by time and type so a noisy error burst does not dominate the timeline.

A typical caller is an on-call tool that fetches this brief at page time so responders share one common timeline. The service deliberately avoids making a diagnosis so responders do not anchor on a false root cause.
