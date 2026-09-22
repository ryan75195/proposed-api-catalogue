# Dimensional Weight DIM Shipping Calculator API

Shipping and e-commerce code must compute dimensional (volumetric) weight, but each carrier applies different DIM divisors and rules, so developers re-implement the logic and miss oversized items. Errors cause unexpected charges at checkout.

Dimensional Weight DIM Shipping Calculator API computes dimensional and billable weight per carrier. A call to POST /calculate with { "lengthCm": 50, "widthCm": 40, "heightCm": 40, "weightKg": 3, "carrier": "ups" } returns { "carrier": "ups", "divisor": 5000, "dimensionalWeightKg": 16, "billableWeightKg": 16, "oversized": true }.

Limits: it applies the carrier's published DIM divisor and rounding rules, not negotiated or dimensional-weight exceptions. Carrier APIs such as FedEx, UPS and USPS each have different DIM rules with no unified calculator across carriers; this API does not quote rates or guarantee the final billed amount.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The billable weight is the larger of the actual and dimensional weight. The oversized flag highlights parcels whose dimensional weight exceeds the actual weight, so callers can spot charges early.