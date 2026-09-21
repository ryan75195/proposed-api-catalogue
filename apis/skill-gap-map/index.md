# Skill Gap Map

Job roles change faster than qualifications, and learners cannot see which skills a role expects but their profile lacks. That makes retraining choices guesswork.

Skill Gap Map compares a supplied skill profile to the expectations of a target role and returns the gaps. A call to POST /gap with { "profile": ["sql", "excel"], "role": "data-analyst" } returns { "gaps": ["python", "dashboards"], "match": 0.6 }.

Limits: the role expectations are a model of common demand, not a guarantee of hiring criteria; profiles and roles change over time.

This is a proposed design and is not implemented.

The match score is the fraction of the role's expected skills present in the profile, so it is easy to read but insensitive to skill depth. Expectations are a model of common demand.

A typical caller is a career service helping a learner choose what to learn next. The gaps are the actionable output; the match score is just context.
