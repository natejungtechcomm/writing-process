---
name: proposal
description: Use when the user wants to write, continue, or revise a business or project proposal. Loads the shared writing-process:workflow skill for the Prewriting/Writing/Postwriting process and sets proposal-specific depth and defaults. Triggers on phrases like "write a proposal," "draft a proposal for [client/project]," or "help me pitch this."
---

# Proposal Writing

Load `writing-process:workflow` for the process itself. This skill only sets what's specific to proposals - depth of each stage and structural defaults - it does not redefine the stages.

## Prewriting depth
- **Rhetorical Situation:** full eight-element treatment, always - a proposal's stakes justify it.
- **Invention:** run angle-finding plus Staging the Debate by default - a proposal usually has more than one defensible strategic framing (cost angle vs. speed angle vs. risk angle), and it's worth weighing them explicitly rather than committing to the first one.
- **Research:** substantial by default - client/organization situation, comparable precedent projects, competitive landscape, and any cost-benefit data the pitch will lean on. Flag anything AI-suggested that needs the user to verify it's real before it goes in the document.

## Writing defaults
- **Macrostructure:** default to Problem-Orientation (Situation -> Problem -> Solution -> Evaluation) - it's the native shape of a proposal. Switch to Rogerian instead when the reader is likely to start skeptical of the whole premise (e.g., proposing a change to something they already own or built).
- Run the full Argumentation sequence (Idea-to-Argument, then reasoning/appeals/fallacy testing) - a proposal's central pitch is exactly the kind of claim that benefits from stress-testing before it's built out into prose.

## Postwriting defaults
- Run the full Style and Revision/Review passes.
- **Executive summary: required.** One page, in this order: situation, problem, proposed solution, the ask/benefit. Write it last, after the full document is stable, and keep it readable by someone who will only read this page.
- If the proposal responds to an RFP or brief with explicit stated requirements, check the draft against the requirements checklist built during Research (see `writing-process:workflow`'s postwriting reference) as an explicit Higher-Order Concern - proposals are marked against exactly this kind of checklist more often than cover letters are, so treat it as load-bearing, not optional.
- Peer review: if the proposal is going to a committee or a skeptical stakeholder, simulating multiple distinct reviewer personas (per `references/postwriting.md`) before it goes out is worth the extra pass.

## After sign-off
Ask whether the user wants anything from `writing-process:extend` - a supporting chart or cost-comparison table is common enough for proposals to be worth asking about directly, rather than waiting for the user to think of it.
