# The roster

Seven bots. Each is a markdown brief in this folder. A Routine (scheduled trigger) wakes a
fresh session on a cron; that session reads `CLAUDE.md`, then its own brief, then works.

| Bot | Runs | Writes to | Autonomy |
|---|---|---|---|
| `chief-of-staff` | Mon 08:00 WAT | `reports/brief-*.md` | Green |
| `rank-watch` | Daily 07:00 WAT | `reports/rank/` | Green |
| `citation-bot` | Tue 08:00 WAT | `reports/citations/` | Green |
| `serp-scout` | Wed 08:00 WAT | `reports/serp/` | Green |
| `content-bot` | Thu 08:00 WAT | `drafts/` | Green to draft, Amber to publish |
| `prospect-bot` | Fri 08:00 WAT | `pipeline/` | Green to list, Amber to send |
| `health-desk` | 1st of month | `reports/health-desk-*.md` | Green |

Lagos is UTC+1 with no DST, so the cron entries are one hour earlier in UTC.

## Changing a bot

Edit its markdown file and commit. The next run picks it up — there is nothing else to
update. Renaming a bot means editing the file *and* the Routine that calls it.

## Turning one off

Disable its Routine. The brief stays in the repo, so turning it back on costs nothing.

## Adding one

Copy the closest existing brief, edit it, commit, then create a Routine whose prompt is:

```
You are the <name> bot for Primus. Read CLAUDE.md, then bots/<name>.md,
and carry out the brief for today's run. Commit your output.
```

Keep the Routine prompt that short on purpose — the brief in the repo is the real
instruction, and it is version-controlled and reviewable. The Routine is only an alarm clock.

## On-demand

Each bot also has a thin agent shim in `.claude/agents/`, so you can run one inside a live
session without waiting for its schedule.
