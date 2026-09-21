# Apprenticeship Suitability

Employers and candidates are unsure whether a role qualifies as an apprenticeship and what level applies, so promising applications get discouraged.

Apprenticeship Suitability returns whether a described role is plausibly apprenticeship-eligible and at what level. A call to GET /suitability?role=...&employerSize=40 returns { "eligible": true, "level": 4, "caveats": ["check approved framework"] }.

Limits: it is an indicator from eligibility rules and is not the funding authority's decision; approval and funding are outside its scope.

This is a proposed design and is not implemented.

Level and eligibility are read from published rules at the time of the call, so framework changes can shift the answer. The result is an indicator for planning, not an approval.

A typical caller is an employer checking whether a role could be advertised as an apprenticeship. The caveats remind them that funding approval is a separate step.

A level of zero means the role does not match a known apprenticeship level under current rules.
