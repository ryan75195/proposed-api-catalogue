# Rental Price Estimate for a Property API

What is a fair monthly rent for this flat based on its features and nearby comparables? Landlords and renters guess at fair rent, while regional lists are averages that ignore the specifics of a unit and paid valuations are slow.

Rental Price Estimate for a Property API returns a plausible rent range for a property based on features and comparables. A call to GET /valuations?postcode=...&beds=2&sqm=55 returns { "lower": 950, "mid": 1050, "upper": 1150, "comparables": 18 }.

Limits: it is an estimate from features and comparables it holds, not an appraisal, and should not be used as a basis for lending or legal decisions.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The range is meant to reflect comparable asking rents rather than achieved rents, which can differ in some markets. Confidence falls when few comparables exist for the area.

A typical caller is a letting agent checking whether an asking rent is plausible for a property. The range is meant to frame a conversation, not to set the final rent.
