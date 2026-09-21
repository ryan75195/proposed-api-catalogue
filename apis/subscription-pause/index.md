# Subscription Pause & Resume

Subscribers want to pause a recurring order for a holiday or a cash-flow squeeze, but many flows only allow full cancellation. That loses a customer who merely wanted a break.

Subscription Pause & Resume schedules a pause window on a subscription and returns the confirmed dates plus the next charge. A call to POST /subscriptions/{id}/pause with { "from": "2026-10-01", "until": "2026-10-20" } returns { "status": "paused", "nextChargeDate": "2026-11-01" }.

Limits: it changes only the schedule it is told to change; it does not create or cancel subscriptions or handle payment capture.

This is a proposed design and is not implemented.

Pausing is intended to defer the next charge without cancelling the plan or changing its terms. The next charge date is computed from the billing cycle and the pause window.

A typical caller is the subscription settings page that offers pause instead of cancel. The service only shifts the billing calendar and leaves payment capture to the payment processor.
