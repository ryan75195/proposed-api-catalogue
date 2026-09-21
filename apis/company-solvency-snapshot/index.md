# Company Solvency Snapshot

Trade credit decisions need a fast read of whether a company is solvent, but full accounts are dense and time-consuming to digest.

Company Solvency Snapshot returns a compact solvency view from a company's latest filed accounts. A call to GET /companies/{regNo}/solvency returns { "netAssets": 120000, "currentRatio": 1.6, "status": "solvent" }.

Limits: it summarises filed data and is not a credit rating or advice. Figures are as filed and may lag the true financial position.

This is a proposed design and is not implemented.

Current ratio and net assets come from the most recent filed accounts, which can be months or a year old. The status label is a mechanical reading of those numbers, not a judgement of risk.

A typical caller is a credit controller deciding how much trade credit to extend. The snapshot is a first screening step, not a substitute for a fuller analysis.

A missing accounts year is surfaced so the reader knows the snapshot may not reflect the latest period.
