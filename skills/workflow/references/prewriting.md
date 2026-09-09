# Prewriting: full reference

Loaded by `workflow` when running Part 1. Adapted from the Prewriting section of "The Process of Generative AI Writing" (rhetorical situation, prompt engineering, invention, research) for direct execution by Claude rather than for a student pasting prompts into a separate chat window.

## The editorial roleplay mechanic

For each rhetorical situation element below, do not analyze it silently. Explicitly adopt the relevant expert persona and interview the user step by step - this keeps the analysis structured rather than free-associated, and it's the mechanism the book's method actually runs on. Before the persona asks its question, give the element's "Teach:" line (or your own version of it) in plain language - what this element is and why it matters - so the user understands the concept, not just the prompt. Then state the persona, ask its question (one element at a time, not all eight at once or even two at once), and summarize findings before moving to the next element.

The "Teach:" lines below are written at full length for a first-time or student user. They're a starting point to draw from, not a script to recite verbatim every time - compress to a single clause, or skip straight to naming the element and asking, once the user shows fluency with the concept or asks to move faster. A working professional who already thinks in these terms shouldn't get a paragraph-length lecture on what audience analysis is.

Where a diagram would clarify an element (marked "Diagram:" below), offer to produce one. In an environment with real diagramming tools, render it. Otherwise, produce a clear structured-text equivalent (labeled tiers, an indented tree, etc.) - never skip the exercise just because rendering is unavailable.

## 1. Rhetorical Situation (all eight elements, every time)

### Audience
Teach: Audience analysis is where every rhetorical decision downstream gets grounded - a document written for the wrong reader fails regardless of how well-crafted the prose is. Introduce the idea of primary and secondary audiences: the primary audience is whoever's reaction actually controls the outcome (the hiring manager, the funding committee); secondary audiences are readers who see the document without being the decision-maker (a screening system, a colleague the primary reader consults, a future reader who finds it later). Most documents have both, and conflating them is a common source of a document that doesn't land.
Persona: an expert editor and audience strategist.
Ask: Who specifically reads this - one person, a committee, a screening algorithm first? What do they already believe, know, and want? What would make them say no? Rank likely readers by how much their reaction actually controls the outcome.
Diagram: concentric circles - primary decision-maker at the center, secondary influencers and gatekeepers in outer rings.

### Author
Teach: This element asks what standing the writer actually has to say this, separate from what they're saying. A gap between a writer's real authority and the authority the document implicitly claims is one of the more common reasons a piece rings false.
Persona: a credibility consultant.
Ask: What authority does the writer actually have on this topic (role, experience, relationship to the reader)? Is there a gap between the writer's real standing and the standing the document needs to project? For roleplay/practice exercises (e.g. rehearsing an interview answer), distinguish Author (Actual) - the real person - from Author (Assumed Role) - a persona being practiced.

### Purpose
Teach: Purpose is the single most commonly skipped element because writers assume they already know it - but "communicate value" or "explain the project" isn't a purpose, it's a topic. Purpose names the general aim of the piece and, where one exists, the concrete outcome behind it (to win a competition, to get funding approved, to inform a reader, to process an experience, to fulfill an assignment) - it is not yet the specific argument or thesis that will achieve that aim. That's a different question, and it belongs to Invention, later - if the answer here starts naming a specific argument or stance rather than a general aim, note it as a candidate for Invention and keep this element about the aim itself.
Persona: a strategy consultant.
Ask: What is this piece trying to accomplish, in general terms - inform, persuade, entertain, win a competition, get something specific approved, fulfill an assignment, process an experience? If there's a concrete next action a reader should take (approve funding, extend an interview, sign a contract), name that specifically rather than a vague goal like "communicate value" - but stop at the aim; don't reach for the specific argument that gets there yet.

### Context
Teach: Context is everything happening around the document that isn't in the document itself but still shapes how it's read - timing, what else the reader is weighing, pressure they're under. The same sentence lands differently depending on what the reader was worried about five minutes before they opened it.
Persona: a situational analyst.
Ask: What's happening around this document that shapes how it lands - timing, competing options the reader is weighing, recent events, organizational pressure? What must the reader already be worried about?
Diagram: spider/radar chart of contextual pressures (budget, timeline, competing priorities, politics).

### Medium
Teach: Medium is the actual physical or digital form the document travels in, and it isn't neutral - a portal upload with a character limit, an email opened on a phone, a printed leave-behind each force and forbid different things (length, formatting, whether images survive). Decisions made before knowing the medium often have to be undone once it's known.
Persona: a delivery-format specialist.
Ask: How will this actually be read - a printed leave-behind, an email attachment opened on a phone, a portal upload with a character limit? What does the medium force or forbid (length, formatting, attachments)?

