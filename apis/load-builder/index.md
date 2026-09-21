# Load Builder

Filling a vehicle without exceeding weight or volume is done by feel in many small operations, leaving either wasted space or overloaded axles.

Load Builder packs a set of parcels into a vehicle respecting weight and volume limits. A call to POST /loads/build with { "parcels": [{ "kg": 4, "m3": 0.02 }], "vehicle": "van-small" } returns { "packed": true, "usedKg": 380, "usedM3": 2.1, "unplaced": [] }.

Limits: it ignores fragile stacking and irregular shapes; it packs by weight and volume only. It does not dispatch vehicles.

This is a proposed design and is not implemented.

Unplaced parcels are returned explicitly so a planner can see exactly what does not fit rather than silently dropping items. Utilisation is reported per vehicle for comparison.

A typical caller is a warehouse packing screen that checks a vehicle before dispatch. Reporting unplaced parcels makes it clear when a second vehicle is needed.

The vehicle catalogue holds weight and volume limits that the caller can extend when a new vehicle type is introduced.
