# UK HMO Licensing Rules API

What HMO licensing rules apply to a property in this council area? Rules for houses in multiple occupation differ by council and change often, so landlords miss requirements and face fines because they cannot track what applies.

UK HMO Licensing Rules API generates a compliance checklist for a property address against the licensing rules for its area. A call to GET /checklists?postcode=... returns { "items": [{ "requirement": "smoke-alarm-test", "status": "required" }], "council": "Bristol" }.

Limits: it is informational, not legal advice, and reflects rules it has been loaded with. It does not guarantee a licence or exemption.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each checklist item carries a status of required, may-apply or not-applicable so landlords can prioritise. The council attribution makes it clear which ruleset the checklist came from.

A typical caller is a landlord preparing a property before a licence application. The checklist helps organise evidence but does not guarantee the licence outcome.

Requirement wording is kept short so a landlord can read it at a glance rather than wade through legislation.
