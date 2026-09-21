# Director Crosscheck

A person may hold directorships across several firms, and counterparties want to know if the same names sit on troubled companies. Manual lookup is slow.

Director Crosscheck returns the directorships of a named individual across companies. A call to GET /people/{personId}/directorships returns { "companies": [{ "regNo": "1234", "role": "director", "status": "active" }] }.

Limits: it reflects the register data provided and is not a vetting or suitability judgement; name collisions can occur and require exact identifiers.

This is a proposed design and is not implemented.

Results depend on a stable person identifier, so name-only searches can be ambiguous. Status reflects the register at the time of lookup and can change with new filings.

A typical caller is a counterparty checking whether the same person sits on many companies. The crosscheck surfaces connections that a single-company lookup would miss.

The person identifier is required so that two directors sharing a name are not merged by accident.
