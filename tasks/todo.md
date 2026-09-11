# Todo

Maintained by the Chief of Staff on Mondays and by whoever is working in a live session.

## Blocking the bot team

- [ ] **Create the `general` repository** — session tooling returned 403 and cannot create it.
      Create at github.com/new, then it can be attached to a session.
- [ ] **Fill `config/targets.md`** and set `STATUS: ACTIVE`. Until this is done every bot runs,
      reports "targets not configured", and stops. Nothing else in the system matters until
      this is real.
- [ ] **Fill `config/clients.md`** and set `STATUS: ACTIVE` — `prospect-bot` needs a market.
- [ ] **Give this repo a default branch.** It currently has none; bots commit to
      `claude/grok-bot-launch-0igi3y`. Merge that branch to `main` and the bots follow.
- [ ] **Authorise the WordPress connector** if drafts should ever reach a CMS. Note that
      `content-bot` is instructed never to publish regardless — this only affects what a human
      can do from a session.

## Decisions for Alex

- [ ] Confirm the daily rank set size. Cost scales with it and `rank-watch` runs 365×/year.
- [ ] Name the pharmacist or clinician who signs off health drafts. Every draft carries a
      `Review:` line that only a human removes, and right now no human is named.

## Done

- [x] Messaging teardown of the Grok Bot launch page — `analysis/grok-bot-launch-teardown.html`
- [x] Bot team defined: `CLAUDE.md`, `bots/`, autonomy ladder, health guardrail
