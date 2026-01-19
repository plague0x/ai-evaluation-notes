# Hallucination vs. Speculation

## Working definitions
**Hallucination:** The model states a specific fact as true when it has no reliable basis for it (or the fact is likely false), and it presents it with confidence.

**Speculation:** The model explicitly signals uncertainty (e.g., “might,” “could,” “I’m not sure”), offers possibilities, and does not present guesses as confirmed truth.

## Practical cues I use
- Does it claim a concrete detail (name, date, statistic, “studies show”) without support?
- Does it cite sources that don’t exist or can’t be verified?
- Does it use confident language where uncertainty is appropriate?
- Does it clearly label uncertainty and offer safe next steps?

## Examples (high-level)
- “X happened on May 4, 2019” with no basis → likely hallucination.
- “I’m not sure, but it could be due to…” → speculation (acceptable if framed carefully).

## How I decide in borderline cases
If the output contains both:
- I focus on whether the user would reasonably walk away believing an untrue “fact.”
- If yes, I treat it as a hallucination/misinformation risk.
- If uncertainty is clear and the model suggests verification, I treat it as speculation.
