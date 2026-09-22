# SSL Certificate Expiry Check API

Teams want to alert before a site's TLS certificate expires but there is no trivial lookup endpoint. Every developer re-implements socket-based certificate inspection for the same task. Qualys SSL Labs grades SSL configuration but is a point-grading tool rather than a simple expiry-lookup API for programmatic use.

SSL Certificate Expiry Check API inspects a hostname and reports the certificate's issuer, subject, expiry date and days remaining. A call to GET /certificates?hostname=example.com returns { "hostname": "example.com", "issuer": "R10,O=Let's Encrypt,C=US", "subject": "CN=example.com", "expires_at": "2026-12-01T00:00:00Z", "days_remaining": 70 }.

Limits: it reflects what is served over TLS at the time of the request, which can change with redeploys or redirects. It does not grade configuration strength, issue certificates or provide legal assurance of a site's identity.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each lookup returns a single certificate for the resolved endpoint. The days_remaining field is computed from the observed expiry date so callers can drive alerts without doing time arithmetic.