# Todo

Maintained by the Chief of Staff on Mondays and by whoever is working in a live session.

## Blocking the bot team

- [ ] **Create the `general` repository** — session tooling returned 403 and cannot create it.
      Create at github.com/new, then it can be attached to a session.
- [ ] **Attach connectors to the six data-pulling Routines** in the claude.ai Routines UI.
      All seven were created without connector grants, so fired sessions currently have no
      DataForSEO, Semrush, PubMed or Gmail tools. See `bots/README.md` for which bot needs
      which. The Chief of Staff is unaffected — it only reads the repo.
- [x] **DataForSEO working** — resolved 2026-09-11 18:58 UTC. The payment simply took time
      to settle; the earlier credentials theory was wrong. Baseline pulled.
- [ ] **Top up Semrush API units** — subscription active, units exhausted
      (semrush.com/mcp-access).
- [ ] **Top up Semrush** — still exhausted. `rank-watch` runs single-sourced until then, with
      no cross-check on any figure.
- [x] **`config/targets.md` is now `STATUS: ACTIVE`** with measured volumes. The bots run from
      their next scheduled fire.
- [ ] **Fill `config/clients.md`** and set `STATUS: ACTIVE` — `prospect-bot` needs a market.
- [ ] **Give this repo a default branch.** It currently has none; bots commit to
      `claude/grok-bot-launch-0igi3y`. Merge that branch to `main` and the bots follow.
- [ ] **Authorise the WordPress connector** if drafts should ever reach a CMS. Note that
      `content-bot` is instructed never to publish regardless — this only affects what a human
      can do from a session.

## From the 2026-09-11 rank baseline

Full findings in `reports/rank/2026-09-11.md`.

- [ ] **Retarget or consolidate the flagship.** `/where-to-get-misoprostol-in-lagos` targets a
      10/mo keyword and ranks for nothing, while "misoprostol price in nigeria" (1,300/mo) is
      served by a product page. Either retarget it to national price intent or fold it into
      `/misoprostol-cytotec-200-microgram-tablets-lagos`, which already holds position 3.
- [ ] **Approve a Postinor-2 page.** "postinor 2 price in nigeria" is 1,600/mo, flat, low
      competition, and has no page — the largest single gap on the site. Tier C by subject, so
      human-written and clinician-reviewed.
- [ ] **Build four local pages** — Ikeja (260/mo), Lekki (140), Surulere (140), Yaba (90).
      Competition index 1–3.
- [ ] **Confirm we are not chasing "pharmacy near me."** 81,300/mo combined at positions 16–22,
      owned by the map pack, wrong intent for a delivery pharmacy. Recorded as a non-target.
- [ ] **Decide how to defend "big pharmacy in lagos"** (320/mo, position 6) — the homepage holds
      it with no dedicated page.
- [ ] Note the category trend: misoprostol demand −47% and mifepristone −55% over 12 months.
      The diversification argument is now a trend line, not a hypothesis.

## From the 2026-09-11 site audit

Full findings in `reports/site-audit-2026-09-11.md`.

- [ ] **Fix the blog template.** `/where-to-get-misoprostol-in-lagos` renders placeholder text
      ("My post content"), two H1s, a raw anchor tag, and two contradicting author/date blocks.
      Template-level, so the fix lifts every post at once.
- [ ] **Name the superintendent pharmacist and PCN number** in the reviewer block. Highest-
      leverage E-E-A-T fix on the site and it costs nothing.
- [ ] **Stop promoting HealthPlus** in the `/where-can-i-get-misoprostol-in-nigeria` meta
      description.
- [ ] **Decide the pricing policy** across the misoprostol cluster — the flagship withholds all
      prices while the mifepristone page publishes ₦9,000–₦30,000+.
- [ ] **Approve a consolidation plan** for the 11-page reproductive cluster before any new page
      is written. They currently compete with each other.
- [ ] **Get real photographs** of the premises and team. Every image on the site is Unsplash
      stock; the flagship's social preview is captioned "white concrete building during daytime".
- [ ] **Add Pharmacy / MedicalWebPage / FAQPage schema.** The flagship has a complete FAQ block
      sitting unmarked.
- [ ] **Confirm clinical sign-off** on `/at-what-stage-of-pregnancy-can-misoprostol-be-used` —
      it carries gestational-age protocol guidance under a team byline.

## Decisions for Alex

- [ ] Confirm the daily rank set size. Cost scales with it and `rank-watch` runs 365×/year.
- [ ] Name the pharmacist or clinician who signs off health drafts. Every draft carries a
      `Review:` line that only a human removes, and right now no human is named.

## Done

- [x] Messaging teardown of the Grok Bot launch page — `analysis/grok-bot-launch-teardown.html`
- [x] Opening site audit — `reports/site-audit-2026-09-11.md`, 35 URLs mapped
- [x] `config/targets.md` populated from the crawl (volumes pending funded APIs)
- [x] Bot team defined: `CLAUDE.md`, `bots/`, autonomy ladder, health guardrail
