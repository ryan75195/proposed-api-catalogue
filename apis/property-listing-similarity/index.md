# Similar Property Listings Matching API

Which nearby listings are comparable to this property, and how similar are they? Buyers see one listing at a time and cannot tell if the asking price is in line with similar homes, because descriptions vary wildly in how they describe the same things.

Similar Property Listings Matching API matches a listing against comparable ones using structured features rather than headline text. A call to POST /listings/{id}/similar returns { "similar": [{ "id": "L8821", "score": 0.91 }], "basis": ["type", "sqm", "area"] }.

Limits: similarity is computed on features provided and is not an appraisal. It cannot infer features that are missing from a listing.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The basis array states which features contributed to matching so the caller can weigh how meaningful a high score is. Listings missing key features are not silently penalised.

A typical caller is a buyer's search that flags unusually priced listings for review. Similarity on structure is more reliable than comparing free-text descriptions.

A low score is returned as a candidate for manual review rather than treated as an automatic rejection.
