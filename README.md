# writing-process

A Claude Cowork / Claude Code plugin that turns writing any document - or preparing any spoken piece or other type of communication - into a staged, collaborative workflow instead of a single-shot prompt, no matter how big or small the piece is. It works out of the box for any genre (a quick essay, a blog post, a memo, a dissertation chapter, a speech), and at present has tuned presets for proposals, cover-letters, and speeches, with more to come.

This plugin is a concrete implementation of the argument made in **"The Process of Generative AI Writing" by Nathan A. Jung**: that good AI-assisted writing entails a staged process with checkpoints, using the same discipline a careful human editor would apply. It is calibrated to help writers exercise their agency in the writing process and use AI as a general purpose tool to assist their project management.

## What it does

Every document goes through the same three-part process the book teaches:

1. **Prewriting** (~40% of effort) - rhetorical situation analysis across all eight elements (audience, author, purpose, context, medium, genre, content, strategy), invention (finding the strongest angle within an already-fixed topic), and research.
2. **Writing** (~20% of effort) - developing a specific thesis or pitch, then drafting at three levels: macrostructure (overall arrangement), mesostructure (paragraphs), microstructure (sentences).
3. **Postwriting** (~40% of effort) - style revision (grammar, transitions, sentence craft, rhetorical appeals), structured review (higher-order concerns before lower-order ones, real critique from at least one source), and front matter (for documents that need one).

Each part has an explicit checkpoint - Claude does not advance without your approval. This design intends to prevent the two common failures of AI-generated writing: a generic full draft dumped in one shot, or prose that reads fine sentence-by-sentence but is structurally wrong for its audience. An optional `extend` skill (graphics, slide decks, posters, oral delivery practice) is available afterward but never runs unless you ask for it.

## Document types

Any genre works with the shared `workflow` skill on its own - it has sensible generic defaults for invention, research, and structure built in. A few genres have their own tuned preset skill on top of that:

1. Proposal - research-based project proposals for business, engineering, etc.

2. Cover-letter - traditional job application cover letters

3. Speech - keynotes, conference talks, technical presentations, etc.

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
