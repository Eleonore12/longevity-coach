# Longevity Coach: a Claude skill

A personal longevity and well-being coach for Claude. It recommends varied training across heart-rate zones 1–5:
- zone 2 endurance
- VO2max intervals
- HIIT
- strength
- mobility, flow and yoga

It also suggests recovery and well-being practices: sauna, cold plunge, breathwork and meditation. Each recommendation builds on what you did before.

## Why this skill?

Most fitness coaching apps are built around aesthetics: losing weight or gaining muscle mass. This skill is built around a different goal: staying strong, capable and energetic for as many years as possible.

It focuses on longevity, healthspan and well-being, the qualities that best predict how well you’ll live in your 60s, 70s and beyond:

- Cardiorespiratory fitness (VO2max), one of the strongest predictors of long-term health
- A deep aerobic base built with zone 2 training
- Strength, stability and balance to stay independent and injury-free
- Mobility to keep moving freely
-Recovery and nervous-system balance through sauna, cold exposure, breathwork, meditation and sleep

The aim isn’t a number on the scale or a summer body. It’s a body and a mind that keep working well for decades.

## How it works
- **First use:** a short questionnaire of about 3 minutes, covering profile, fitness, goals, equipment, health and supplements.
- **Every use after that:**
  1. A quick check-in: did you do the last session, and how do you feel?
  2. A recommendation, either for today's session or for the week. You choose.
  3. The recommendation is saved to your training log.
- **Memory:** your profile and log are stored in **your own Notion workspace**, in a page called `Longevity Coach`. The skill itself contains no personal data, so sharing the skill never shares anyone's data.

## Requirements
- Claude with skills enabled (claude.ai, the desktop or mobile apps, or Claude Code)
- The **Notion connector** connected to Claude (Settings → Connectors → Notion). A **personal** Notion workspace is recommended: the skill stores health data, which is better kept out of an employer's workspace.

## Install
**Claude app (web, desktop or mobile):**
1. Download **[longevity-coach-skill.zip](https://github.com/Eleonore12/longevity-coach/releases/latest/download/longevity-coach-skill.zip)** from the latest release.
2. In Claude, go to Settings → Capabilities → Skills → **Upload skill**, and select the zip. Make sure "Code execution and file creation" is enabled.
3. Connect Notion (Settings → Connectors → Notion). A personal workspace is recommended.
4. Start a new chat and ask: *"What should I do today?"*

The skill syncs to all your devices, mobile included.

**Claude Code:** copy the `longevity-coach` folder into `~/.claude/skills/`.

## Use
Try asking:
- "What should I do today?"
- "Plan my week"
- "Give me a 20-min mobility flow"
- "I slept badly and I'm sore, adapt today"
- "I ran 8 km yesterday, log it"
- "Update my profile: I now have access to a sauna"
- "When should I take my magnesium given my training?"

## Disclaimer
This skill provides general fitness and well-being guidance, not medical advice. Check with a healthcare professional before starting a new exercise, sauna, cold-exposure or supplement routine, especially if you have a medical condition, are pregnant, or take medication.

## Structure
```
longevity-coach/
├── SKILL.md                    # main instructions
└── references/
    ├── onboarding.md           # first-run questionnaire
    ├── notion-storage.md       # where & how memory is stored
    ├── programming.md          # zones, weekly balance, progression, readiness
    ├── catalog.md              # activity library
    ├── exercise-links.md       # verified demo videos/articles + form cues
    └── safety.md               # contraindications & supplement guardrails
```

## License
[MIT](LICENSE) — free to use, adapt and share, with attribution. Linked videos and articles belong to their respective creators.
