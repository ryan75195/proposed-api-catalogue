# Local Climate Trend

Planners and farmers want to know whether a location's climate is changing beyond year-to-year noise, but raw station data is noisy and hard to summarise.

Local Climate Trend returns a smoothed trend for a temperature or rainfall metric at a location. A call to GET /trend?postcode=...&metric=tmax&since=2000 returns { "deltaC": 0.6, "direction": "warming", "years": 24 }.

Limits: it summarises observed station data only and is not a forecast or attribution study. Gaps in station data reduce confidence.

This is a proposed design and is not implemented.

The delta is the fitted change over the selected window using a simple linear model, so it is sensitive to the window chosen. Data gaps reduce the number of usable years reported.

A typical caller is a regional planner checking whether a council area is warming. The smoothed trend is easier to communicate than a scatter of noisy yearly values.

Only years with a minimum number of valid observations are counted to avoid a trend from a sparse record.
