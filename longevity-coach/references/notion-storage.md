# Notion storage

All memory lives in the **user's own Notion workspace**, via whatever Notion connector tools are available in the session (search, fetch, create pages, update page). Nothing is stored in the skill itself, so the skill can be shared without sharing anyone's data.

Plain pages are used (rather than a Notion database) because a page can be read in one fetch and edited reliably by every Notion connector, on every surface including mobile. Markdown tables still render nicely in Notion for the user.

## Pages

```
📄 Longevity Coach                       (parent page, top level of the workspace)
├── 📄 Longevity Coach — Profile
└── 📄 Longevity Coach — Training Log
```

The exact titles matter: they're how the skill finds its memory next time.

### Finding the pages
1. Search for `Longevity Coach — Profile` (and `Longevity Coach — Training Log`).
2. Only accept results whose title matches exactly. Search can return loose matches.
3. If there are duplicates, use the most recently edited one and mention it to the user so they can delete the extras.
4. If the Profile exists but the Training Log doesn't, create the Training Log under the same parent. Don't redo onboarding.

### Creating the pages (first run)
1. Create the parent page `Longevity Coach` at the top level of the workspace. The page body should say: "Managed by the longevity-coach skill. Feel free to read and edit; keep the page titles unchanged."
2. Create the two child pages from the templates below.

## Profile template

```markdown
_Last updated: YYYY-MM-DD_

## About
- Age: 
- Sex: 
- Height: 
- Weight: 

## Fitness
- Level: beginner | intermediate | advanced
- Current activities & weekly frequency: 
- VO2max: (value + source, e.g. "Garmin estimate", "lab test"), or unknown
- Resting HR: 
- Max HR: (measured or estimated, with formula)
- HR monitor / watch: yes (which) | no

## Heart-rate zones
| Zone | bpm | Feel |
|---|---|---|
| Z1 | | |
| Z2 | | |
| Z3 | | |
| Z4 | | |
| Z5 | | |
_Method: ..._

## Goals & constraints
- Priorities: 
- Availability: X sessions/week, Y min/session (and any preferred days)
- Access & equipment: 
- Preferences / dislikes: 

## Health & safety
- Injuries / pain: 
- Medical conditions: 
- HR-affecting medication: yes/no
- Safety notes: (what was flagged at onboarding and what is restricted)

## Supplements
| Supplement | Dose (as declared) | Frequency / days | Time of day |
|---|---|---|---|
```

## Training Log template

```markdown
## Program state
- Current phase: base | build | maintain   (started YYYY-MM-DD)
- Week in block: 1 of 4   (week 4 = deload)
- Zone 2 track: typical session length XX min, weekly total ~XX min
- VO2max track: current protocol (e.g. "6×1′/1′", "4×3′", "4×4′")
- Strength track: split + current key loads/levels (e.g. "goblet squat 16 kg 3×10")
- Mobility focus: 
- Well-being habits: (e.g. "sauna 2×/wk", "cold plunge 1×/wk", "10-min meditation daily goal")
- Notes: (niggles, travel, life context)

## Recent log (last 28 days)
| Date | Activity | Category | Zone | Duration | Status | RPE | Readiness | Notes |
|---|---|---|---|---|---|---|---|---|

## History summary (older than 28 days)
- 
```

**Column conventions**
- **Category:** `endurance`, `vo2max`, `hiit`, `strength`, `mobility`, `yoga/flow`, `sport`, `recovery`, `well-being`
- **Zone:** Z1–Z5 for cardio. Use `—` for strength, mobility and well-being.
- **Status:** `planned` (from a week plan), `recommended`, `done`, `modified`, `skipped`, `unknown`, `self-logged` (user did it on their own)
- **Readiness:** energy, body freshness and sleep, written as `E4 B2 Sl3`. Each scale runs 1–5 and 5 is always good, so B5 means no soreness. Record it on the row of the day it was reported, usually today's session, and only when known.

## Writing rules
- **Table syntax.** The pipe tables in this file only show the structure. When writing to Notion, use whatever table syntax the connector expects. The official Notion connector uses Notion-flavored `<table header-row="true"><tr><td>…</td></tr></table>` markup; pipe tables may come out as plain text. If unsure, check the connector's markdown documentation once before the first write.
- **Privacy.** Create the parent page as a private page, e.g. the connector's private/draft creation mode. Never put it in a shared or team space.
- Update the page in place: replace the whole page content with the edited version, or use the connector's targeted edit if it has one. Never create a new page per session.
- Keep the log in chronological order, oldest first.
- **Roll-up:** when entries are older than 28 days, remove them from the table. Add a line per week to "History summary", for example: `2026-W38: 5 sessions (Z2 150 min, 2× strength, 1× 4×4, 2× sauna), avg RPE 6, skipped 1`.
- Update `_Last updated_` on the Profile whenever it changes.
- When the user updates their profile ("I'm 62 kg now", "new knee pain"), edit only the relevant field. Recompute zones if age, max HR or resting HR changed.
- If a write fails, tell the user in one line and show the entry so nothing is lost. Don't retry endlessly.

## Data deletion
If the user asks to delete their data, tell them to delete the `Longevity Coach` page in Notion and then empty it from Notion's trash. That page holds all the data, and the user should do the permanent deletion themselves.
