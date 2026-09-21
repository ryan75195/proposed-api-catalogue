# Cart Session Recovery

Shoppers abandon carts and return later to find their items gone or the price changed. Recovering a session should restore intent without forcing a full rebuild.

Cart Session Recovery matches a returning visitor token to a previously saved cart and returns the items plus any price deltas. A call to GET /carts/{token}/restore yields { "items": [{ "sku": "SW-12", "qty": 2 }], "priceDeltas": [{ "sku": "SW-12", "old": 20.0, "new": 22.5 }] }.

Limits: it stores only what the merchant posts; it does not re-price automatically or place orders. Prices shown are advisory snapshots.

This is a proposed design and is not implemented.

The token is meant to be set client-side and expires after a configurable period. Price deltas are snapshots from the saved session and are not live quotes at retrieval time.

A typical caller is the checkout page that re-hydrates a returning visitor's cart. The service is meant to reduce friction at return rather than drive the purchase itself.
