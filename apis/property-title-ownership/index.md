# Property Title and Ownership Lookup API

Legal and diligence workflows need to confirm who owns a property, but HM Land Registry title searches sit behind a paid business e-services portal. HM Land Registry e-services require a paid business account and offer no free programmatic title lookup across the register.

The Property Title and Ownership Lookup API takes an address or postcode and returns title register ownership and tenure information where available. A call to GET /titles?postcode=... returns { "titles": [{ "address": "1 High Street", "owner": "Jane Doe", "tenure": "freehold", "title_number": "AV123456" }] }.

Limits: it returns ownership and tenure information only where a title is registered, and cannot confirm the identity of the legal owner with certainty or serve as a substitute for a full official title search.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

Each result carries the property address, registered owner, tenure and title number where available, letting a caller identify who owns a property before progressing with a purchase or due-diligence check.