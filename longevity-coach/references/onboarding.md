# Onboarding questionnaire (first run only)

Send the whole questionnaire in **one message** so the user can answer in one go. Keep the framing short: one sentence on why you're asking, then the questions. Tell them they can answer loosely ("about 60 kg", "no idea") and skip anything.

Suggested message:

---

Welcome! Before your first recommendation, I need a quick picture of you so I can personalise everything from now on. It takes about 3 minutes. Answer in any format, and skip anything you don't know or don't want to share. Your answers are saved only in **your own Notion**, in a page called "Longevity Coach". (Tip: if the Notion connected to Claude is your company workspace, consider connecting a personal one instead, since this is health data.)

**1 · About you**
1. Age, sex, height, weight

**2 · Fitness**

2. How would you rate your current level: beginner, intermediate or advanced?
3. What do you currently do, and how often per week? (e.g. "run 2×, yoga 1×")
4. Do you know your VO2max, resting heart rate or max heart rate? If so, where do they come from (watch, lab test)?
5. Do you train with a heart-rate monitor or a watch? Which one?

**3 · Goals & constraints**

6. Your top 2–3 priorities: endurance, strength, mobility, stress, sleep, body composition, energy, something else?
7. Time available: how many sessions per week, and how many minutes per session? Any preferred days?
8. What do you have access to: gym, home equipment (which), pool, sauna, cold plunge or cold shower, outdoor space?
9. Any injuries, recurring pain, or medical conditions I should know about? (e.g. heart condition, high blood pressure, pregnancy, joint issues)
10. Do you take any medication that affects heart rate, such as beta-blockers?

**4 · Supplements**

11. Do you take supplements? If yes, list each one with the dose, how often or which days, and the time of day you take it.

---

## After the answers

1. **Missing data is fine.** Fill gaps with sensible defaults and note them in the Profile (for example, an estimated max HR). Ask a follow-up only if something critical for safety is ambiguous, such as "heart thing" with no detail.
2. **Level sanity check.** Self-rated level is often off. Cross-check it with their actual weekly activity. If they say "intermediate" but do one walk a week, program as beginner for the first 2–3 weeks and say so kindly.
3. **Safety screen.** Apply `safety.md`. Record any restrictions in "Health & safety → Safety notes".
4. **Zones.** Compute them as described in `programming.md`.
5. **Program state.** Initialise the Training Log:
   - Phase: `base` for beginners or anyone returning from a break. `build` for intermediate or advanced users who are already consistent.
   - Week in block: 1 of 4.
   - Zone 2, VO2max and strength tracks: set starting points from `programming.md` → Progression tracks, matched to their level.
6. **Supplements.** Note anything relevant for training timing (caffeine, creatine, magnesium, iron, high-dose antioxidants…). Mention 1–2 useful timing observations in the summary. Don't lecture.
7. **Confirm.** Show a short summary: the key profile facts, the zone table, and the safety notes. Tell them they can say "update my profile" anytime.
