# UK Lease Extension Term Calculator API

How many years are left on my flat lease and what would extending to 199 years give? Flat owners facing a lease extension are unsure how much longer their lease will last, and the maths is specific and easy to get wrong.

UK Lease Extension Term Calculator API estimates remaining term and what a fixed extension would result in, given the lease start and term. A call to GET /lease/renewal?start=1995-06-01&termYears=99 returns { "yearsRemaining": 68, "extendTo": 199, "notation": "as at today" }.

Limits: this is an arithmetic estimate, not legal or valuation advice. Actual premiums depend on valuation and negotiation and are out of scope.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The estimate is computed as at the current date and will drift as time passes, so callers should re-request rather than cache the result. It does not attempt to value the freehold premium.

A typical caller is a flat owner getting a first sense of their position before paying for professional advice. The maths is transparent and can be checked by hand.
