# GTIN Barcode Validation and Lookup API

E-commerce apps need to validate GTIN/UPC/EAN barcodes and resolve the GS1 prefix and product info, but validators are just libraries and the official GS1 data is not machine-readable. The GS1 official parsers ship as a C library only, and official GS1 data is not exposed as a hosted lookup API.

GTIN Barcode Validation and Lookup API checks a GTIN/UPC/EAN barcode and resolves its GS1 prefix and product metadata when available. A call to GET /lookup?barcode=4006381333931 returns { "barcode": "4006381333931", "valid": true, "check_digit_ok": true, "gs1_prefix": "400", "product_name": "Sample Product", "manufacturer": "Example Corp" }.

Limits: check-digit validity is computed locally and reliably, but product metadata depends on the coverage of the underlying data and is empty when no record exists. It does not guarantee a product's authenticity or retail availability.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Every response reports valid and check_digit_ok so callers can reject malformed codes, plus the GS1 prefix and any available product fields. Lookup coverage varies by barcode and region.