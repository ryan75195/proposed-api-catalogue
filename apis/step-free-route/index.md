# Step-Free Route

Wheelchair users and people with luggage need to know a route avoids stairs, but standard journey planners only flag steps at one station, not along the whole path.

Step-Free Route returns a route that avoids steps and reports the accessibility features on it. A call to GET /routes/step-free?from=...&to=... returns { "stepsAvoided": 3, "legs": [{ "mode": "bus", "levelAccess": true }], "notes": ["lobby lift out of order"] }.

Limits: it reflects accessibility data it is given and can be wrong if that data is stale or unreported. It is not a medical or mobility judgement.

This is a proposed design and is not implemented.

Level access is reported per leg from accessibility data, so a leg marked as level may still have a small lip in practice. Notes surface known temporary issues such as a broken lift.

A typical caller is a wayfinding app that plans a journey for a wheelchair user. Step avoidance is the headline benefit, but the per-leg notes matter for confidence.
