# Neighbourhood Quality Scores by Postcode API

How good is this area for transport, schools and noise before I move? A property is only as good as its surroundings, but those factors are described in scattered places, and home movers want one view of a neighbourhood.

Neighbourhood Quality Scores by Postcode API returns a compact profile of an area from location data feeds. A call to GET /areas?postcode=... returns { "score": 0.72, "facets": { "transport": 0.8, "noise": 0.5 }, "amenities": 34 }.

Limits: scores are a normalisation of the data provided, not an official quality measure, and can go stale if feeds are not updated.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Scores are normalised against the best and worst values seen in the dataset, so a middling area sits near the middle of the range. Feeds must be refreshed to keep scores current.

A typical caller is a property portal embedding a neighbourhood summary on a listing page. The single score helps comparison but hides the nuance of individual facets.
