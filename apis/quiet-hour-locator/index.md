# Quiet Hour Locator

Sensory-sensitive visitors plan shopping around quieter times, but which venues run a quiet hour and when is scattered and often out of date.

Quiet Hour Locator returns venues near a location that run a reduced-stimulus quiet hour. A call to GET /quiet-hours?postcode=... returns { "venues": [{ "name": "Central Library", "when": "Sat 09:00-10:00" }] }.

Limits: it lists what venues have self-declared; hours can change without notice and absence of a listing does not mean a venue is not quiet.

This is a proposed design and is not implemented.

Quiet hours are self-declared by venues and are not independently audited, so they can be cancelled or changed without notice. A venue without a listing may still be quiet at off-peak times.

A typical caller is an accessibility feature on a venue map that filters to quiet times. It helps sensory-sensitive visitors choose when to go, not where to shop.

Opening and closing of the quiet window are both returned so it can be shown on a venue card.
