# Thrive — Health • Habits • Mindset

A self-contained Claude Code skill that turns Claude into a personal coach across three pillars:

1. **Health** — sleep, nutrition, training, recovery, biomarkers.
2. **Habits** — daily routines and behavior change that compound.
3. **Mindset** — identity, mental models, wealth psychology.

This is the answer to questions like:
- *"How do I better track my health?"*
- *"Top 10 habits for a long life?"*
- *"How do I change my mindset to become a millionaire?"*
- *"What should my morning routine look like?"*
- *"I keep failing to stick to habits — why?"*

---

## What's inside

```
thrive/
├── SKILL.md                          # Skill definition + routing logic
├── frameworks/
│   ├── health-foundations.md         # Sleep, training, nutrition, recovery, biomarkers
│   ├── longevity-habits.md           # Top 10 habits ranked by evidence × effect size
│   ├── wealth-mindset.md             # 7 identity shifts + mental models for wealth
│   └── habit-design.md               # BJ Fogg / Atomic Habits / identity-based change
├── protocols/
│   ├── morning-routine.md            # The 60-min stack (+ 15-min minimum)
│   ├── sleep-optimization.md         # 10 rules + troubleshooting
│   └── identity-shift.md             # 5-step "become a different person" protocol
└── README.md                         # This file
```

The frameworks are the *theory*. The protocols are the *do-this-today*.

---

## Sources synthesized

Pulled the strongest parts from:

- Peter Attia — *Outlive* (Zone 2, VO2max, ApoB, lifespan vs. healthspan)
- Matthew Walker — *Why We Sleep* (sleep protocol)
- Andrew Huberman — circadian light, dopamine, sauna/cold
- James Clear — *Atomic Habits* (4 laws, identity-based change)
- BJ Fogg — *Tiny Habits* (B = MAP equation)
- Naval Ravikant — *Almanack* (specific knowledge, leverage, long games)
- Morgan Housel — *Psychology of Money*
- Maxwell Maltz — *Psycho-Cybernetics* (self-image)
- Charlie Munger — mental models, inversion
- Blue Zones research (Buettner) and Harvard Study of Adult Development
- Finnish sauna cohort (Laukkanen), Cleveland Clinic VO2max study (Mandsager)

No single existing GitHub skill covered all three pillars — Thrive is the hybrid.

---

## How to use it as a Claude Code skill

### Option A — drop into your project

```bash
cp -r thrive ~/your-project/.claude/skills/thrive
```

Then in any Claude Code session in that project, just ask:
- "How should I improve my sleep?"
- "Top 10 habits for longevity?"
- "What mindset shifts do millionaires actually make?"

Claude will auto-load `SKILL.md` and the relevant framework file.

### Option B — install globally

```bash
mkdir -p ~/.claude/skills
cp -r thrive ~/.claude/skills/thrive
```

Now it's available in every Claude Code session, in any project, on this machine.

### Option C — move it to its own private repo

This folder is fully self-contained. To put it in a separate private repo:

```bash
# from inside the thrive/ folder
git init
git add .
git commit -m "Initial commit: Thrive skill"
gh repo create thrive --private --source=. --push
```

Or via the GitHub UI: create an empty private repo, then:

```bash
cd thrive
git init
git remote add origin git@github.com:YOUR_USER/thrive.git
git add . && git commit -m "Initial commit"
git push -u origin main
```

---

## Hard limits (read me)

- **Not medical advice.** Coach-level guidance only. Symptoms, medication, dosages → see a clinician.
- **No supplement prescriptions.** Categories at most.
- **Won't diagnose disease.** Will push you toward the right professional + the questions to ask them.
- **Won't moralize.** Coaches, doesn't lecture.

---

## Status

v0.1 — first complete release. Solid for the core questions. Future additions could include: nutrition deep-dives, protocols for stress/anxiety, financial-habits protocol, weekly review template, training program templates.
