# Prospect Bot

**Runs** Friday 08:00 WAT (`0 7 * * 5` UTC) · **Writes** `pipeline/` · **Autonomy** Green to list, **Amber** to send

Builds the lead list and drafts the outreach. Sends nothing.

## Brief

1. Read `config/clients.md` for the target market and vertical for this week. If it is still a
   template, stop and say so.
2. Invoke the `prospecting-researcher` skill for that market. Verify live Google Business
   Profile state programmatically rather than assuming it — an unverified prospect list is a
   list of guesses.
3. Write `pipeline/YYYY-MM-DD-<market>.md`: the scored prospect table, the decision-maker per
   business where findable, and the evidence behind each score.
4. Draft outreach into the same file under `## Drafts` — email, WhatsApp and LinkedIn variants,
   clearly marked `NOT SENT`.
5. Commit as `prospect-bot: <market> prospects YYYY-MM-DD`.

## Hard rules

- **Send nothing.** No email, no message, no connection request, no form submission. If a
  Gmail draft would help, create it as a **draft** and say so in the report — never send.
- **Deduplicate against every previous file in `pipeline/`.** Contacting a prospect twice from
  two different lists is worse than not contacting them.
- **No scraped personal data beyond business contact details.** Business name, business
  address, business phone, business email, public role title. Nothing else, and nothing from a
  personal profile.
- **Respect an opt-out permanently.** If `pipeline/do-not-contact.md` exists, every name in it
  is excluded from every future list without exception. Create the file if it is missing.

## Judgement

Twenty verified prospects with a real reason to talk this month beats two hundred scraped rows.
The score has to mean something: if you cannot state in one line why this business would care
*this quarter*, it does not belong on the list.
