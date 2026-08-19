# Stretch: Work plan for Finding 2

**Finding:** Unbounded email tool operating under the builder's identity. Severity Blocking, pending the answer to Q2.

**Objective:** The system cannot be induced by conversation input to send mail to an arbitrary recipient under John's identity.

## Deliverable

A technical change plus a short control note. Three parts:

1. **Recipient pinned at the node.** The Resend node's `to` field is set to a fixed address in the node configuration, not passed through from agent output. If a reply address supplied by the end user is needed, it goes into the body or the reply-to header, never the recipient.
2. **Content constrained.** Subject and body drawn from a fixed template with the user's message inserted as quoted text, so agent output cannot form the whole message. Length cap on the inserted text.
3. **Control note in the repository.** Half a page in `project documentation/` recording what the email tool can and cannot address, why, and what would have to change to widen it. This is what converts a fix into evidence that a fix exists.

If outbound mail to third parties is genuinely intended, the plan changes: an allowlist plus an explicit user confirmation turn, plus rate limiting per session. Materially more work, and the audit position would be that it is not worth building for a portfolio project.

## Owner

John Adams. Provider and deployer are the same person, so there is no one to delegate to and no one to escalate past. That is itself worth noting in the control note.

## Timeline

| Step | Effort | When |
|---|---|---|
| Confirm current node configuration and answer Q2 | 15 minutes | Immediately, before any public URL is shared |
| Pin recipient and template the body | 1 to 2 hours | Same day if Q2 confirms the recipient is agent selected |
| Adversarial test, ten attempts | 45 minutes | Same day, after the change |
| Write the control note | 30 minutes | Within the week |

Total under half a day. The severity comes from exposure, not from complexity.

## Verification evidence

The finding is closed when all four exist:

1. A screenshot or JSON excerpt of the Resend node showing a literal recipient address rather than an expression referencing agent output.
2. A short transcript log of at least ten adversarial attempts through the live chat interface, instructing the agent to mail an arbitrary address, with the resulting behaviour recorded. Include the attempts that came closest to working.
3. A `chat_log` and `error_log` extract from those attempts, confirming the attempts are visible after the fact rather than silent.
4. The control note committed to the repository.

Items 1 and 4 alone are not sufficient. A prompt level instruction that the agent should only mail John is not a control, because the same channel that carries the instruction carries the attack.
