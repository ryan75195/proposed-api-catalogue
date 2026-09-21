# Demand Response Readiness

Grid operators pay households to shift energy use, but knowing when a home can shed load and for how long is hard to forecast.

Demand Response Readiness reports a home's indicative shiftable load and availability window. A call to GET /readiness/{accountId} returns { "shiftableKw": 1.5, "windowStart": "2026-09-22T17:00:00Z", "windowEnd": "2026-09-22T20:00:00Z" }.

Limits: it estimates from declared appliances and behaviour patterns; it does not operate devices or guarantee load reduction.

This is a proposed design and is not implemented.

Shiftable load is estimated from declared appliances and past usage patterns rather than live measurement. It does not guarantee that load will actually be shed when a window is opened.

A typical caller is an energy aggregator grouping homes that can shift load during a grid event. The estimate supports planning even though it cannot control devices.

A readiness value near zero tells an aggregator a home is a poor candidate, which is useful signal too.
