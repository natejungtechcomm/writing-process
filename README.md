# writing-process

A Claude Cowork / Claude Code plugin that turns writing any document - or preparing any spoken piece - into a staged, collaborative workflow instead of a single generate-and-hope prompt, no matter how big or small the piece is. It works out of the box for any genre (a quick essay, a blog post, a memo, a dissertation chapter, a speech); proposal, cover-letter, and speech are just the genres with their own tuned presets so far.

This plugin is a concrete implementation of the argument made in **"The Process of Generative AI Writing" by Nathan A. Jung**: that good AI-assisted writing isn't a single prompt that produces a finished document, but a staged process with real checkpoints - the same discipline a careful human editor would apply, made explicit and repeatable. Where the book makes that argument, this plugin makes it executable.

## What it does

Every document goes through the same three-part process the book teaches, enforced by the shared `workflow` skill:

1. **Prewriting** (~40% of effort) - rhetorical situation analysis across all eight elements (audience, author, purpose, context, medium, genre, content, strategy), invention (finding the strongest angle within an already-fixed topic), and research.
2. **Writing** (~20% of effort) - turning that angle into a specific, stress-tested thesis or pitch, then drafting at three levels: macrostructure (overall arrangement), mesostructure (paragraphs), microstructure (sentences).
3. **Postwriting** (~40% of effort) - style revision (grammar, transitions, sentence craft, rhetorical appeals), structured review (higher-order concerns before lower-order ones, real critique from at least one source), and front matter (an executive summary, for documents that need one).

Each part has an explicit checkpoint - Claude does not advance without your approval. That's the mechanism that prevents the two common failure modes of AI-generated writing: a generic full draft dumped in one shot, or prose that reads fine sentence-by-sentence but is structurally wrong for its audience. An optional `extend` skill (graphics, slide decks, posters, oral delivery practice) is available afterward but never runs unless you ask for it.

## Document types

Any genre works with the shared `workflow` skill on its own - it has sensible generic defaults for invention, research, and structure built in. A few genres have their own tuned preset skill on top of that:

- `proposal` - business/project proposals (full rhetorical and research depth, Problem-Orientation structure by default, executive summary required)
- `cover-letter` - job application cover letters (lighter research, condensed structure, no separate summary)
- `speech` - speeches, talks, and prepared oral presentations - keynotes, toasts, conference talks, remarks (live-delivery-specific rhetorical situation, Story Spine or classical oration structure, read-aloud/timing check instead of an executive summary)

New document types can be added as additional skills; they only need to set the depth and structural defaults for that document, since the three-part process itself is shared. Adapting an *already-finished* document into a spoken pitch or slide deck (rather than composing the speech itself from scratch) is handled by the optional `extend` skill instead.

## Installing

Install directly from this repo with Claude Code:

```
claude plugin install natejungtechcomm/writing-process
```

Or, once it's listed on Anthropic's plugin directory, install it from **claude.com/plugins** in Claude Cowork.

## Author & license

Written by Nathan A. Jung, author of *The Process of Generative AI Writing*.

MIT licensed - see [LICENSE](./LICENSE).
