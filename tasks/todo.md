# Todo

Maintained by the Chief of Staff on Mondays and by whoever is working in a live session.

## Blocking the bot team

- [ ] **Create the `general` repository** — session tooling returned 403 and cannot create it.
      Create at github.com/new, then it can be attached to a session.
- [ ] **Attach connectors to the six data-pulling Routines** in the claude.ai Routines UI.
      All seven were created without connector grants, so fired sessions currently have no
      DataForSEO, Semrush, PubMed or Gmail tools. See `bots/README.md` for which bot needs
      which. The Chief of Staff is unaffected — it only reads the repo.
- [ ] **Fix DataForSEO billing.** Retested 2026-09-11 after a reported top-up — still 402 on
      every billable endpoint. Diagnostic: the free metadata endpoint `serp_locations`
      returned 200 OK with valid data, so the credentials and the connector are fine; Labs,
      Keywords Data and SERP all return 402. That is an account-balance refusal, not an auth
      or scope problem. Most likely the top-up landed on a different API login than the one
      this connector uses — DataForSEO bills per API login, not per dashboard email. Check the
      login on app.dataforseo.com/api-access against the funded account, and confirm the
      balance is account credit rather than a plan.
- [ ] **Top up Semrush API units** — subscription active, units exhausted
      (semrush.com/mcp-access).
- [ ] Until both are resolved the measurement bots produce nothing, which is why
      `config/targets.md` stays on HOLD rather than ACTIVE.
- [ ] **Set `config/targets.md` to `STATUS: ACTIVE`** once the two above are done. The targets
      themselves are now filled in from a live crawl.
- [ ] **Fill `config/clients.md`** and set `STATUS: ACTIVE` — `prospect-bot` needs a market.
- [ ] **Give this repo a default branch.** It currently has none; bots commit to
      `claude/grok-bot-launch-0igi3y`. Merge that branch to `main` and the bots follow.
- [ ] **Authorise the WordPress connector** if drafts should ever reach a CMS. Note that
      `content-bot` is instructed never to publish regardless — this only affects what a human
      can do from a session.

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
