# AI Cartoon Script Generator

Use this prompt to run the full AI cartoon production pipeline in a single session.  
For the complete multi-stage workflow, see `workflows/ai-cartoon-workflow.md`.

## Quick-Start Prompt

```
You are a cinematic scriptwriter and AI video director.

I want to create a short animated video. Here is my story concept:

**Title:** [your title]
**Genre:** [cartoon / cinematic / horror / comedy / etc.]
**Tone:** [playful / dark / inspirational / dramatic]
**Duration:** [30s / 60s / 90s]
**Main character:** [name + one-line description]
**Setting:** [where and when]
**Core conflict:** [what the character wants and what stops them]
**Resolution:** [how it ends]
**Art style:** [e.g. 3D Pixar-style, hand-drawn cartoon, Studio Ghibli, cinematic live-action]

Run this full production pipeline and give me all 4 outputs:

---

OUTPUT 1 — CINEMATIC SCRIPT
Write the full script as a series of beats. For each beat:
- NARRATION/DIALOGUE: exact words
- VISUAL: what the viewer sees, camera angle, action
- EMOTION: the feeling this moment creates

---

OUTPUT 2 — SCENE BREAKDOWN
Split the script into individual scenes (3-8 seconds each). For each scene:
- Duration
- Characters on screen
- Setting/background
- Action
- Camera angle and movement
- Lighting
- Color palette
- Transition out

---

OUTPUT 3 — SEEDANCE 2.0 PROMPTS
For each scene, write an optimized video generation prompt:
[Subject + action], [setting], [lighting], [camera movement], [art style], [color grade], highly detailed, 4K, smooth motion, cinematic

Keep each prompt under 75 words. Lead with the subject. Include the art style in every prompt for visual consistency.

---

OUTPUT 4 — PREVIEW STORYBOARD
Write a 200-word director's preview describing the finished film playing in real time. Make the reader feel the film.
```

## Notes

- Fill in the bracketed fields before running the prompt
- For longer films (3+ min), run Stage 2 and Stage 3 separately using the full workflow
- Copy your art style tag exactly into every Scene Prompt — consistency breaks without it
- Generate Scene 1 in Seedance first, lock the visual style, then proceed with remaining scenes
