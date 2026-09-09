---
name: cover-letter
description: Use when the user wants to write, continue, or revise a job application cover letter. Loads the shared writing-process:workflow skill for the Prewriting/Writing/Postwriting process and sets cover-letter-specific depth and defaults. Triggers on phrases like "write a cover letter," "help me apply for [role]," or "draft a cover letter for this job."
---

# Cover Letter Writing

Load `writing-process:workflow` for the process itself. This skill only sets what's specific to cover letters - depth of each stage and structural defaults - it does not redefine the stages.

## Prewriting depth
- **Rhetorical Situation:** full eight-element treatment, always - even a short document benefits from knowing exactly who's reading and what they need to hear, and this is the stage most likely to save a cover letter from sounding generic.
- **Invention:** angle-finding only by default (what's the single strongest, most specific reason this candidate fits this role) - skip Staging the Debate unless the candidate genuinely has two very different possible angles to choose between (e.g., pitching on domain expertise vs. pitching on a transferable skill after a career change), in which case run it.
- **Research:** light but real - the company's specific situation, recent news, and what the role actually needs, tied back to the Strategy element from the rhetorical situation. Not a full research process; a few well-chosen facts beat exhaustive research here.

## Writing defaults
- **Macrostructure:** a condensed shape by default - hook/statement of fit, then evidence (one or two specific, concrete examples, not a resume rehash), then a close with a clear call to action. Use full Classical structure only if the letter needs to explicitly address an objection (an employment gap, a career pivot) with its own counterargument beat.
- Run the Idea-to-Argument sequence on the central pitch (why this candidate, this role) even though the document is short - a vague or generic thesis is the single most common failure mode of cover letters, and this catches it before drafting.

## Postwriting defaults
- Run the full Style pass - cover letters are short enough that every sentence carries real weight.
- **No separate executive summary** - the letter itself is already summary-length. Skip that stage.
- The single highest-value check at Revision and Review: could this letter be sent to a different company with just a name swapped? Pose this to the user directly and let them judge it rather than answering it yourself - candidates differ on how much employer-specific detail they want, and how much is enough is the user's call, not a default to assume. If they agree it reads as swappable, fix specificity before anything else.
- Also check the draft against the ad/posting's own requirements checklist from Research (required and preferred qualifications, requested application materials, degree/status asks - see `writing-process:workflow`'s postwriting reference) - walk through any gaps one at a time with the user rather than just listing them.
- Convert to the delivery format the application actually needs - ask whether it's a formatted document or pasted plain text into a form field, since the two need different final formatting.

## After sign-off
`writing-process:extend` rarely applies to a cover letter - only offer it if the user specifically mentions an interview or presentation coming up (oral delivery practice could be relevant there).
