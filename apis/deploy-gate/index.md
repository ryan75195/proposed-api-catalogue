# Deploy Gate

Teams struggle to stop a bad deployment before it reaches production. Rollouts are often gated by human sign-off that lags behind the pipeline, so a failed canary can sit live for minutes while watchers are offline.

Deploy Gate accepts a proposed release ID and returns an approve or block decision by combining configured policies: blast-radius size, on-call coverage, and how long the canary has been green. A call to POST /releases/{id}/decide with the release id and a canary-health ratio returns { "decision": "block", "reasons": ["on-call rotated", "error-rate above 2%"] }.

Limits: it does not run pipelines or enforce anything; it only reports a recommendation. Decisions are advisory, configurable per service, and carry no rollback or automation hook.

This is a proposed design and is not implemented. No live endpoint exists; the example above is illustrative only.

The decision logic is intended to run in the pipeline as a reviewer, not a gatekeeper with override power. Teams may configure policy weights per environment so a hotfix can proceed with fewer checks than a weekend release.
