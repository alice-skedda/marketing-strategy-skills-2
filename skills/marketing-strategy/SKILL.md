---
name: marketing-strategy
description: Show the status of the marketing strategy document — what sections are complete and what to work on next. Run this to check progress or get guidance on the next exercise.
allowed-tools: [Read, Write, Glob]
---

# Marketing Strategy Tracker

The marketing strategy document is looked up in this order:
1. `./marketing-strategy.md` — in the current working directory (recommended for teams: commit this file to your repo)
2. `~/Desktop/marketing-strategy.md` — fallback for personal use

## Instructions

When this skill is invoked:

1. Check if `./marketing-strategy.md` exists in the current working directory. If yes, use that.
2. Otherwise, fall back to `~/Desktop/marketing-strategy.md`.
3. If neither exists, create `./marketing-strategy.md` with a title line `# Marketing Strategy` and report all sections as incomplete.
4. Scan the file content for each of the 8 section headers listed below.
5. Display the progress dashboard.
6. Guide the user to the next incomplete exercise.

## The 8 Sections (in order)

| # | Exercise | Header to detect |
|---|----------|-----------------|
| 1 | Company Overview | `# COMPANY STRATEGY PROFILE` |
| 2 | ICPs | `## ICPs BY MATURITY` |
| 3 | Advantages | `## MARKETING ADVANTAGES` |
| 4 | Perceptions | `## PERCEPTIONS` |
| 5 | Positioning | `# POSITIONING STATEMENT` |
| 6 | Revenue Levers | `## REVENUE LEVERS` |
| 7 | Big Bets | `## BIG BET CAMPAIGNS` |
| 8 | KPO Goals | `## KPO GOALS` |

## Status Display

Show this dashboard. For each section, mark it with a checkmark if its header is present in the file, or a blank box if not:

```
Marketing Strategy Progress

[x] 1. Company Overview        — # COMPANY STRATEGY PROFILE
[x] 2. ICPs                    — ## ICPs BY MATURITY
[ ] 3. Advantages              — ## MARKETING ADVANTAGES
[ ] 4. Perceptions             — ## PERCEPTIONS
[ ] 5. Positioning             — # POSITIONING STATEMENT
[ ] 6. Revenue Levers          — ## REVENUE LEVERS
[ ] 7. Big Bets                — ## BIG BET CAMPAIGNS
[ ] 8. KPO Goals               — ## KPO GOALS

X/8 sections complete.
```

(The above is an example — show actual status based on the file contents.)

## Next Steps Guidance

After the dashboard:

- **All 8 done:** Tell the user the marketing strategy is complete. Offer to review or refine any section.
- **Some done:** Identify the next incomplete section by number. Tell the user which exercise to run next and give a one-line description of what that exercise covers.
- **None done:** Tell the user to start with Exercise 1 — Company Overview, which creates the `# COMPANY STRATEGY PROFILE` section.

## Saving Exercise Output

When the user completes an exercise with Claude, append the output to the resolved file path (prefer `./marketing-strategy.md` in the current directory, fall back to `~/Desktop/marketing-strategy.md`) under the correct section header. Preserve all existing sections — never overwrite previous content. Use the Write tool only after reading the current file contents first.
