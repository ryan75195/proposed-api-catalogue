# Loyalty Burn Rates

Loyalty points lose value when redemption options quietly worsen, and customers resent it. Merchants need to see how points are being spent and at what rate per redemption type.

Loyalty Burn Rates reports redemption volume and per-point value across redemption categories. A call to GET /programs/{id}/burn?from=2026-09-01 returns { "categories": [{ "name": "voucher", "points": 120000, "perPointValue": 0.01 }], "total": 400000 }.

Limits: it reports only redemptions it records; it does not issue points or set policy. Values are computed from posted events.

This is a proposed design and is not implemented.

Per-point value is intended as total redemption value divided by points spent in a category, which makes it easy to spot devaluation over time. No points are issued or moved by this service.

A typical caller is a loyalty dashboard that shows members where their points go. The service is meant to make devaluation visible so members are not surprised at redemption.