### Genre
Teach: Every genre carries conventions readers expect whether or not they could name them - and a document that violates them without a deliberate reason reads as a mistake, not a choice. Genre analysis is about learning which conventions are load-bearing (breaking them reads as incompetence) and which are just habit (breaking them can read as confidence).
Persona: a genre convention expert.
Ask: What does this type of document conventionally include, and where can convention be broken for effect versus where breaking it reads as incompetence? What do the best examples of this genre share?
Where practical, locate one or two real examples of the genre in question (a sample cover letter for a similar academic role, a comparable proposal) rather than relying only on general genre knowledge, and use them to check or sharpen the conventions named here.
Diagram: decision tree - genre conventions to follow strictly vs. bend vs. safely ignore for this specific case.

### Content
Teach: Content here doesn't mean "everything true and relevant" - it means the specific, ranked subset that actually moves this particular reader toward the action named in Purpose. Most drafts fail not from omitting facts but from including true, impressive facts the reader doesn't care about at the expense of the ones that would have moved them.
Persona: a content strategist.
Ask: Of everything that could be said, what must be included for the reader to say yes, and what's actually irrelevant to them even if it's true and impressive? Build a ranked list, not a complete inventory.

### Strategy
Teach: Strategy isn't an eighth independent fact to gather - it's the synthesis of the seven elements above into one governing approach to how the document leads (with credibility, with empathy, with data, with urgency). Naming it explicitly, out loud, before drafting is what keeps the later stages consistent with each other instead of drifting.
Persona: an overall rhetorical strategist.
Ask: Given everything above, what's the single governing approach - lead with credibility, lead with empathy, lead with data, lead with urgency? Strategy is the synthesis of the previous seven elements into one guiding choice, not an eighth independent question - review the prior answers before naming it.

**End-of-stage output:** a short rhetorical situation summary (a few sentences per element is enough, not an essay) that the user explicitly approves before Invention begins.

## 2. Invention

The topic is already fixed (this job, this contract) - Invention here means finding the strongest specific argument or angle within it, not discovering a topic from scratch. Depth is set by the calling document skill; run at minimum the first technique below, and the others when the document is high-stakes enough to warrant it.

- **Angle-finding (always run):** Thesis/angle formation is real thinking work and deserves real time - don't compress it into one exchange. Ask first, openly, given the rhetorical situation summary: what's the user's own instinct for the strongest argument or angle here? That message contains only the question - no candidate sentence offered alongside it "just in case," even hedged as "here's a shot, but shape it yourself." Handing over a fully-formed sentence in the same breath as asking is still Claude doing the thinking; wait for an actual answer first. Once the user offers something, even rough or partial, treat it like the sentence-level Drafting loop: reflect back and tighten just what they gave you, ask them to lock it in or take another pass, don't rewrite it into your own version. Only after the user has made a real attempt and says they're stuck, or explicitly asks for options or examples, generate 3-5 distinct possible angles or emphases (e.g., for a proposal: cost-efficiency angle vs. speed-to-market angle vs. risk-reduction angle), state the tradeoff of each plainly, and ask which resonates or invite a hybrid - this fallback only follows a genuine attempt, never arriving pre-emptively.
- **Staging the debate (optional, higher-stakes documents):** Argue the strongest case for two or three competing angles as if they were rival consultants pitching the user, then have the user (or Claude, explicitly noting it's doing so) moderate and pick a winner or blend.
- **Classical topoi (optional):** Prompt for supporting material using the classical categories - comparison (how does this compare to alternatives), circumstance (why now), testimony (precedent, references, prior results), definition (what does "success" mean here specifically).
- **Freewriting toward voice (optional, when the user is stuck):** Ask a sequence of open questions (who, what, when, where, why) and have the user answer in their own words without editing, then identify the most specific, most alive sentence they produced as a seed for drafting.

**End-of-stage output:** one clear sentence naming the chosen angle.

## 3. Research

Depth is set by the calling document skill - thin for most cover letters (light company research), substantial for most proposals (client situation, comparable precedents, supporting data).

- Identify what claims in the eventual document will need support, and go find or ask the user for that support before drafting, not after.
- For company/client research: what does the reader's organization actually care about right now (recent news, stated priorities, competitors)? Connect this back to the Strategy element from the rhetorical situation.
- For evidence-heavy proposals: gather comparable examples, cost/benefit data, and precedent cases; note the source and reliability of each rather than treating AI-suggested "examples" as verified fact - flag anything that needs the user to confirm it's real before it goes in the document.
- Keep a running short list of source -> claim mappings rather than a full annotated bibliography (that apparatus is built for academic research writing and is overkill here) - unless the document skill says otherwise.
- When the document responds to a source document with explicit asks (a job ad's required/preferred qualifications and requested materials, an RFP's stated requirements), extract those into a short, explicit checklist as part of Research - not just background reading material, but a literal list of things the document must be checked against later. Carry this checklist forward; Postwriting's Review stage checks the draft against it directly (see `references/postwriting.md`).

**End-of-stage output:** a short list of key findings/evidence the draft will lean on, plus the requirements checklist where one applies, approved by the user, closing out Prewriting.
