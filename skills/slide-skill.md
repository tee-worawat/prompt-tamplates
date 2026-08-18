---
name: generic-slide-creator
description: Create structured presentation slides from user goals and source materials. Use when the user asks to create slides, a deck, lecture slides, or presentation HTML. Starts with a comprehensive intake questionnaire, then builds a single lecture-slides.html output by default.
disable-model-invocation: true
---

# Generic Slide Creator

## Purpose

Produce clear, visually structured slides for typical presentations (teaching, demos, business updates, project walkthroughs) with a repeatable intake-first workflow.

Default output: one HTML deck file named `lecture-slides.html`.

## Required Workflow

Follow this sequence every time:

1. Gather requirements with a structured intake.
2. Confirm available source material and constraints.
3. Draft slide architecture (sections and narrative arc).
4. Generate the deck.
5. Refine readability and presenter usability.
6. Validate flow against the original objective.

## Intake Questions (Ask Before Building)

Use `AskQuestion` for multiple-choice decisions. Ask follow-up free text only when needed.

Collect at minimum:

1. **Presentation objective**
   - Teach
   - Persuade
   - Report status
   - Demo workflow
   - Other
2. **Audience**
   - Beginners
   - Mixed
   - Experts
   - Executives/non-technical
3. **Mood and tone**
   - Academic
   - Professional
   - Conversational
   - Energetic
   - Formal
4. **Knowledge base availability**
   - Full resource set available (docs/notebooks/transcripts)
   - Partial resource set
   - No source material yet
5. **Slide constraints**
   - Target duration
   - Slide count range
   - Visual density (light/medium/dense)
6. **Output format**
   - Single `lecture-slides.html` (default)
   - Other format (only if user requests)
7. **Brand/style constraints**
   - Existing theme/colors/fonts
   - No brand constraints
8. **Presenter support**
   - Speaker-friendly prompts and demo cues
   - Slides-only

## If Knowledge Base Is Missing

If the user does not provide enough material:

- Ask for source assets (docs, transcript, notebook, links, or outline).
- Offer to build from a short brief, but explicitly mark assumptions.
- Keep claims generic until source-backed details are provided.

## Slide Design Rules

1. One core idea per slide.
2. Keep hierarchy obvious: title -> concept -> evidence/example.
3. Use examples early, not only at the end.
4. Favor scanability over paragraphs.
5. Keep typography projector-friendly.
6. Use visuals where they reduce cognitive load.
7. Maintain consistent semantic components (concept box, example box, demo box).

## Standard Deck Structure

Adapt as needed, but start from this:

1. Title + outcome
2. Agenda / map
3. Core concepts (progressive)
4. Worked examples
5. Operational workflow / implementation
6. Risks and anti-patterns
7. Recap and next actions

## Generation Checklist

Before finalizing:

- Objective is answered by the final slide.
- Tone matches requested mood.
- Audience level is respected.
- Every major section has at least one concrete example.
- Claims map to available source material.
- Visual balance is acceptable at presentation zoom.

## Suggested AskQuestion Set

Use this exact structure when possible:

- Objective
- Audience level
- Tone
- Source completeness
- Duration
- Preferred depth
- Need speaker notes/demo cues

## Output Contract

Unless user asks otherwise:

- Create/update `lecture-slides.html`.
- Use a light, readable theme.
- Ensure keyboard navigation works.
- Include presenter-friendly spacing and readable font sizes.

## Example Invocation

User asks: "Create slides for this lesson."

Agent should:

1. Run intake questions first.
2. Read provided materials.
3. Build `lecture-slides.html`.
4. Iterate on order, emphasis, and examples based on feedback.
