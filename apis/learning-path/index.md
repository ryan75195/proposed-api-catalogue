# Learning Path Builder

From a single goal, learners are unsure which courses to take in what order. A sensible sequence shortens time to competency.

Learning Path Builder returns an ordered sequence of courses to move from a start skill set to a goal. A call to POST /paths with { "goal": "aws-architect", "current": ["networking"] } returns { "steps": [{ "course": "C-7", "order": 1 }], "estimatedHours": 60 }.

Limits: the path is built from catalogue dependencies and is a recommendation, not a curriculum guarantee or a promise of certification.

This is a proposed design and is not implemented.

Steps are ordered by prerequisite dependencies in the catalogue, so a course is never scheduled before a course it depends on. Estimated hours are a rough total, not a commitment.

A typical caller is an onboarding platform that generates a curriculum for a new role. The dependency order prevents a learner from hitting a prerequisite gap.
