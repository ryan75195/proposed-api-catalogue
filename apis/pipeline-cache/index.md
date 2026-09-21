# Pipeline Cache

CI runs rebuild the same dependencies repeatedly because cache keys are inconsistent across jobs and platforms. This wastes compute and slows feedback for every push.

Pipeline Cache provides a content-addressed key service so jobs agree on what to cache. A call to POST /keys with a manifest hash returns a stable key plus an expiry; GET /entries/{key} reports whether a cached artifact exists. Output: { "key": "sha-9f2c..", "status": "hit", "sizeBytes": 1048576 }.

Limits: it does not store artifacts, only the key ledger and hit status. Retention and eviction are configured by the operator and are not guarantees.

This is a proposed design and is not implemented.

Keys include the platform and toolchain so the same manifest is not shared between different build environments. Teams can still force a miss by posting a fresh manifest hash.

A typical caller is a CI runner that asks for a key before deciding whether to restore a cache layer. Keeping the key ledger separate from storage means multiple tools can agree on the same key.
