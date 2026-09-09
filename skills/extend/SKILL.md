---
name: extend
description: Optional, opt-in only - use after a document from writing-process:workflow has already been signed off, and only when the user explicitly asks to extend it further (e.g. "turn this into a pitch deck," "I need a chart for this proposal," "help me practice presenting this," "add a table of contents"). Never load automatically at the end of a document - the core workflow only offers this, it does not run it.
---

# Extending the Process

Adapted from the "Extending the Process" chapter of "The Process of Generative AI Writing." Everything here is additive to an already-finished document - none of it is part of the default path.

Ask which of the following the user wants; do not run more than what's requested.

## Additional front/back matter
Beyond the default executive summary (proposals only): a table of contents (only worth generating for long/formal documents - offer to skip it otherwise), an abstract-style short summary if the document will circulate to readers who want a condensed version, or a glossary if it uses terms a reader might not know. Generate a draft, then have the user confirm it actually reflects the finished document's structure (AI-generated TOCs/indexes are unreliable enough that they need a human check against the real document, not just the outline).

## Graphics integration
When the document would benefit from a chart, table, or diagram (comparisons, cost/benefit data, a process sequence, spatial relationships):
1. Identify what specific relationship the graphic should show, and whether that relationship is genuinely better shown visually than in prose.
2. Recommend a graphic type suited to that relationship (bar chart for comparison, flowchart for sequence, table for structured data) rather than defaulting to one type.
3. Check placement - does the graphic appear after the text that introduces it, not before?
4. Write or tighten the caption and the surrounding in-text reference so the graphic is explained, not just dropped in.
5. If the user is building the graphic in an external tool (Excel, Canva, etc.), help draft the labels/values/layout rather than attempting to generate a precise image directly - AI image generation is not reliable for data-accurate charts or technical diagrams.

## Slide deck adaptation
Use the Assertion-Evidence model, not a bullet-dump of the source document:
1. Extract 5-7 core sequential assertions from the finished document - each a complete sentence stating a claim (these become slide headers), not a topic fragment.
2. For each assertion, propose one strong piece of visual evidence (chart, image, table) rather than restating the assertion in bullets.
3. Write short speaker notes per slide - what to say aloud, not another paragraph of text.
4. Check the sequence builds logically and no slide is overloaded.

## Poster adaptation
Split into standard sections (Title, Introduction/Problem, Methods or Approach, Results or Offer, Conclusion), draft 2-3 bullet points per section, and propose a visually balanced layout - posters are read by a wandering crowd making eye-contact-level judgments, not read start to finish, so prioritize scannability over completeness.

## Oral delivery / pitch practice
This section is for adapting an already-finished written document into a spoken pitch after the fact. To compose a speech or presentation as the primary piece from the start, use `writing-process:speech` instead - it runs the full process (including its own Story Spine / oration-structure choice) rather than compressing a finished document down.

1. Translate the document into the Story Spine structure (a classic beat sequence: a situation, a status quo, an inciting change, consequences building on each other, a resolution, a new status quo) at whatever length fits the occasion.
2. Adjust for the actual audience, time limit, and their existing familiarity with the topic.
3. Offer a short vocal/delivery warm-up sequence if the user is nervous about live delivery (breathing, then articulation) - keep this brief and practical, not a full performance-coaching module.
