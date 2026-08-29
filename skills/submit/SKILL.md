---
description: Submit all queued highlight comments as one precise follow-up for Claude to address
disable-model-invocation: true
---

Using the Bash tool, in order:

1. Run `highlight-state list` — this prints the queued items as a JSON array of `{"quote": ..., "comment": ..., "ts": ...}`.
2. Run `highlight-state mode-off`.
3. Run `highlight-state clear`.

If the queue was empty, tell the user nothing was queued and stop.

Otherwise, treat the queued items as the user's actual follow-up request for this turn — not a meta-summary of what they did.

Don't just reply to each comment in isolation. Step back and read your original response together with every queued comment as one set of feedback on that response — like an editor's markup on a document, not a list of separate questions. Then decide the best shape for your reply based on what the feedback actually calls for:

- If the comments reveal the response needs correcting, rebalancing, or restructuring, rewrite the relevant parts (or the whole response) rather than bolting on point-by-point patches.
- Where a comment is a specific question, correction, or pushback that doesn't require rewriting anything, address it directly and reference the quote so it's clear which part you're responding to.
- If the feedback, taken together, surfaces an ambiguity or a fork in what to do next, ask a concise follow-up question instead of guessing.

Use whichever mix of these fits — a revised response, direct replies, a follow-up question, or some combination — but make sure every queued item is accounted for somewhere in your reply.
