# Trip Consolidator

A trip's bookings live in separate emails and apps, so travellers cannot see conflicts or gaps across flights, hotels and transfers in one place.

Trip Consolidator merges supplied booking records and flags conflicts or gaps. A call to POST /trips/consolidate with { "bookings": [...] } returns { "itinerary": [ ... ], "conflicts": [{ "type": "overlap" }], "gaps": 1 }.

Limits: it only merges the records it is given and cannot read emails or booking sites itself; it does not manage or change reservations.

This is a proposed design and is not implemented.

Conflicts are detected between the booking records supplied, so a real conflict hidden by a missing record will not be found. The itinerary is a read-only merge and never alters reservations.

A typical caller is a traveller pasting booking references from confirmation emails into one view. The conflict list is the most valuable output and drives manual attention.
