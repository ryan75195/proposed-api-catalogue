# When to Plant Vegetables API

I need a planting and sowing calendar by crop and location to build a garden planner. Knowing when to sow a crop depends on local frost dates and soil temperature, which vary even within a county, and guessing costs a failed germination.

When to Plant Vegetables API returns a recommended sowing window for a crop in a location from climate norms. A call to GET /calendar?crop=carrot&postcode=... returns { "window": { "from": "2026-03-20", "to": "2026-05-15" }, "frostRisk": "low" }.

Limits: it uses historical climate norms, not current weather, and does not predict a season. Local microclimates can differ from the window.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The frost risk reflects the historical last-frost date, not this year's conditions, so a cold spring can still disrupt an early sow. Multiple crop names may map to the same window.

A typical caller is a grower planning a season's sowings across a range of crops. The window is a planning aid that should be combined with on-the-ground conditions.

Locations are resolved to a nearby climate grid point, so very small sites may share the same window.
