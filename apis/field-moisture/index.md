# Field Moisture Readings

Irrigation decisions are made on guesswork when a field has only occasional manual moisture checks. Over- and under-watering both cost money.

Field Moisture Readings aggregates moisture sensor data for a field and returns a reading and a watering recommendation. A call to GET /fields/{id}/moisture returns { "vwcPct": 28, "status": "adequate", "trend": "falling" }.

Limits: it reports only the sensors it is given; it does not control irrigation hardware and recommendations are indicative for the measured spot.

This is a proposed design and is not implemented.

The reading is an average across the sensors configured for the field, which may not reflect dry pockets within it. Status thresholds are indicative and configurable by the grower.

A typical caller is a grower's irrigation schedule that waters a field only when the average falls below a threshold. The trend helps anticipate the next irrigation sooner.

Sensor identity is carried with each reading so faulty sensors can be spotted and excluded by the caller.
