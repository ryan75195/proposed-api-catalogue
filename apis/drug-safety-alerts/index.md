# Drug Safety Alerts and Recalls API

Pharmacy and health platforms need to surface current drug safety alerts and recalls, but MHRA publishes them as filterable web articles with only an RSS feed. There is no structured API for querying by medicine name or status, so developers must scrape or manually track updates.

Drug Safety Alerts and Recalls API lets you send a medicine name or therapeutic area and get back matching safety alerts, recalls and their published date. A call to `GET /alerts?medicine=duloxetine` returns `{ "alerts": [{ "medicine": "duloxetine", "type": "recall", "published": "2025-06-02" }] }`.

Limits: it is informational, not medical or legal advice, and does not replace clinical judgement or official MHRA guidance. Coverage depends on the underlying source feeds and may lag live announcements.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each alert carries a type of safety-alert, recall or advisory, plus the medicine, therapeutic area and published date so platforms can filter and sort. The published date makes it easy to show the newest items first.