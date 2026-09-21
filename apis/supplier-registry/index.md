# Supplier Registry Lookup

Procurement teams need to confirm a supplier exists and see its verified identifiers before onboarding. Manual verification across registers is slow.

Supplier Registry Lookup resolves a supplier to its registry record and verified identifiers. A call to GET /suppliers/{id} returns { "regNo": "1234", "vatNo": "GB...", "status": "verified", "foundedYear": 2010 }.

Limits: it returns identifiers it has verified against the register data available; it does not vouch for performance or financial reliability.

This is a proposed design and is not implemented.

Verified identifiers are those the registry data supports; some fields may be blank where a record is incomplete. The result is a confirmation of identity, not of creditworthiness.

A typical caller is a procurement onboarding step that validates a supplier before contracting. Verified identifiers reduce the risk of acting on a misspelt record.

A blank verified field is returned explicitly rather than hidden, so gaps in the record are visible.
