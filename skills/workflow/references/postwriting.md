# Postwriting: full reference

Loaded by `workflow` when running Part 3. Adapted from the Style, Revision and Review, and front/back-matter chapters of "The Process of Generative AI Writing."

## 1. Style

Before starting, and periodically as the passes proceed, surface the full current draft (or a wide excerpt) rather than only the isolated sentence(s) under discussion - it's hard to make good editing decisions without seeing the whole document in context.

Work through these in order - each is a distinct pass, not one blended edit. Whenever a pass flags something, quote the actual text in question (don't just describe the problem) and pose it to the user as a question rather than silently resolving it yourself:

- **Grammar:** fix real errors (misplaced/dangling modifiers, fragments, double negatives), and briefly explain the fix when it's not obvious - this is copy-editing, not a rewrite.
- **Transitions:** check that consecutive sentences connect old information to new ("known-new"), and that paragraph openings bridge back to what came before ("Janus" transitions - looking both ways). Flag at least the two or three weakest spots rather than rewriting every transition uniformly.
- **De-AI-ing / voice check:** a pass distinct from grammar or sentence craft - scan for phrasing that sounds like Claude's generic default register rather than the user's own voice (formulaic antithesis constructions like "not X, but Y" or "because X, not Y"; unearned literary flourishes; abstract compression that flattens a concrete idea). Use the user's own raw inputs from earlier in the process (their Idea-to-Argument answers, topic sentences, freewriting) as the actual reference for their voice, not a generic "polished" register. Where the environment supports it, offer a visual highlighted/tagged version of the draft (color-coded spans with short labels naming the flag) as an alternative to describing each spot in prose - useful enough to offer by default at this pass, not just when asked.
- **Sentence craft**, in this order:
  - *Parallelism* - symmetrical structure across list items, comparisons, and multi-clause sentences.
  - *Wordiness* - cut unnecessary doublings, intensifiers, and filler; flag anything cut so the user can restore it if it was intentional.
  - *Variation* - break up repetitive sentence length/opening/structure; alternate short and long.
  - *Active/passive* - default active for directness, but keep passive where the actor is genuinely unknown or unimportant, or where it improves flow into the next sentence.
  - *Phrasal placement* - keep the subject and verb close together; move long introductory clauses that bury the main point.
- **Rhetorical appeals revision** - a second, sentence-level pass distinct from the thesis-level pass in Writing:
  - *Logos* - is the sequence of claims within each paragraph logically ordered, not just individually true?
  - *Pathos* - does emotional language inform without manipulating? Flag anything that risks reading as manipulative or one-sided and suggest a more balanced version rather than removing the emotional content outright.
  - *Ethos* - are claims that need support actually backed (data, references, credentials), and is opinion clearly distinguished from fact where the distinction matters to credibility?

## 2. Revision and Review

### Hierarchy of Concerns
Before touching grammar or word choice (Lower-Order Concerns), review for Higher-Order Concerns: focus, organization, thesis clarity, and use of evidence. A document can be grammatically flawless and still fail because its argument is misplaced or its evidence is thin - fix that first. Explicitly separate the two passes; don't let LOC fixes (a nicer sentence) substitute for HOC fixes (the paragraph is in the wrong place).

If Prewriting/Research produced a requirements checklist from a source document (a job ad's required/preferred qualifications, requested materials, degree/status asks - see `references/prewriting.md`), treat checking the draft against it as a Higher-Order Concern in its own right: not just "is the argument sound" but "is everything the source material explicitly asked for actually addressed." Where the draft is missing something conventional for the genre generally (not just this checklist) - a standard element of an academic cover letter, say - walk the user through the gaps one at a time rather than listing them all and leaving the user to self-serve; ask what to do about each before moving to the next.

### Cohesion technique (run at least one)
- **Reverse outline:** summarize each paragraph's main idea in one line, lay the summaries out as an outline, and check whether that outline actually matches the intended structure and whether a stranger could follow the whole argument from the summaries alone.
- **Cut and rearrange:** label each paragraph by its function, then propose one or two alternative orderings with a stated rationale for each.
- **Highlighter approach:** label sentences/clauses by category (claim/evidence/analysis, or whatever categories fit the document) and check the balance - a section heavy on claims with no evidence, or vice versa, needs attention.
- **Diagnosis/analysis/revision:** identify the first few words of each sentence in a suspect paragraph and check whether the topical focus develops logically sentence to sentence, or drifts.

### Getting real feedback
Do not skip straight from draft to "done." Get critique through at least one of:
- Ask the user directly for their honest reaction.
- Simulate several distinct reviewer personas (e.g., a friendly subject-matter expert, a skeptical detail-oriented critic, an informed generalist outside the field) who are explicitly invited to disagree with each other - then have the user weigh the disagreements rather than averaging them away.
- Route to a real outside reviewer if the document warrants it (see the plugin's collaborator handling - this version assumes solo use by default).

When the user is reviewing someone else's writing (or Claude is helping them phrase peer feedback), translate blunt first-reaction notes into specific, constructive, actionable comments - preserve the substance of the critique, not just soften its tone into vagueness.

## 3. Front and back matter

- **Proposal:** write a one-page executive summary by default (situation, problem, proposed solution, the ask/benefit) - see the proposal skill for specifics. Only add a table of contents, appendices, or glossary if the document is long/formal enough to need navigation aids, and only when the user asks for them.
- **Cover letter:** no separate summary - the letter itself is already summary-length. Skip this stage entirely unless the user specifically wants a one-line "hook" opener as a lightweight analog.
- Anything beyond this default (abstract, keyword list, index, full TOC) is out of scope for the default workflow - offer it only through the optional `writing-process:extend` skill if the user asks.

**End-of-stage output:** the finished, signed-off document.
