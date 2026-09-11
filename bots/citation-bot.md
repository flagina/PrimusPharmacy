# Citation Bot

**Runs** Tuesday 08:00 WAT (`0 7 * * 2` UTC) · **Writes** `reports/citations/YYYY-MM-DD.md` · **Autonomy** Green

Tracks whether Primus and its clients get *cited by language models*, not just ranked by
Google. For a health brand this is increasingly where the first impression happens, and almost
nobody is measuring it — which is the point.

## Brief

1. Read `config/targets.md` for brands and prompts to monitor.
2. Pull LLM mention data: `ai_opt_llm_ment_search` for the tracked brands,
   `ai_opt_llm_ment_top_domains` and `ai_opt_llm_ment_top_pages` for who is being cited
   instead, `ai_opt_llm_ment_agg_metrics` for the trend. Record model and locale — a mention
   share is meaningless without them.
3. Write `reports/citations/YYYY-MM-DD.md`:

   - **Share of citation** — our brands' mention rate this week vs last, per model.
   - **Who is being cited instead** — the top domains answering our target prompts. This is
     the section with the actual strategy in it.
   - **Newly cited / newly dropped** — pages that gained or lost citation since last week.
   - **Gap** — prompts where a competitor is cited and we are not, and what kind of page they
     won with (a comparison table, a definition block, a study citation, a forum thread).
     Name the *format*, not just the URL — that is what `content-bot` needs to act on.
   - **Not checked** — failed pulls, with the error.

4. Append any actionable gap to `config/targets.md`'s keyword queue as a suggestion block
   marked `# suggested by citation-bot YYYY-MM-DD` — suggestions only, never promoted into the
   active list by a bot.
5. Commit as `citation-bot: YYYY-MM-DD citation share`.

## Health-specific note

Language models cite sources with visible authorship, dates and references far more readily on
health topics than elsewhere. If a competitor is winning citations, check whether their page
carries a named clinical reviewer, a review date and outbound references before concluding
anything about their SEO. Report that as the finding — it is usually the real one.
