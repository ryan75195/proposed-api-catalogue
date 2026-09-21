# Form Data Extraction

Scanned forms are still processed by hand in many offices. Reading fields off a scan reliably would save hours, but generic OCR is noisy.

Form Data Extraction reads labelled fields from a scanned form image. A call to POST /forms/extract with a file reference returns { "fields": [{ "name": "customerRef", "value": "C-9981", "confidence": 0.93 }] }.

Limits: accuracy drops on handwriting and low-quality scans, and results should be reviewed; it is not a certified or authoritative read.

This is a proposed design and is not implemented.

Field names follow a template the caller registers, so extraction is predictable for known forms. Confidence per field lets a human reviewer focus only on low-confidence values.

A typical caller is an office that digitises intake forms before a workflow. Predictable field names mean the output can feed a downstream system unchanged.

A low-confidence field is included rather than omitted so nothing is silently dropped from the record.
