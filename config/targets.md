# Targets

STATUS: ACTIVE

Volumes and positions below are measured — DataForSEO, Nigeria, en, pulled 2026-09-11.
Baseline: `reports/rank/2026-09-11.md`. Site audit: `reports/site-audit-2026-09-11.md`.

> Semrush remains unavailable (API units exhausted), so `rank-watch` has no cross-check
> source. Single-sourced figures are still figures — run, and note the missing cross-check in
> each report until Semrush is funded.

## Domains

| Domain | Whose | Market | Location | Language | Priority |
|---|---|---|---|---|---|
| primuspharmacy.com | Primus (own) | Nigeria | Nigeria | en | high |

Platform: Hostinger AI Builder (Zyro). Premises: 14 Awoniyi Elemo Street, Ajao Estate, Lagos.
Trading since 2015. Orders via WhatsApp, +234 816 617 7733.

Baseline state: 45 ranked keywords, ETV 230 visits/month, **4 of 35 pages ranking at all**.

Location and language are not optional. A keyword checked in Lagos and the same keyword
checked in London are different numbers, and mixing them silently is how this whole system
starts lying.

## Keyword queue

Re-ordered on evidence, not hypothesis. Several terms from the first draft of this file —
"pharmacy home delivery lagos", "medicine delivery lagos", "same day medicine delivery lagos",
"buy medicine online lagos" — returned **no search volume at all** and have been dropped.
That is what the `[unverified]` marks were protecting against.

### Tier A — local pages (uncontested, build first)

Sixteen delivery areas appear as plain text across the site. None has a page. Competition
index 1–3 is as close to free as this data gets.

| # | Keyword | Volume /mo | Competition idx | Existing page | Drafted |
|---|---|---|---|---|---|
| 1 | pharmacy in ikeja | 260 | 3 | none | |
| 2 | pharmacy in lekki | 140 | 2 | none | |
| 3 | pharmacy in surulere | 140 | 1 | none | |
| 4 | pharmacy in yaba | 90 | 2 | none | |

Ajao Estate — the actual premises — returned no volume, but build it anyway for the Google
Business Profile and the local entity signal. It is not a traffic play.

### Tier B — national commercial

| # | Keyword | Volume /mo | Competition | Existing page | Drafted |
|---|---|---|---|---|---|
| 5 | online pharmacy nigeria | 320 | LOW (33) | `/` ranks 21 | |
| 6 | metformin price in nigeria | 210 | LOW | none | |
| 7 | online pharmacy lagos | 170 | LOW (31) | `/online-pharmacy-store` — no rankings | |
| 8 | coartem price in nigeria | 140 | LOW | none | |
| 9 | weight loss drugs in nigeria | 70 | MEDIUM (49) | `/services` — no rankings | |
| 10 | xarelto price in nigeria | 20 | LOW | `/xarelto-10-mg` — no rankings | |

The pattern across the site is that **price-in-Nigeria queries carry the demand**. Product
pages that name the drug and the price out-perform articles that describe the service.

### Tier B2 — defend what already ranks

The homepage holds these without a dedicated page. Give them one before a competitor does.

| Keyword | Volume /mo | Current position |
|---|---|---|
| big pharmacy in lagos | 320 | 6 |
| big pharmacies in lagos | 320 | 7 |
| biggest pharmacy in lagos | 320 | 8 |
| pharmacy in lagos nigeria | 390 | 11 |
| pharmacy in lagos | 390 | 17 |

### Not a target — "near me"

The homepage ranks 16–22 for "pharmacy near me", "pharmacy closest to me" and "pharmacy close
to me" — 27,100/mo each, 81,300 combined. **We are not chasing these.** The map pack owns
them, the intent is a physical counter within walking distance, and the conversion rate for a
delivery pharmacy is close to zero. Recorded here so no bot and no future session mistakes the
volume for an opportunity.

### Tier C — reproductive health (MONITOR ONLY — no bot drafting)

Tracked by `rank-watch`, `serp-scout` and `citation-bot`. **`content-bot` must not draft,
extend or revise anything in this tier.** Human-written, clinician-reviewed, no exceptions.

