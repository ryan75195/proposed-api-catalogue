# Step-free Accessible Route Planner API

Show me a route between two places that avoids all stairs and steps. Wheelchair users and people with luggage need to know a route avoids stairs, but standard journey planners only flag steps at one station, not along the whole path.

Step-free Accessible Route Planner API returns a route that avoids steps and reports the accessibility features on it. A call to GET /routes/step-free?from=...&to=... returns { "stepsAvoided": 3, "legs": [{ "mode": "bus", "levelAccess": true }], "notes": ["lobby lift out of order"] }.

Limits: it reflects accessibility data it is given and can be wrong if that data is stale or unreported. It is not a medical or mobility judgement.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Level access is reported per leg from accessibility data, so a leg marked as level may still have a small lip in practice. Notes surface known temporary issues such as a broken lift.

A typical caller is a wayfinding app that plans a journey for a wheelchair user. Step avoidance is the headline benefit, but the per-leg notes matter for confidence.
