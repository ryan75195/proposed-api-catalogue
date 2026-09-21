# Document Format Converter

Exchanging files between teams means converting formats that do not preserve structure well, like moving a styled document to plain text or a table to CSV.

Document Format Converter converts a supplied document between formats while preserving structure. A call to POST /convert with { "fileRef": "doc-1", "from": "docx", "to": "markdown" } returns { "status": "converted", "outputRef": "out-7", "lossy": false }.

Limits: conversion cannot preserve features unsupported in the target format and flags lossy cases; it does not archive or publish documents.

This is a proposed design and is not implemented.

Lossy is set true when the target format cannot represent some feature of the source, so callers can warn users. Structural elements like headings and tables are preserved where supported.

A typical caller is a team standardising on a format for a repository. The lossy flag tells them when a round-trip will lose structure so they can avoid it.
