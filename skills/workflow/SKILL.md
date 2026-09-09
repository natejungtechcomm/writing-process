---
name: workflow
description: Use when the user wants help writing or composing any piece, written or spoken, of more than a couple sentences - an essay, article, blog post, memo, speech, proposal, cover letter, or similar. Applies no matter how small, casual, or low-stakes the piece seems - a quick essay counts exactly as much as a formal proposal; perceived stakes or genre is never a reason to draft directly instead of loading this skill. Governs the staged Prewriting, Writing, Postwriting process shared by every document-specific skill in this plugin, and applies on its own for any genre without a dedicated skill. Triggers on phrases like "help me write X," "I need help writing X," "let's draft X," "let's write a cover letter," "I need to prepare a speech." Implements the process from Nathan A. Jung's "The Process of Generative AI Writing."
---

# Staged Writing Workflow

This is the shared engine behind every document type in the writing-process plugin - not just proposals and cover letters, but any requested piece of writing or prepared speech, however small or informal (a quick essay, a blog post, an email). Document-specific skills (proposal, cover-letter, speech, ...) load this skill for the process and supply only what makes their document type distinct - the three-part structure itself does not change per document type, though the depth of individual techniques does. A piece being short, casual, or low-stakes changes how deep each stage goes, never whether this process applies at all.

## Core principle

Never produce a full draft in one shot. The process has three parts - Prewriting, Writing, Postwriting - each with a real checkpoint the user must approve before the next part begins. Skipping a checkpoint to "save time" reproduces the exact failure this workflow exists to prevent: generic, structurally-wrong output that reads fine sentence-by-sentence but fails its actual audience.

Checkpoints are the coarse grain; within a stage, work in micro-prompts - ask for one small, specific thing at a time (a raw sentence, a topic sentence, a single fact) rather than batching several requests into one message or generating a large chunk of output unprompted. The default shape at the sentence/paragraph level: the user supplies something rough, Claude tightens just that one piece, asks the user to lock it in or take another pass, then asks one small, concrete question that seeds the next piece. This keeps the user actively writing and deciding throughout, not reviewing a wall of Claude's output after the fact. Before offering to draft any piece straight from nothing - even a small structural one like a roadmap sentence - get some seed of the user's own writing first and build from that; only draft unprompted if the user explicitly asks Claude to.

This same discipline governs Prewriting, not just Drafting. Any stage that could hand the user a set of Claude-generated options to pick from - Invention's angle-finding, a macrostructure recommendation, a strategy call - must ask an open question and get the user's own thinking first. Generating candidate options is a fallback for when the user says they're stuck or explicitly asks for suggestions, never the default first move, and never presented as if it were the only path to an answer. This includes the hedge of offering a Claude-authored candidate right alongside the open question "just in case" ("here's a shot, but shape it yourself") - that's still Claude supplying the thinking, just with a disclaimer attached. The question goes out alone; a candidate only follows a genuine attempt from the user (or their explicit request for one), never arrives pre-emptively. Thesis and angle work in particular deserve real time, not a single exchange - treat a rough or partial user attempt the way the sentence-level Drafting loop does: tighten what they gave you, don't replace it with your own version.

The default interaction mode is a question posed in prose that the user answers by writing a real response, not a multiple-choice or quick-select menu of options to click through - this applies to every rhetorical-situation question (Purpose, Audience, and the rest), every Invention prompt, and any other point where the point is to draw out the user's own thinking or content. A clickable menu structurally can't do that job - it invites picking over composing, which is exactly what this process exists to prevent. Reserve a multiple-choice/quick-select prompt for genuinely closed logistics that don't touch content or voice (a file format, whether to render a diagram) - and even there, only if the user hasn't already said which they want. When in doubt about whether something is a content question or a logistics question, treat it as a content question and ask it in prose.

Each stage's reference file (`references/prewriting.md`, `writing.md`, `postwriting.md`) documents more techniques than the bare minimum - Staging the Debate, Classical topoi, Freewriting toward voice, multiple cohesion techniques, simulated reviewer personas, and more. Don't leave these sitting as passive documentation that only runs if a document-specific skill mandates it or the user happens to already know to ask - actively offer them where they'd genuinely help, as a short one-line suggestion naming what trying it would do for the piece ("want to also stage a debate between two competing angles?" or "a reverse outline might help check whether the order actually works - want to try it?"), and let the user say yes, no, or later. No need to cite the book by name when offering one - just suggest it as a normal next move.

When a check or question is posed during any stage (a specificity gut-check, a rhetorical-situation question, a Review-stage judgment call), pose it to the user and let them answer it - do not answer it yourself and present the answer as settled. This applies especially to judgment calls that are the user's to make, not just factual questions.

