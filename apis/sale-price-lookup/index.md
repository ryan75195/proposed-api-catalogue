# Property Sale Price Lookup API

Mortgage and valuation apps want the recent sale price of a house or street, but Land Registry only publishes it as huge monthly bulk downloads. HM Land Registry's Price Paid Data is a monthly bulk text/CSV only, updated on the 20th working day, with no per-postcode lookup API.

The Property Sale Price Lookup API takes a postcode or address and returns matched sold transactions with price, date, property type and tenure. A call to GET /sales?postcode=... returns { "sales": [{ "address": "1 High Street", "price": 285000, "date": "2024-03-15", "type": "terraced", "tenure": "freehold" }] }.

Limits: it reflects completed sales recorded on the Price Paid register, which is updated monthly, so the most recent transactions may be delayed and it does not include asking prices or property valuations.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each transaction carries the address, sale price, completion date, property type and tenure, allowing a caller to build a street-level history for a valuation or affordability check.