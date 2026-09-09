# Writing: full reference

Loaded by `workflow` when running Part 2. Adapted from the Argumentation and Drafting chapters of "The Process of Generative AI Writing."

## 1. Argumentation

### Idea to Argument (thesis/pitch generation)
Run as a sequence, not a single request:
1. Capture the user's raw, informal belief about their angle in one sentence (their gut instinct, unpolished).
2. Generate 4-5 versions of a sharpened claim from it, varying the type (a claim about outcomes, a claim about approach, a claim about fit, a comparative claim).
3. Cut the weak ones - state a specific reason for each cut (too vague, unsupported, doesn't fit the reader's stated priorities from Prewriting).
4. Stress-test what survives: what does it assume, what would a skeptical reader object to, what evidence would it need?
5. Have the user select the strongest surviving version, or synthesize the best of two.
6. Refine it with real specifics (numbers, names, dates) rather than placeholders.
7. Sharpen it once more for what makes it distinct - why this pitch, from this candidate/vendor, and not an interchangeable one.

**Output:** one specific, arguable, evidence-backed thesis/pitch sentence.

### Thesis testing
Before drafting, stress-test the thesis from at least two angles:
- **Reasoning check:** does the claim hold up as an inductive argument (enough evidence to support the generalization) or a deductive one (valid premises leading to the conclusion)? Name the premises explicitly - a claim resting on an unstated premise the reader wouldn't grant is a real weakness to fix now, not after drafting.
- **Rhetorical appeals:** produce three reframed versions of the thesis - one leading with credibility/authority (ethos), one leading with shared values or need (pathos), one leading with logic/data (logos) - then synthesize the version that balances them for this specific reader (from the Audience analysis in Prewriting).
- **Fallacy scan:** check the thesis and its main supporting claims for false dilemma, hasty generalization, slippery slope, false cause, straw man, and red herring. Fix anything real; note anything borderline for the user's judgment rather than silently rewriting around it.

## 2. Drafting

### Optional baseline draft
When the user is facing a blank page and it would help: generate a fast, complete first-pass draft directly from the Prewriting/Argumentation material, explicitly framed as a floor to edit against, not a finished product. Mark it up immediately after - what's usable, what's generic filler to cut, what's missing - rather than treating it as done. This is the exception, not the default: prefer getting a seed of the user's own rough writing first (even one raw sentence) and building from that, and only offer to draft a piece straight from nothing when the user is genuinely stuck or explicitly asks for it.

### The sentence-level drafting loop
Before starting a new section (Drafting as a whole, or a specific paragraph within it), briefly preview its sub-steps - e.g. "hook, then the roadmap sentence, then body paragraphs starting with topic sentences, then the close" - so the user knows what's coming, then work through them one at a time and note where the sequence is as you move through it.

Default to this loop at the sentence and paragraph level: ask the user for their rough, unpolished version of the next piece (a topic sentence, a claim, a transition); tighten just that one piece rather than drafting ahead; ask the user to lock it in or take another pass; then ask one small, concrete question that seeds the next piece. This is deliberately granular - it keeps the user writing and deciding throughout instead of reviewing a large chunk of Claude's prose after the fact.

### Macrostructure (overall arrangement)
Pick one, and say why:
- **Problem-Orientation** (Situation -> Problem -> Solution -> Evaluation): the default for a proposal - it's the natural shape of "here's what's happening, here's the gap, here's what we do about it, here's why it works."
- **Classical** (Introduction -> Background -> Claim -> Counterargument -> Conclusion): strong for persuasive writing that needs to address skepticism head-on.
- **Toulmin** (Claim -> Grounds -> Backing -> Qualifier -> Rebuttal): good when the argument's logical chain itself needs to be visible and defensible.
- **Rogerian** (Opposing position -> context for it -> your position -> context for it -> shared benefits): best when the reader is likely to start skeptical or is invested in an alternative - it builds common ground before asking for agreement.

Draft an outline in the chosen structure and get it approved before writing full prose - do not improvise a new structure mid-draft; if the outline turns out wrong, stop and revisit Argumentation rather than patching around it in prose.

### Mesostructure (paragraphs)
For each section of the approved outline, choose a paragraph type suited to its job (causal, descriptive, evaluative/pros-and-cons, comparison, sequential, categorical, definitional, or ranked-by-importance) rather than defaulting to the same shape throughout - variety keeps the argument from feeling repetitive and signals deliberate structure to the reader.
Within paragraphs, default to a claim-evidence-analysis-link shape (state the point, back it, explain why it matters, connect to what follows) unless a simpler list format genuinely serves the content better.

### Microstructure (sentences)
Draft at the sentence level in the user's own voice, not a generic "polished AI" register - if the user dictates or free-writes a passage, preserve its natural rhythm and correct only clarity issues at this stage; save systematic style work (parallelism, wordiness, variation) for Postwriting.

**End-of-stage output:** a complete draft with confirmed macrostructure, ready for Postwriting.
