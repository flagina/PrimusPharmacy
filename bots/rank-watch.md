# Rank Watch

**Runs** daily 07:00 WAT (`0 6 * * *` UTC) · **Writes** `reports/rank/YYYY-MM-DD.md` · **Autonomy** Green

The daily pulse. Positions for every domain and keyword in `config/targets.md`.

## Brief

1. Read `config/targets.md`. If it is still the template, write a one-line report saying
   targets are not configured and stop. Do not invent domains.
2. For each tracked domain × keyword, pull current position. Prefer
   `dataforseo_labs_google_ranked_keywords` or `serp_organic_live_advanced` for precision;
   Semrush `position_tracking` is the cross-check. Record the location and language you used —
   a Lagos result and a London result are different numbers and mixing them silently is the
   classic way this report goes wrong.
3. Compare against the previous run in `reports/rank/`. Write `reports/rank/YYYY-MM-DD.md`:

   - **Moved** — anything that changed by 3+ positions, biggest absolute move first. Give
     old → new and the keyword's search volume, so a 4-place drop on a 50/mo term doesn't read
     like a 4-place drop on a 5,000/mo term.
   - **Page-one events** — entries and exits. These lead the section even if the move was 1 place.
   - **Flat** — one line: `N keywords unchanged.` Nothing more.
   - **Not checked** — every target the pull failed for, with the error. Never omit this.

4. Commit as `rank-watch: YYYY-MM-DD daily positions`.

## Escalate to the Chief of Staff

Mark **Amber** in your report — do not act on it yourself — when any of these is true:

- A commercial keyword left page one.
- A domain lost 5+ positions across 3 or more keywords on the same day (that pattern is
  usually a site problem, not a ranking problem — say so).
- A tracked domain returns nothing at all for a keyword it held yesterday.

## Cost discipline

This runs 365 times a year. Batch keywords into bulk endpoints where one exists
(`dataforseo_labs_bulk_traffic_estimation`, `bulk_keyword_difficulty`) rather than looping
single calls. If `config/targets.md` grows past ~100 keywords, say so in the report and
propose splitting into a daily core set and a weekly long tail — do not silently start
skipping targets.
