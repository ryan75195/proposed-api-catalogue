# Secrets Rotation Planner

Rotating a credential across many services is manual and error-prone; a secret may be rotated in one consumer and forgotten in another. No one wants to discover the gap during an outage.

Secrets Rotation Planner maps a secret identifier to every consumer that references it and suggests an ordered rotation. A call to GET /secrets/{name}/consumers returns { "consumers": [{"service": "api-gateway", "path": "env/DB_PASS"}], "lastRotatedAt": "..." }.

Limits: it reports dependencies it is told about; it cannot detect references it was never given. It does not perform rotations or write credentials.

This is a proposed design and is not implemented.

The consumer map is meant to be maintained alongside deployment manifests so it stays accurate. A rotation plan is a proposal only; it never reads, writes or transmits the secret value itself.

A typical caller is a compliance tool that lists consumers during a scheduled rotation. Because it only holds references, the service can be given a read-only view of the environment.
