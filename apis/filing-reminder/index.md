# Filing Deadline Reminder

Companies miss statutory filing deadlines because reminders sit in inboxes that go unread. A single view of upcoming deadlines per company would reduce late filings.

Filing Deadline Reminder returns the upcoming statutory filing deadlines for a company. A call to GET /companies/{regNo}/deadlines returns { "next": { "type": "accounts", "due": "2026-11-30" }, "late": [] }.

Limits: it lists deadlines derived from the register schedule and is not an official reminder; it does not file documents or stop penalties.

This is a proposed design and is not implemented.

Deadlines are derived from the statutory schedule for the company's accounting reference date and are not personalised reminders. The service does not send messages or file anything.

A typical caller is a finance team that consolidates filing obligations across many companies. A single view of due dates reduces the chance of a late submission.

The accounting reference date is the anchor for the schedule, so a change of year-end shifts all dates.
