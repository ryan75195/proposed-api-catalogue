# Warehouse Dock Appointment Booking API

I need a carrier to book an arrival slot at a warehouse dock before the truck leaves. Carriers arrive to find docks full, then wait or re-route, and small sites track slots in spreadsheets.

Warehouse Dock Appointment Booking API books an inbound or outbound bay slot and returns a confirmation. A call to POST /slots with { "warehouse": "uk-east", "window": "2026-09-22T14:00:00Z" } returns { "slotId": "s-881", "status": "confirmed", "bay": "B3" }.

Limits: it manages the slot ledger only; it does not manage physical dock traffic or predict wait times. Availability depends on bookings made.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

A bay is assigned at booking time and can be reassigned if a slot is cancelled and rebooked. Overlapping windows for the same bay are rejected as conflicts.

A typical caller is a carrier system that books an arrival window before a truck leaves the depot. The service helps spread arrivals but cannot control what actually happens at the dock.
