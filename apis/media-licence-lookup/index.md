# Media Licence Lookup

Reusing an image or clip requires knowing its licence, but licence terms are buried in provider pages and often copied into metadata inconsistently.

Media Licence Lookup returns the recorded licence terms for a media asset identifier. A call to GET /assets/{id}/licence returns { "type": "royalty-free", "allowCommercial": true, "attributionRequired": true }.

Limits: it returns the terms recorded against the asset and does not grant rights or verify authenticity; a mislabelled asset can give a wrong answer.

This is a proposed design and is not implemented.

The licence terms returned are those recorded against the asset identifier, not an authoritative statement of rights. A mismatched identifier can therefore yield a wrong answer.

A typical caller is an editor reusing an asset and checking whether commercial use is allowed. The answer is only as reliable as the metadata attached to the asset.

The attribution flag tells an editor whether a credit line is required before reuse.
