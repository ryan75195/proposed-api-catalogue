# Draft Rewrite

Teams produce drafts at different reading levels for different audiences, but rewriting for tone, length or clarity by hand is slow and inconsistent.

Draft Rewrite returns a rewritten version of supplied text for a requested tone and length. A call to POST /rewrite with { "text": "...", "tone": "plain", "targetWords": 150 } returns { "rewritten": "...", "wordCount": 148, "tone": "plain" }.

Limits: rewrites are generated suggestions that need human review; they are not a substitute for professional editing or legal wording.

This is a proposed design and is not implemented.

The target length is treated as a guide rather than a strict bound so the rewrite reads naturally. Tone and length are applied together, so a plain rewrite is shorter and more direct.

A typical caller is a comms team producing a plain-language version of a technical brief. The rewrite is a draft a human edits rather than a final document.
