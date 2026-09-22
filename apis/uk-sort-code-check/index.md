# UK Sort Code and Account Validation API

UK fintech and invoicing apps must validate 6-digit sort codes and 8-digit account numbers, but there is no free authoritative sort-code-to-bank lookup, so developers hand-roll format checks. This leads to false payments and failed direct debits.

UK Sort Code and Account Validation API checks a sort code and account number together. A call to GET /validate?sort_code=20-00-00&account_number=55779911 returns { "valid": true, "sortCode": "200000", "bank": "Barclays", "branch": "Head Office", "message": "Sort code and account number are valid." }.

Limits: validation confirms format and the linked bank/branch, not that an account is open or has funds. UK Payments data offers no free authoritative sort-code-to-bank lookup, so developers write their own checks; this API is not a guarantee of payment success.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The result distinguishes a valid sort code from a validated account pair. It does not confirm the account holder's identity or authorise a payment.