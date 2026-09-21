# Roster Balance

Schedulers build rosters that pass coverage checks but fail on fairness, leaving some staff with the weekends and late shifts repeatedly.

Roster Balance reports fairness metrics across a submitted roster and flags unbalanced staff. A call to POST /roster/balance with { "shifts": [...] } returns { "weekendsPerPerson": { "max": 3, "min": 0 }, "flagged": ["P-12"] }.

Limits: fairness is judged against the rules and shifts supplied; it does not create the roster or enforce agreements.

This is a proposed design and is not implemented.

Fairness is measured against the rules and shifts submitted, so the metrics are only as complete as the roster provided. It reports, but does not propose, an alternative roster.

A typical caller is a scheduler checking a proposed week before publishing it. Flagging unbalanced staff lets them fix the roster before complaints arrive.

The flagged list is the primary output so a scheduler can fix people, not re-read raw metrics.
