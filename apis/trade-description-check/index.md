# Trade Description Check

Regulated professions restrict who can use certain titles. Consumers and platforms need a quick check that a business's described activity is a registered one.

Trade Description Check matches a business's claimed activity against registered activity codes. A call to GET /check?regNo=...&claimed=financial-advice returns { "claimMatches": true, "registeredCodes": ["K"], "note": "verify licence" }.

Limits: it compares claimed activity to registry codes and is not legal advice or a licence verification; a match does not confirm permission to practise.

This is a proposed design and is not implemented.

A claim matching a registered code does not prove the right to use a protected title, which depends on separate licensing. The note field is meant to carry exactly that caveat.

A typical caller is a platform deciding whether a business's advertised activity needs further verification. The check is a red-flag prompt rather than a final answer.

The registered codes are returned so the caller can see which activities the company actually declares.
