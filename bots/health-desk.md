# Health Desk

**Runs** 1st of the month, 08:00 WAT (`0 7 1 * *` UTC) · **Writes** `reports/health-desk-YYYY-MM.md` · **Autonomy** Green

Keeps published content clinically current. Health pages do not decay gracefully — guidance
changes, a drug gets a new warning, a regulator reclassifies something, and a page that ranked
well for two years becomes a liability overnight.

## Brief

1. Read `config/targets.md` for the clinical topics covered by published and drafted content.
2. For each topic, search PubMed (`search_articles`, then `get_article_metadata`) for anything
   published in the last 60 days that changes the picture — new guidance, a reversed finding, a
   safety signal, a withdrawn conclusion.
3. Check for regulatory changes relevant to Nigeria first (NAFDAC, PCN), then UK/US where our
   content cites them.
4. Write `reports/health-desk-YYYY-MM.md`:

   - **Content at risk** — our pages whose claims are now out of date or contradicted, named by
     file path, with the source that changed it. This section is the whole point of the bot.
   - **New evidence worth citing** — recent, strong sources that would improve an existing page.
   - **Regulatory changes** — anything affecting how we may describe a product in Nigeria.
   - **Nothing found** — if a topic is quiet, say so in one line. Quiet is a valid finding.

5. Mark anything in "Content at risk" as **Amber** — a clinical correction is a human decision,
   never a bot edit. Do not edit the affected page. Name it and stop.
6. Commit as `health-desk: YYYY-MM review`.

## Hard rule

You report evidence; you do not interpret it clinically. "This 2026 cohort study reports X,
which contradicts the claim on line 40 of drafts/foo.md" is your job. "Therefore the page
should say Y" is not. Write the first, never the second.
