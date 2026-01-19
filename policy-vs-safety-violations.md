# Policy Violations vs. Safety Violations

## Working definitions

**Policy violation:**  
The model output breaks a documented rule or guideline, but does not necessarily create immediate or meaningful risk of harm. These are often boundary, scope, or formatting issues rather than dangerous content.

**Safety violation:**  
The output creates or meaningfully increases the risk of harm to a user, another person, or a system. This can happen even if the content appears reasonable or partially compliant on the surface.

---

## Practical cues I use

- Is the issue mainly about *rule compliance*, or about *preventing harm*?
- Would a reasonable user be put at risk by following or trusting this output?
- Is the content disallowed because it crosses a usage boundary, or because it could cause damage?
- Does the response need a simple correction, or does it require refusal and redirection?
- Does the model acknowledge uncertainty and limits where appropriate?

---

## Examples (high-level)

- Providing allowed information but in the wrong format or scope → likely a **policy violation**.
- Giving actionable guidance that could cause physical, financial, or psychological harm → **safety violation**.
- Answering a restricted topic confidently without safeguards → **safety violation**, even if no rule is explicitly cited.
- Discussing a sensitive topic at a high level with proper framing → generally acceptable.

Examples are intentionally abstract and illustrative, not tied to any specific platform or task.

---

## How I decide in borderline cases

When it’s not immediately clear, I focus on what the user could realistically do next:

- If a user might walk away believing or acting on something harmful, I treat it as a **safety risk**.
- If the issue is primarily about boundaries, structure, or completeness, I treat it as a **policy issue**.
- When uncertainty is present, I look for whether the model clearly signals limits and encourages verification.
- I prioritize harm prevention over technical correctness when the two are in tension.

The goal is to reduce real-world risk, not just enforce rules in isolation.
