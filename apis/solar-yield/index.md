# Solar Yield Estimate

Households weighing solar panels get payback figures that differ by installer and weather. A neutral, location-based yield estimate helps compare.

Solar Yield Estimate returns an indicative annual generation estimate for an array at a location. A call to GET /solar/yield?postcode=...&kwp=4.0&tilt=35 returns { "kwhPerYear": 3800, "confidence": "medium", "bestMonth": "June" }.

Limits: it estimates from irradiance norms, not live weather or shading, and is not a quote or an electrical design. Real yield will vary.

This is a proposed design and is not implemented.

The estimate assumes a clear-sky irradiance profile for the location and an unshaded array, so surrounding buildings can reduce real output. It is meant for comparing options, not sizing a system.

A typical caller is a household comparing two installer proposals by their yield figures. A neutral estimate gives them a baseline against which to judge those quotes.

Results are returned monthly so a user can see which part of the year contributes most generation.