| Keyword | Volume /mo | 12-month trend | Where we rank |
|---|---|---|---|
| postinor 2 price in nigeria | **1,600** | flat | **no page** |
| how much is misoprostol in nigeria | 1,300 | −47% | — |
| misoprostol price in nigeria | 1,300 | flat | — |
| mifepristone price in nigeria | 720 | −55% | pos 27 |
| mifepristone and misoprostol tablets price in nigeria | 1,300 | — | pos 28 |
| mifepristone and misoprostol price in nigeria | 320 | flat | — |
| misoprostol price in pharmacy lagos | 260 | — | **pos 3** |
| how much is misoprostol in naira | 260 | — | **pos 6** |
| cytotec price in nigeria | 140 | volatile | — |
| where to get misoprostol in lagos | **10** | flat | no rankings |

Two standing findings:

- **The flagship is aimed at the 10.** `/where-to-get-misoprostol-in-lagos` targets a 10/mo
  term and ranks for nothing. Retarget to national price intent or fold into the product page.
- **Postinor-2 is the largest gap on the whole site** and has no page. Still Tier C by subject.

Cannibalisation to resolve before anything new is written — eleven pages, one winner:

- `/misoprostol-cytotec-200-microgram-tablets-lagos` — **12 keywords, best position 3. The asset.**
- `/mariprist-combipack` — 3 keywords, best 16
- `/mifepristone-price-in-lagos-nigeria` — 3 keywords, best 27
- `/where-to-get-misoprostol-in-lagos` — zero
- `/where-can-i-get-misoprostol-in-nigeria` — zero; meta description promotes a competitor
- `/how-much-is-misoprostol-in-nigeria-2026` — zero
- `/do-pharmacies-have-misoprostol` — zero
- `/what-is-the-pharmacy-name-of-misoprostol` — zero
- `/can-abortion-pill-cause-hormonal-imbalance` — zero
- `/at-what-stage-of-pregnancy-can-misoprostol-be-used` — zero; clinical protocol content,
  needs named clinician sign-off before anything else happens to it
- `/buy-mifepak-misoprostol-mifepristine-lagos` — zero

## Daily rank set

What `rank-watch` checks every day. Deliberately short — this runs 365 times a year and cost
scales with the list. Chosen to cover every tier plus the three defended homepage terms.

- online pharmacy nigeria
- online pharmacy lagos
- big pharmacy in lagos
- pharmacy in lagos nigeria
- pharmacy in ikeja
- pharmacy in lekki
- pharmacy in surulere
- misoprostol price in nigeria
- how much is misoprostol in nigeria
- misoprostol price in pharmacy lagos
- mifepristone price in nigeria
- postinor 2 price in nigeria
- metformin price in nigeria
- coartem price in nigeria

Batch these into bulk endpoints rather than looping single calls.

## Weekly long tail

Everything in Tier A, B, B2 and C not in the daily set, plus the remaining twelve delivery
areas (Victoria Island, Festac, Mushin, Agege, Apapa, Lagos Island, Amuwo-Odofin, Eti-Osa,
Somolu, Lagos Mainland, Ajah, Ikorodu) and the nationwide cities.

## Citation prompts

What `citation-bot` checks for brand mentions. Written the way a person actually asks a model.
Deliberately non-reproductive — these are the questions where a licensed Lagos pharmacy has a
defensible, citable answer and being cited is commercially useful.

- "best online pharmacy in Lagos for home delivery"
- "which pharmacies in Lagos deliver medication same day"
- "where can I buy genuine medication online in Nigeria"
- "how do I know if medication bought in Nigeria is counterfeit"
- "what should I check before buying medicine from an online pharmacy in Nigeria"
- "how much does Coartem cost in Nigeria"

## Clinical topics

Subjects `health-desk` monitors monthly for new evidence and regulatory change.

- Misoprostol — licensed indications, NAFDAC registration, counterfeit alerts
- Mifepristone — NAFDAC status, availability in Nigeria
- Levonorgestrel / Postinor-2 — OTC status, NAFDAC registration, counterfeit alerts
- Antimalarials (Coartem / artemether-lumefantrine) — resistance and guidance changes
- Metformin — NAFDAC recalls, impurity notices
- Rivaroxaban (Xarelto) — safety updates
- Bromocriptine (Parlodel) — safety updates
- Nigerian regulatory: NAFDAC recalls and PCN guidance affecting online dispensing
