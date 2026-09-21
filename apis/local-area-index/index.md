# Local Area Index

A property is only as good as its surroundings, but transport, schools and noise are described in scattered places. Home movers want one view of a neighbourhood.

Local Area Index returns a compact profile of an area from location data feeds. A call to GET /areas?postcode=... returns { "score": 0.72, "facets": { "transport": 0.8, "noise": 0.5 }, "amenities": 34 }.

Limits: scores are a normalisation of the data provided, not an official quality measure, and can go stale if feeds are not updated.

This is a proposed design and is not implemented.

Scores are normalised against the best and worst values seen in the dataset, so a middling area sits near the middle of the range. Feeds must be refreshed to keep scores current.

A typical caller is a property portal embedding a neighbourhood summary on a listing page. The single score helps comparison but hides the nuance of individual facets.
