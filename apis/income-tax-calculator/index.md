# Income Tax Calculation and Reporting API

Compute exact tax owed for an individual or business; no reliable public engine exists and commercial ones are locked down. Intuit/TurboTax keeps its calculation engine closed rather than exposing a general API, and IRS Free File offers no public calculation or filing API for developers.

Income Tax Calculation and Reporting API computes tax due from income, deductions and jurisdiction and returns quarterly reporting figures. A call to POST /calculations with { "jurisdiction": "US-FEDERAL", "filing_status": "single", "gross_income": 75000, "deductions": 13500 } returns { "tax_due": 8450.00, "effective_rate": 0.1127, "quarterly": [{ "period": "Q1", "payment": 2112.50 }] }.

Limits: results are estimates for planning, not filed returns, and the engine reflects rules it has been loaded with for the jurisdictions it supports. It does not guarantee an audit outcome or replace a licensed tax professional.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each calculation returns tax_due in the reporting currency and a breakdown of quarterly payments. Figures change with rate and threshold updates, so callers should pass the tax year explicitly.