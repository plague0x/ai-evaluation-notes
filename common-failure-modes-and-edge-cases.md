# Common Failure Modes and Edge Cases

This section captures patterns I watch for when evaluating model outputs. These are not platform-specific issues, but recurring ways models can fail in subtle or borderline situations.

---

## Common failure modes

### Overconfidence with weak grounding
The model presents an answer confidently even when evidence is thin, outdated, or missing. This often looks polished on the surface but breaks down under verification.

### Partial correctness
Parts of the response are accurate, but key details are wrong, missing, or misleading. These are risky because they feel trustworthy while still leading the user astray.

### Implicit assumptions
The model fills in gaps based on likely scenarios rather than confirmed information, without clearly signaling that it is making assumptions.

### Vague safety framing
The model gestures at caution (“be careful,” “consult a professional”) but still provides enough detail for a user to take unsafe action.

### Scope drift
The response starts within the allowed scope but gradually moves into restricted or inappropriate territory without clearly marking the transition.

---

## Edge cases I pay close attention to

- Topics that are allowed at a high level but risky if made actionable
- Requests that mix benign curiosity with potential misuse
- Hypothetical or fictional framing that still maps cleanly to real-world harm
- Situations where the user intent is unclear or evolving mid-conversation
- Answers that are technically correct but misleading without context

---

## Signals that raise concern

- Confident claims paired with no sources or unverifiable references
- Precise numbers, dates, or statistics presented without justification
- Language that discourages verification or follow-up
- Advice framed as general knowledge when expertise is actually required
- Safety disclaimers added after the fact rather than integrated into the response

---

## How I reason through ambiguous cases

When a case sits in a gray area, I focus on downstream impact:

- What might a reasonable user believe after reading this?
- Could this response reasonably lead to harm if taken at face value?
- Are uncertainty and limits clearly communicated at the right moments?
- Does the response guide the user toward safer next steps?

If the risk of harm is plausible, I treat the issue conservatively even if the content is partially correct.

---

## Guiding principle

Most failures aren’t obvious errors — they’re judgment failures.

My goal is to identify situations where an answer *sounds* helpful or correct, but quietly increases risk due to overconfidence, missing context, or poor framing.
