---
name: speech
description: Use when the user wants to write, continue, or revise a speech, talk, or prepared oral presentation - a keynote, toast, conference talk, remarks, eulogy, or similar - composed in advance of live delivery, whether or not slides accompany it. Loads the shared writing-process:workflow skill for the Prewriting/Writing/Postwriting process and sets speech-specific depth and defaults. Triggers on phrases like "help me write a speech," "I need to prepare remarks for," "I'm giving a talk on," or "help me draft a toast." Distinct from writing-process:extend's oral-delivery section, which adapts an already-finished written document into a spoken pitch rather than composing a speech from scratch.
---

# Speech & Presentation Writing

Load `writing-process:workflow` for the process itself. This skill only sets what's specific to speeches and prepared oral presentations - depth of each stage and structural defaults - it does not redefine the stages.

A speech is composed just like any other piece of writing, however casual or high-stakes - the difference is the delivery medium, not the process. Run the full Prewriting/Writing/Postwriting sequence; let the live-delivery constraints below shape each stage rather than skipping stages because the piece will be spoken.

## Prewriting depth
- **Rhetorical Situation:** full eight-element treatment, always. Weight Medium and Context toward the live-delivery specifics that written documents don't have to answer: the actual time limit, whether the piece will be memorized, read from notes, read from slides, or delivered extemporaneously from an outline, whether visuals/slides will accompany it, and the formality of the occasion (a wedding toast and a keynote both live here, at very different registers). Get concrete numbers (minutes allotted) rather than leaving timing vague - it constrains Drafting directly.
- **Invention:** angle-finding only by default (the single strongest thing this audience needs to hear, in this moment, from this speaker) - escalate to Staging the Debate only if the occasion genuinely supports more than one defensible angle (e.g., a retirement speech that could center gratitude vs. legacy vs. what's next).
- **Research:** depth scales with the occasion - light for a toast or short remarks (a few real, specific details beat generic sentiment), heavier for a keynote or conference talk (audience's existing familiarity with the topic, what other speakers on the program are covering, current developments in the field). Ask which end of that range applies rather than assuming.

## Writing defaults
- **Macrostructure:** default to the Story Spine (situation, status quo, inciting change, consequences building on each other, resolution, new status quo) - it's the shape a listener can follow without rereading. Offer classical oration structure (exordium, narratio, partitio, confirmatio, refutatio, peroratio) as the alternative for formal, persuasive speeches that need to explicitly raise and answer objections. Ask which fits rather than defaulting silently when the occasion could plausibly go either way.
- **Mesostructure/microstructure:** draft for the ear, not the page. Favor shorter sentences and simpler subordination - a listener can't reread a tangled sentence the way a reader can. Use rhetorical devices built for spoken delivery (tricolon, anaphora, deliberate repetition) more freely than in written prose. Signpost more heavily than a written piece would need ("here's the second thing," "so where does that leave us") since the audience has no table of contents or page to flip back to.
- Run the Idea-to-Argument sequence on the central point even for a short piece (a toast, brief remarks) - a speech with a fuzzy point is worse than a written piece with one, since there's no second pass for the listener.

## Postwriting defaults
- Run the Style pass with a read-aloud rehearsal as part of it, not an afterthought: read the full draft aloud (or have the user do so) and time it against the actual limit from Rhetorical Situation. Flag anywhere the timed read runs long, sounds stilted spoken aloud, or trips on a phrase that reads fine silently but not aloud.
- **No separate executive summary.** Replace it with a single clear "big idea" stated early in the piece - spoken audiences need the point up front since they can't skim ahead the way a reader can; this is a Drafting-stage concern (it belongs in the opening), not a bolt-on front-matter section.
- Fold in a brief vocal/delivery warm-up note once the text is stable (breathing, then articulation - keep it short and practical, not a full performance-coaching module) since finishing a speech includes preparing to deliver it, not just finishing the words. If the user wants a fuller practice pass, that's `writing-process:extend`'s oral-delivery section, applied here to the piece's own text rather than to an adaptation of something else.
- If slides or other visuals will accompany the speech, note that pairing them goes through `writing-process:extend`'s slide-deck-adaptation and graphics-integration guidance rather than duplicating that here - finish the spoken text first, then adapt.

## After sign-off
Ask whether the user wants slides or supporting visuals built from the finished speech (`writing-process:extend`'s slide-deck-adaptation flow) - common enough for keynotes and conference talks to be worth asking about directly. A vocal warm-up pass, if not already done during Postwriting, is also worth offering here if a live delivery is coming up soon.