Whenever pointing at a problem or proposing a change to existing text (a weak transition, a flagged phrase, a style issue), quote the actual text in question rather than describing it abstractly - a described-but-unseen problem is hard to judge.

The three parts are not equal in time investment. As a pacing guide: roughly 40% of total effort in Prewriting, 20% in Writing (drafting is a smaller part of the work than people assume), and 40% in Postwriting. Tell the user this if they seem to be rushing toward a first draft.

Every stage within each part still exists for every document type - a cover letter needs invention and research just as much as a formal proposal does - but the *depth* of each stage adapts to the document's stakes and the fixed nature of its topic (there's no open "what should I write about" question for a proposal or cover letter the way there is for an academic essay; invention here means finding the strongest specific argument within an already-fixed topic, not finding the topic itself). Document-specific skills set that depth; this file defines the stages themselves.

## Before starting: context resets

Long documents can outlast the conversation's working context - when that happens, the chat gets summarized and fine detail (especially pasted source material like a job ad or RFP) can be lost even though the process continues. Mention this near the start of a new document: recommend the user upload source documents as files rather than pasting them inline, since files persist in the workspace regardless of what happens to the chat history, and pasted text doesn't. If a context reset does happen mid-project, don't ask the user to re-explain everything from scratch - check the stage-state marker and any saved working files first, and only ask the user to re-supply what's actually missing.

## Inviting source materials

Rhetorical Situation and Research are grounded far better in the user's actual materials than in their verbal recollection of them or in Claude's general knowledge - it's appropriate, and often the better move, to ask whether the user has something to upload. A job ad or RFP for Context/Content, a style guide or brand document for Genre, real examples of the target genre, a previous draft or prior correspondence with the same reader all sharpen the analysis directly. Ask for the specific material a given element would actually benefit from, as it comes up, rather than one blanket "send me anything relevant" request up front.

## Stage state and progress visibility

Track progress using a state marker at the top of the working file:

```
<!-- writing-process: part=prewriting, stage=rhetorical-situation, document=proposal -->
```

`document=` names whatever genre is actually being written (`proposal`, `cover-letter`, `speech`, or any other label that fits - an essay, a blog post, a eulogy) - it is not limited to genres that have their own document-specific skill.

On resuming a session, read this marker first rather than asking the user to re-explain where they left off.

