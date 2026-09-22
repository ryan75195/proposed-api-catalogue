# Product Price Comparison API

How do I compare this product's price across merchants? Shoppers find different prices, bundles and postage for the same product, and comparing them manually is tedious and error-prone.

Product Price Comparison API matches a product identifier against a set of merchant offers and returns them ranked by total landed cost. A call to GET /offers?gtin=5031... returns { "offers": [{ "merchant": "acme", "total": 29.99, "deliveryDays": 3 }] }.

Limits: it ranks only offers that merchants have posted and does not guarantee freshness. Delivery estimates are merchant-provided, not tracked.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Total landed cost is meant to include the merchant's listed price and delivery, but excludes any taxes a shopper could not know in advance. Ranked order is for display and not a recommendation.

A typical caller is a comparison site that lists offers side by side for a product page. The service is meant to standardise what comparison means rather than rank quality.
