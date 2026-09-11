# Targets

STATUS: TEMPLATE

> Every bot checks that line first. While it reads `TEMPLATE`, bots write a one-line report
> saying targets are not configured and do nothing else — they will not invent domains or
> keywords to have something to do. Change it to `STATUS: ACTIVE` once the lists below are
> real, and the team starts working on its next scheduled run.

## Domains

| Domain | Whose | Market | Location | Language | Priority |
|---|---|---|---|---|---|
| primuspharmacy.com | Primus (own) | Nigeria | Lagos, Nigeria | en | high |
| _client domain_ | _client name_ | | | | |

Location and language are not optional. A keyword checked in Lagos and the same keyword
checked in London are different numbers, and mixing them silently is how this whole system
starts lying.

## Keyword queue

Ordered. `content-bot` takes the top undrafted item each Thursday.

| # | Keyword | Volume /mo | Intent | Cluster | Drafted |
|---|---|---|---|---|---|
| 1 | _keyword_ | | informational / commercial | | |
| 2 | | | | | |

## Daily rank set

Keywords `rank-watch` checks every day. Keep this under ~100 — everything else goes in the
weekly long tail below.

- _keyword_

## Weekly long tail

- _keyword_

## Citation prompts

The questions `citation-bot` checks for brand mentions. Write them the way a person would
actually ask a model, not as keywords.

- _"what's the best pharmacy in Lagos for ..."_
- _"is ... available in Nigeria"_

## Clinical topics

Subjects `health-desk` monitors monthly for new evidence and regulatory change.

- _topic_
