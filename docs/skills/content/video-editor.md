# Video Editor Dot Skill

Edit compelling videos with narrative structure, pacing, cuts, sound design, and color workflow.

## Skill Metadata

* Identifier: `dots-skill-video-editor`
* Category: Content
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Video Editor specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
```

## Governance and Permission Mapping

| Action Phase | Operation | Assigned Permission Mode |
| :--- | :--- | :--- |
| Ingestion | Scanning feeds, reading logs, and inspecting state | Autonomous Execution |
| Processing | Running local transforms, filtering, and drafting | Autonomous Execution |
| Verification | Compiling candidate recommendations and reports | Prompt-Initiated Execution |
| Modification | Committing changes, dispatching messages, or updating records | Supervised Execution |
| Destruction | Deleting records, purging branches, or revoking access | User Handoff |

## Operational Instructions

## Overview

Editing is where footage becomes story: the selection, arrangement, and rhythm of shots determine
whether viewers watch to the end or click away in ten seconds. This skill covers the creative
editing craft - narrative structure, pacing, cutting technique, sound design, and color - plus the
project organization that keeps complex edits manageable.

## When to use

- Editing YouTube videos, shorts, documentaries, or marketing videos

- Structuring raw footage into a compelling narrative

- Improving pacing and retention in existing edits

- Learning cutting technique, transitions, and sound design

- Organizing large editing projects and media

## Core concepts

- - **Story first, software second.** Before touching the timeline: what's the video about in one
 sentence? What's the hook (first 15 seconds), the turns, the payoff? Edit to the story, not to the
 footage you happen to like.
- - **The hook is everything.** First 5-15 seconds decide retention: state the payoff, pose the
 question, or show the most compelling moment. No logos, no "hey guys welcome back," no
 throat-clearing.
- - **Cutting on action and emotion.** Cut during movement to hide the cut; cut to reactions to land
 emotion. J-cuts (audio leads video) and L-cuts (video leads audio) create fluid, professional flow
 - hard cuts on silence feel amateur.
- - **Pacing = retention.** Vary rhythm: fast montages for energy, held shots for weight. Cut
 ruthlessly - every second must earn its place. If you're bored watching your own edit, the
 audience left minutes ago.
- - **Sound design is 50% of the edit.** Music (licensed, leveled under dialogue), SFX (whooshes,
 impacts, ambience - subtle layers sell reality), and clean dialogue. Mute the video: does the
 audio alone tell a story?
- - **Color: correct then grade.** Correction (fix white balance, exposure, match shots) before
 grading (creative look). Consistent color across shots is more important than a fancy LUT - 
 mismatched shots scream amateur.

## Practical workflow

1. 1. **Ingest and organize.** Folder structure (footage/audio/graphics/exports), descriptive bin
 names, sync multi-cam/audio, mark selects. An hour of organization saves ten of hunting.
2. 2. **Build the radio edit.** Cut the story using audio first (dialogue/voiceover) - if it works
 as audio-only, the visuals will support it. Arrange selects into the narrative arc: hook setup
 development payoff.
3. 3. **Rough cut.** Lay visuals to the radio edit. Don't polish - focus on structure and pacing.
 Watch through: does the story flow? Fix structure now; it's 10x harder later.
4. 4. **Refine the cut.** Tighten every edit point (trim dead air, cut on action), add B-roll to
 cover cuts and illustrate points, pace to the music's energy. The 10% trim: cut your favorite
 shot if it doesn't serve the story.
5. 5. **Sound design pass.** Level dialogue consistently, add music (duck under speech), layer SFX
 and ambience, check the mix on headphones and laptop speakers. Normalize loudness to platform
 spec.
6. 6. **Color pass.** Correct all shots (exposure, WB, match), then apply the creative grade
 consistently. Check skin tones - the fastest grade quality test.
7. 7. **Graphics and titles.** Lower thirds, titles, captions - restrained and on-brand. Burned-in
 captions for social (85% watch muted). Keep text readable at phone size.
8. 8. **Export and review.** Export per delivery spec, watch the full export on the target device,
 get fresh eyes on it, fix, and re-export. Never ship the first export unwatched.

## Common pitfalls

- **Slow openings.** 60 seconds of intro before the content. The hook goes first - always.

- - **Falling in love with footage.** Keeping a beautiful shot that breaks pacing or story. Kill
 your darlings; the audience never saw what you cut.
- - **Transition abuse.** Star wipes, 3D flips, and spin transitions. Cut or dissolve 95% of the
 time - fancy transitions call attention to the edit instead of the story.
- - **Neglecting audio.** Great visuals with peaking, echoing, or inconsistent audio. Fix audio
 before adding a single effect.
- - **No B-roll discipline.** Talking head for 10 straight minutes. B-roll covers cuts, illustrates
 points, and resets attention - plan for it in the shoot, not the edit.
- - **Skipping the fresh-eyes review.** Editing so long you can't see it anymore. A new viewer
 catches pacing dead spots and confusing moments you've gone blind to.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
