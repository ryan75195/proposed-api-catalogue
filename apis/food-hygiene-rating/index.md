# Food Hygiene Rating Lookup API

Food-delivery and review apps want a hygiene rating for a restaurant, but ratings are only searchable through the FSA's public web portal. The FSA Food Hygiene Ratings portal provides a public search page, and the underlying ratings data has no simple stable per-business API.

Food Hygiene Rating Lookup API returns the hygiene rating for a premises. A call to GET /ratings?postcode=... returns { "business": "The Crown", "rating": 5, "score": 5, "authority": "Bristol City Council", "address": "1 High Street, Bristol" }.

Limits: it reflects the rating as published by the local authority and may lag the most recent inspection. It is not an endorsement of food safety and does not substitute for a formal compliance check.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Search by business name or postcode. The response includes the hygiene rating band, the numeric score, and the rating authority so apps can show a consistent badge and attribute the source.