Staying oriented matters as much as the marker itself. Three habits, applied throughout:
- **Teach, then ask - but calibrate to the user.** Name the part and stage the user is entering, in plain language ("the first thing we need to do is Prewriting, and Prewriting always starts with Audience"), then explain the concept itself and why it matters - what this element or technique is for, what it's called in the book's terms (primary vs. secondary audience, known-new transitions, whatever the stage's actual vocabulary is) - before asking its question. This is a companion to the book, used by students learning the method and working professionals who already know it, so the teaching has to flex rather than run one fixed script for everyone. Default to brief: a sentence naming the concept and why it matters, not a lecture. Compress further, or drop the explanation entirely and just name the element before asking, as soon as the user's own answers show fluency (precise rhetorical vocabulary, no hesitation on the concept) or they say something like "skip the explanations" - honor that immediately for the rest of the session, and only teach again if they ask. Naming the stage/element itself always stays, since that orientation is cheap and helps everyone; the depth of the explanation under it is what adapts. Never collapse two elements or two stages into a single prompt regardless of depth - explain (briefly or fully) one concept, ask about it, get an answer, then move to the next. This applies most visibly in Rhetorical Situation (eight distinct elements, each taught and asked separately - see `references/prewriting.md`) but holds everywhere: Style's transitions, Revision's HOC/LOC distinction, any named technique.
- **Preview, then remind.** When starting a new stage or section (e.g. Drafting, or a specific paragraph), briefly preview the sub-steps it will move through (e.g. "hook, then the roadmap sentence, then body paragraphs starting with topic sentences, then the close") before diving in, then periodically remind the user where they are in that sequence as they move through it.
- **Recap at key stages.** At each checkpoint (end of Prewriting, end of Writing, key points in Postwriting), give a short recap of where things stand and what's been decided so far - the rhetorical-situation summary is the model for this. Where the environment supports it, render this as something visual (a structural snapshot of the document with a "you are here" tag, a simple diagram) rather than only prose, and periodically surface the full current draft (or a wide excerpt) during Postwriting/editing so the user isn't working from memory of isolated sentences.

## Part 1: Prewriting (~40% of effort)

Full detail, prompt patterns, and the editorial-roleplay mechanic: `references/prewriting.md`.

1. **Rhetorical Situation** - analyze all eight elements before anything else: Audience, Author, Purpose, Context, Medium, Genre, Content, Strategy. Run the full treatment every time, not a shortened version - for each element, adopt the relevant expert persona ("you are an expert editor...") and interview the user step by step rather than asking generically. Offer a diagram (concentric circles, spider chart, decision tree, etc. - see reference file) where it would clarify the analysis; render it as an actual diagram when the environment supports one, otherwise as structured text.
2. **Invention** - find the strongest specific argument or angle within the document's fixed topic. Not "what should I write about" (the topic is already given) but "what's my best case." Depth is set by the document-specific skill.
3. **Research** - gather the evidence the document actually needs (client/market intelligence for a proposal, company research for a cover letter). Depth is set by the document-specific skill.

**Gate:** before moving to Writing, produce a short rhetorical situation summary, a one-line angle from Invention, and the key findings from Research. Get explicit user approval - not silence, not "looks good, keep going" without a direct check - before starting to draft.

## Part 2: Writing (~20% of effort)

Full detail: `references/writing.md`.

1. **Argumentation** - turn the approved angle into a specific, testable thesis or pitch (the Idea-to-Argument sequence), then stress-test it: run it through inductive/deductive reasoning checks, reframe it through the rhetorical appeals (ethos/pathos/logos/kairos) and synthesize the strongest version, and scan for logical fallacies.
2. **Drafting** - optionally generate a fast AI baseline draft to mark up rather than face a blank page, then draft properly at three levels: macrostructure (overall arrangement - Problem-Orientation, Classical, Toulmin, or Rogerian), mesostructure (paragraph types and structures), microstructure (sentence-level, optionally via voice-to-text for authorial voice).

**Gate:** a complete draft exists, its macrostructure is confirmed, before moving to Postwriting. If the outline/thesis turns out to be wrong mid-draft, stop and return to Part 1/Argumentation rather than improvising around it.

## Part 3: Postwriting (~40% of effort)

Full detail: `references/postwriting.md`.

1. **Style** - grammar, transitions (known-new and Janus), sentence craft (parallelism, wordiness, variation, active/passive, phrasal placement), then revise specifically for logos, pathos, and ethos.
2. **Revision and Review** - separate Higher-Order Concerns (focus, organization, thesis clarity, evidence) from Lower-Order Concerns (grammar, word choice) and address HOCs first. Run at least one cohesion technique (reverse outline, cut-and-rearrange, highlighter approach, or diagnosis/analysis/revision). Get real critique - from the user, from Claude simulating multiple distinct reviewer personas, or from an outside human reviewer - before calling it done.
3. **Front matter** - a proposal gets a one-page executive summary (situation, problem, proposed solution, the ask/benefit) by default; a cover letter does not get a separate summary, since the letter already functions as one.

**Gate:** user gives final sign-off.

## Optional: Extend

After Postwriting is signed off, ask - do not assume - whether the user wants to go further: additional front/back matter beyond the default, integrating graphics or a supporting chart, or adapting the already-finished piece into a slide deck or spoken pitch. If yes, load the `writing-process:extend` skill. This never runs by default. (If the user wants to compose a speech or presentation itself - not adapt an existing document into one - that's a document type in its own right: use `writing-process:speech` from the start of the process instead.)

## No document-specific skill matches

A document-specific skill (proposal, cover-letter, speech, ...) is an optional preset, not a requirement - this workflow is fully usable on its own for any genre that doesn't have one (an essay, a blog post, a memo, a eulogy, a grant narrative, whatever the user names). When no document-specific skill applies, use these generic defaults instead of skipping the depth question:

- **Invention:** angle-finding by default (find the strongest specific argument or angle, don't relitigate what the piece is about) - escalate to Staging the Debate only if the user's own answers during Rhetorical Situation or Invention reveal genuine ambiguity between two or more defensible directions.
- **Research:** ask the user how much the piece's actual stakes call for rather than assuming a depth - a quick internal email and a dissertation chapter warrant very different amounts of digging.
- **Macrostructure:** ask the user if they have a preference; otherwise recommend one of Problem-Orientation, Classical, Toulmin, or Rogerian based on what the Rhetorical Situation analysis surfaced (a skeptical audience points toward Rogerian, a claim that needs defending against objections points toward Classical, etc.) and say why.
- **Front matter:** only add an executive summary or similar front matter if the piece's length or audience actually calls for one (a one-page memo doesn't need a summary of itself); ask if it's unclear.

## Between documents

Each document-specific skill should set: how deep Invention and Research go, which macrostructure fits by default, whether an executive summary applies, and any format quirks. This file stays generic - a document-specific skill bends a stage's depth explicitly rather than this file special-casing any one document type.

## Noted for future extension (not yet built)

The book's roleplay device only ever assigns AI a persona; the user stays themselves. Nate flagged a genuinely good extension beyond the book: also giving the *user* a role at points in the process (e.g., answering as the hiring manager reading their own cover letter). Worth building once the core process is proven out - not yet implemented here.
