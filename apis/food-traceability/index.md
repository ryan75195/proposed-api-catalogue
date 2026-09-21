# Food Traceability Map

A contamination recall needs to find where a batch went, but the supply chain is fragmented across suppliers and documents. Manual tracing takes too long.

Food Traceability Map returns the upstream and downstream path of a batch identifier. A call to GET /batches/{id}/path returns { "upstream": [{ "supplier": "Farm Co", "batch": "F-221" }], "downstream": ["Warehouse 4"] }.

Limits: it maps only the chain that has been recorded with it; gaps in the data produce gaps in the trace and it is not a substitute for a recall authority.

This is a proposed design and is not implemented.

Upstream suppliers and downstream destinations are returned as recorded links, so a missing hop shows as a gap rather than being silently bridged. The map is not an official recall statement.

A typical caller is a quality team asked by an authority for the path of a batch. Showing gaps explicitly helps them know where their records are incomplete.
