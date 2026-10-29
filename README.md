# The race-week coach panel

Four Claude agents, each in its own terminal pane, each given the same athlete brief and data. Each one writes a review in the same four sections, so you can read them side by side and see where they agree.

| File | Coach | Owns |
|---|---|---|
| `run-coach.md` | Running coach | race goal, pacing, the sessions left before race day |
| `physiologist.md` | Exercise physiologist | heart-rate zones, thresholds, recovery signals |
| `strength-coach.md` | Strength & conditioning coach | lifting around the run plan, injury risk |
| `dietitian.md` | Sports dietitian | daily intake, carb load, race-day fuelling, caffeine |
| `athlete-brief.md` | (you fill this in) | the facts every coach reads |

## How to run it
1. Fill in `athlete-brief.md`. Paste real data: per-km splits, heart rate, sleep, resting HR, HRV, recent sessions. Whole-run averages hide the story. Per-km splits are what changed the panel's verdict.
2. Open four Claude sessions. Give each one its coach file plus the brief: "Read <coach>.md and athlete-brief.md, then write your review."
3. Read the four reviews together. Where they agree is your plan. Where they disagree, ask the owner of that topic.
4. When something new comes in (a key workout, a race-date change), add it to the brief and ask each coach for a v2 that starts with "what I got wrong".

Training plan itself: [claude-coach](https://github.com/felixrieseberg/claude-coach) by Felix Rieseberg (MIT). These coach files are the review layer on top of a plan, not a replacement for one.

Not medical advice. Anything involving pain, injury or a health condition goes to a real professional.
