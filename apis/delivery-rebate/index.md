# Delivery Rebate Ledger

Retailers pay carriers for delivery but rarely reconcile whether promised service levels were met. Missed SLAs quietly go unclaimed.

Delivery Rebate Ledger records delivery outcomes against a service-level promise and computes a claimable rebate. A call to POST /deliveries/{id}/assess with { "promised": "before-18:00", "actual": "19:02" } returns { "slaMet": false, "rebatePence": 250 }.

Limits: it computes rebates from posted data only and does not enforce contracts or raise claims. Amounts are estimates based on the tariff supplied.

This is a proposed design and is not implemented.

The promised service level is supplied per assessment so the same delivery can be judged against whichever tariff applies. Rebates are estimates and do not constitute a filed claim.

A typical caller is a retail finance team reconciling delivery spend against contracted service levels. The service turns a vague promise into a number that can be checked.

The rebate tariff is supplied alongside the assessment so different contracts can be evaluated with the same call.
