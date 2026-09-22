# Company Charges Register Lookup API

Lenders and diligence tools want a company's registered charges, but the charges register is searched through the Companies House website with no clean structured lookup. Companies House charges search lets you browse charge details on the website, and full charge documents are not exposed as a simple lookup.

Company Charges Register Lookup API returns the registered charges for a company. A call to GET /charges?companyNumber=01234567 returns { "company": "Example Ltd", "charges": [{ "type": "Fixed charge", "amount": 250000, "status": "outstanding" }] }.

Limits: it reflects charges as registered and may not capture every collateral arrangement, and it does not provide the full charge documents. It is not legal or credit advice.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Search by company number or name. The response includes each charge's type, amount, and status so lenders can assess a company's secured obligations before transacting.