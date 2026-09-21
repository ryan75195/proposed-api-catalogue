# Course Search

Learners search courses by title, but two courses with the same name can differ in length, mode and level. Search returns noise unless structured filters are used.

Course Search returns courses matching a query with structured attributes. A call to GET /courses?query=cybersecurity&level=6&mode=online returns { "courses": [{ "id": "C-41", "level": 6, "durationWeeks": 12 }], "count": 3 }.

Limits: it searches the course catalogue it is given and does not validate provider quality or accreditation; availability and fees are not covered.

This is a proposed design and is not implemented.

The catalogue is assumed to be structured with consistent level and mode values, which makes filters reliable. Fees, dates and provider accreditation are deliberately out of scope.

A typical caller is a comparison tool that lets learners filter by level and mode. Structured attributes make the filters dependable across the catalogue.

Count is returned alongside results so a learner knows when a filter is too narrow.
