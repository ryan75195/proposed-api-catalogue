# Broadband Availability at Postcode API

Developers need to check what broadband and fibre speeds are actually available at a given postcode, but the data only exists behind a manual web checker. Ofcom's Broadband Checker is a manual web form only, with no programmatic endpoint, and bulk data requires large annual downloads.

The Broadband Availability at Postcode API takes a UK postcode and returns fixed broadband availability, fibre-to-the-premises coverage and advertised speeds for that location. A call to GET /availability?postcode=... returns { "postcode": "BS1 5TR", "fibre_fttp": true, "max_speed_mbps": 1000, "suppliers": ["Openreach"] }.

Limits: it reports advertised availability and speeds, not measured performance at a specific connection, and does not guarantee that a supplier will install a service at the address.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Responses carry a fibre-to-the-premises flag plus maximum advertised download speed and the list of supplier networks present, so a caller can quickly tell whether a fibre service is realistic before contacting an ISP.