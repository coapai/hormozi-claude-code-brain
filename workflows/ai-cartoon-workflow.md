# AI Cartoon Workflow

A structured production pipeline for creating animated AI videos.  
**Pipeline:** Story → Script → Scene Split → Video Prompts → Preview

---

## Overview

This workflow turns a raw story idea into production-ready scene prompts for Seedance 2.0 (or any AI video generator). Each stage has a clear input, output, and Claude prompt to run.

Use it for:
- AI cartoons
- Short animated stories
- Cinematic reels
- Character scenes
- Story-driven marketing videos

---

## Stage 1: Story Input

**Goal:** Define the story before touching any AI tool.

Fill in this brief:

```
Title: [Your story title]
Genre: [cartoon / cinematic / horror / comedy / etc.]
Tone: [playful / dark / inspirational / dramatic / etc.]
Duration target: [30s / 60s / 90s / 3 min]
Main character: [Name + 1-line description]
Setting: [Where and when]
Core conflict: [What does the character want? What stops them?]
Resolution: [How does it end?]
Intended platform: [YouTube / Instagram Reels / TikTok / etc.]
```

---

## Stage 2: Script Generator

**Goal:** Turn the story brief into a full cinematic script with narration and visual direction.

### Prompt

```
You are a cinematic scriptwriter specializing in short animated films.

Here is my story brief:

Title: [title]
Genre: [genre]
Tone: [tone]
Duration: [duration]
Main character: [character]
Setting: [setting]
Core conflict: [conflict]
Resolution: [resolution]

Write a full script for this animated short. For each beat include:
- NARRATION or DIALOGUE (exact words spoken or on-screen text)
- VISUAL DIRECTION (what the viewer sees — camera angle, action, atmosphere)
- EMOTIONAL BEAT (the feeling this moment should create)

Format each beat like this:

---
[BEAT 1 - OPENING]
NARRATION: "..."
VISUAL: ...
EMOTION: ...
---

Keep the total script tight for the target duration. Make every line earn its place.
```

---

## Stage 3: Scene Splitter

**Goal:** Break the script into individual scenes ready for video generation, one at a time.

### Prompt

```
Take this script and split it into individual scenes for AI video generation.

[PASTE YOUR SCRIPT HERE]

For each scene output:

SCENE [number]:
- Duration: [seconds]
- Characters on screen: [list]
- Setting/background: [description]
- Action: [what physically happens]
- Camera: [angle + movement — e.g. slow push in, wide establishing, close up, aerial]
- Lighting: [e.g. golden hour, neon glow, overcast, moonlit]
- Color palette: [3-4 colors that define the mood]
- Transition out: [cut / fade / dissolve / smash cut]

Aim for scenes of 3-8 seconds each for AI video generation. Split longer beats into multiple scenes.
```

---

## Stage 4: Video Generation Prompts (Seedance 2.0)

**Goal:** Convert each scene into an optimized prompt for Seedance 2.0.

### Prompt

```
Convert each of these scenes into an optimized video generation prompt for Seedance 2.0.

[PASTE SCENE LIST HERE]

For each scene, write a single video prompt using this structure:

[Subject + action], [setting + environment], [lighting + atmosphere], [camera movement + angle], [art style], [color grade], [quality tags]

Rules:
- Lead with the subject and what they're doing
- Be specific about camera movement (slow zoom in / tracking shot / static wide / aerial pullback)
- Include art style: e.g. "3D Pixar-style animation", "hand-drawn cartoon", "cinematic live-action", "Studio Ghibli watercolor"
- End with quality tags: "highly detailed, 4K, smooth motion, cinematic"
- Keep each prompt under 75 words
- Do NOT use negative prompts — Seedance handles that separately

Output format:

SCENE [number] PROMPT:
[The prompt]

SCENE [number] NEGATIVE PROMPT (optional):
[Only if there's something specific to exclude]
```

---

## Stage 5: Preview Storyboard

**Goal:** Get a text-based storyboard to review the full film before generating video.

### Prompt

```
Based on these scenes and prompts, write a text storyboard — a director's preview of the finished film.

[PASTE SCENES + PROMPTS HERE]

Write it as if you are describing the finished video playing in real time:

"The film opens on [description]... The camera slowly [movement]... We see [character] [action]... The music swells as [event]..."

Include:
- What the viewer sees at each moment
- The emotional arc from opening to close
- How transitions feel
- What makes this film memorable

Keep it under 300 words. Write it like a pitch — make the reader feel the film.
```

---

## Full Pipeline Checklist

| Stage | Input | Output | Status |
|-------|-------|--------|--------|
| 1. Story Brief | Idea in your head | Filled brief template | [ ] |
| 2. Script | Story brief | Full cinematic script | [ ] |
| 3. Scene Split | Script | Scene-by-scene breakdown | [ ] |
| 4. Video Prompts | Scene breakdown | Seedance 2.0 prompts | [ ] |
| 5. Preview | All of the above | Text storyboard | [ ] |

---

## Tips for Better Results

**On scripts:** Shorter is better. A 60-second film needs ~8-12 beats. Cut anything that doesn't move the story or emotion forward.

**On scenes:** 4-6 seconds per scene is the sweet spot for AI video generation. Longer scenes lose coherence.

**On prompts:** Lead with the subject, end with quality tags. The camera movement instruction is the most important variable for cinematic feel.

**On iteration:** Run Stage 4 one scene at a time in Seedance. Generate 2-3 variations per scene and pick the best. Don't generate all scenes at once until you've locked in the visual style with Scene 1.

**On consistency:** Use the same character description and art style tag in every single prompt. Copy-paste it exactly — even one word difference will break character consistency.
