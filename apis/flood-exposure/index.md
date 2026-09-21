# Flood Exposure Score

Buyers and insurers want a sense of flood risk for an address, but maps are hard to interpret for a single plot and are full of caveats.

Flood Exposure Score returns a coarse exposure score for an address from flood map data. A call to GET /exposure?postcode=...&address=... returns { "score": 3, "band": "moderate", "sources": ["rivers", "surface"] }.

Limits: it is a score derived from maps at plot resolution, not a site survey or a guarantee of insurability, and must not be used as the sole risk decision.

This is a proposed design and is not implemented.

The band is a coarse grouping of the underlying score and is not a statutory flood zone designation. It should be combined with official maps and a site visit before any decision.

A typical caller is a buyer screening a shortlist of addresses before a deeper enquiry. The score helps prioritise which plots warrant a closer look.
