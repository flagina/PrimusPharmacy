# SERP Scout

**Runs** Wednesday 08:00 WAT (`0 7 * * 3` UTC) · **Writes** `reports/serp/YYYY-MM-DD.md` · **Autonomy** Green

Watches the *shape* of the results page, not our position on it. Which source types Google is
favouring for our keywords decides what we should even be building.

## Brief

1. Read `config/targets.md`.
2. For each priority keyword, pull the live SERP (`serp_organic_live_advanced`, correct
   location and language) and classify the top 10 by source cluster: publisher blog, forum or
   community, video, retailer, government or regulator, clinical or journal, brand site.
3. Note which SERP features are present: AI Overview, Discussions and Forums, People Also Ask,
   video carousel, Top Stories, local pack.
4. Write `reports/serp/YYYY-MM-DD.md`:

   - **Cluster shifts** — keywords where the dominant source type changed since the last run.
     This is the headline; a shift from blogs to forums changes what we build, entirely.
   - **Feature changes** — AI Overview or Discussions box appearing or disappearing, by keyword.
   - **New entrants** — domains in the top 10 that were not there last week, and their cluster.
   - **Reshaping candidates** — keywords where the SERP is dominated by a cluster we are not
     competing in, with the cluster named. Cross-reference the `serp-reshaping` skill's
     eligibility criteria before listing one; a candidate that fails those criteria is noise.
   - **Not checked** — failed pulls, with the error.

5. Commit as `serp-scout: YYYY-MM-DD SERP shape`.

## Judgement

A single-week cluster shift is usually noise. Flag a shift as real only if it holds across two
consecutive runs, and say which run you are on. Being second to notice a durable change beats
being first to report a flicker.

**YMYL note:** for health queries Google leans hard on regulator, clinical and established-
publisher sources. If the top 10 for a keyword is entirely NAFDAC, NHS, Mayo and journals, the
correct finding is usually *do not compete here directly* — say that plainly rather than
producing a reshaping candidate that will waste a quarter.
