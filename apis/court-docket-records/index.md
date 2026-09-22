# Unified Court Records and Docket API

Look up court cases, dockets, and filings without paying per-document; records sit behind fragmented, paywalled court systems. PACER charges per page and offers no clean bulk API, while CourtListener is free but has limited coverage and no live docket streaming.

Unified Court Records and Docket API returns case and docket details across court databases. A call to GET /cases?party=... returns { "caseNumber": "1:20-cv-01234", "court": "D. Mass.", "status": "open", "docket": [{ "filing": "Complaint", "date": "2024-03-01" }] }.

Limits: it summarises docket and filing metadata and is not a substitute for reviewing the official court record, and coverage varies by court. It is not legal advice.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Search by party name or case number. The response includes the docket entries, associated filings, parties, and case status so diligence teams can track a matter without per-page fees.