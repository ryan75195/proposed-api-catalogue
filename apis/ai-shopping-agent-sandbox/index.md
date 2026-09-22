# Test Merchant API for AI Shopping Agents API

Developers building AI shopping agents have no real storefront to test against during development. Stripe test mode provides test-only payment data but not a full mock merchant catalog to exercise browsing and purchase flows.

Test Merchant API for AI Shopping Agents API provides a mock storefront that agents can query and shop against. A call to POST /carts with { "action": "add", "product_id": "p-1001", "quantity": 2 } returns { "cart_id": "c-42", "items": [{ "product_id": "p-1001", "name": "Ergonomic Chair", "quantity": 2, "unit_price": 129.00 }], "total": 258.00 }.

Limits: all products, inventory and prices are synthetic fixtures for testing and carry no real stock or payment value. It does not process live payments, ship goods or validate real merchants.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The catalog endpoint returns product data with ids, names and prices so agents can browse and select. Cart actions let agents add, update and remove items and read a running total to exercise a full purchase flow.