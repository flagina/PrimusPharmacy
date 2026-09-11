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

## Routine IDs

| Bot | Cron (UTC) | Trigger |
|---|---|---|
| `chief-of-staff` | `0 7 * * 1` | `trig_01KDbrpw9oBY2oNoikNDuxuT` |
| `rank-watch` | `0 6 * * *` | `trig_012SXo2nqYK7L4mEMDcZCHgS` |
| `citation-bot` | `0 7 * * 2` | `trig_017ohbrYBxZbpn8PiHjqqTVK` |
| `serp-scout` | `0 7 * * 3` | `trig_013pA4rcC6dLX2fHTUQ9GLjb` |
| `content-bot` | `0 7 * * 4` | `trig_013ADh4Nibjfwo2gDsnY79x4` |
| `prospect-bot` | `0 7 * * 5` | `trig_01KqNj1rD3NWiaKMiSXFBfQK` |
| `health-desk` | `0 7 1 * *` | `trig_01MGSvYWK3M5nUE3pBbtaQTd` |

Only the Chief of Staff notifies (push + email). One signal a week, not seven — the other six
report into the repo and the Monday brief decides what is worth an interruption.

## Known limitation: the Routines carry no connectors

All seven were created without MCP connector grants — the tool that created them could not
pass any through, and it said so on every call. A fired session therefore starts with no
`mcp__*` tools: no DataForSEO, no Semrush, no PubMed, no Gmail, no GitHub API.

In practice that means `rank-watch`, `citation-bot`, `serp-scout` and `health-desk` cannot pull
the data their briefs depend on until this is fixed, and will correctly report the source as
unavailable rather than inventing numbers.

**The fix:** open each Routine in the claude.ai Routines UI and attach the connectors it needs.
Per bot: `rank-watch` → DataForSEO, Semrush. `citation-bot` → DataForSEO. `serp-scout` →
DataForSEO. `content-bot` → DataForSEO, PubMed. `prospect-bot` → Vibe Prospecting, DataForSEO.
`health-desk` → PubMed. `chief-of-staff` → none needed; it only reads the repo, so it works as
created.

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
