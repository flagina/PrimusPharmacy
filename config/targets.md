# Targets

STATUS: HOLD

> Bots run only when this reads `STATUS: ACTIVE`. It is on HOLD rather than TEMPLATE because
> the targets below are real — what is missing is the data to measure them with. DataForSEO
> returns HTTP 402 (out of credits) and Semrush reports its API units exhausted, so every
> measurement bot would produce an empty report every day. Fund both, attach the connectors to
> the Routines (see `bots/README.md`), then set this to ACTIVE.

Populated from a live crawl on 2026-09-11 — see `reports/site-audit-2026-09-11.md`.

## Domains

| Domain | Whose | Market | Location | Language | Priority |
|---|---|---|---|---|---|
| primuspharmacy.com | Primus (own) | Nigeria | Lagos, Nigeria | en | high |

Platform: Hostinger AI Builder (Zyro). Physical premises: 14 Awoniyi Elemo Street, Ajao
Estate, Lagos. Trading since 2015. Orders run through WhatsApp on +234 816 617 7733.

Location and language are not optional. A keyword checked in Lagos and the same keyword
checked in London are different numbers, and mixing them silently is how this whole system
starts lying.

No client domains yet. Add them here as they sign.

## Search volume is unverified

Every volume column below is empty on purpose. Both paid sources were unavailable when this
file was built, and `CLAUDE.md` forbids inventing a number. The first successful `rank-watch`
run fills them. Until then treat the ordering as a hypothesis from the crawl, not from data.

## Keyword queue

Ordered. `content-bot` takes the top undrafted item each Thursday. Tier A leads deliberately:
the site's visibility is concentrated in one scrutinised category, and this is the
diversification work.

### Tier A — non-reproductive commercial (underbuilt, safe for bots)

| # | Keyword | Volume /mo | Intent | Existing page | Drafted |
|---|---|---|---|---|---|
| 1 | online pharmacy lagos | [unverified] | commercial | /online-pharmacy-store | |
| 2 | buy medicine online lagos | [unverified] | transactional | partial | |
| 3 | pharmacy home delivery lagos | [unverified] | transactional | none | |
| 4 | same day medicine delivery lagos | [unverified] | transactional | none | |
| 5 | coartem price in nigeria | [unverified] | commercial | none | |
| 6 | metformin price in nigeria | [unverified] | commercial | none | |
| 7 | xarelto price in nigeria | [unverified] | commercial | /xarelto-10-mg | |
| 8 | hypertension medication lagos | [unverified] | informational | none | |
| 9 | diabetes supplies lagos | [unverified] | commercial | none | |
| 10 | erectile dysfunction treatment lagos | [unverified] | commercial | none | |
| 11 | weight management pharmacy lagos | [unverified] | commercial | /services | |
| 12 | lab results review lagos | [unverified] | commercial | /services | |
| 13 | wholesale medical supplies lagos | [unverified] | commercial | none | |

### Tier B — local (16 delivery areas named on site, none has a page)

One page per area, built from real delivery data, not spun. Start with the three where the
pharmacy actually has volume — Alex to say which.

| Area | Page | Notes |
|---|---|---|
| Ajao Estate | none | the physical premises — build this one first |
| Ikeja | none | |
| Lekki | none | |
| Victoria Island | none | |
| Surulere · Yaba · Festac · Mushin · Agege · Apapa · Lagos Island · Amuwo-Odofin · Eti-Osa · Somolu · Lagos Mainland · Ajah · Ikorodu | none | second wave |
| Abuja · Port Harcourt · Ibadan · Sagamu · Abeokuta · Enugu | none | nationwide shipping, lower priority |

### Tier C — reproductive health cluster (MONITOR ONLY — no bot drafting)

Tracked by `rank-watch`, `serp-scout` and `citation-bot`. **`content-bot` must not draft,
extend or revise any page in this tier.** Human-written, clinician-reviewed, no exceptions.

Existing pages, and the cannibalisation problem to resolve before anything new is written:

- /where-to-get-misoprostol-in-lagos — flagship, keep as the canonical target
- /where-can-i-get-misoprostol-in-nigeria — meta description currently promotes a competitor
- /do-pharmacies-have-misoprostol — consolidation candidate
- /what-is-the-pharmacy-name-of-misoprostol — consolidation candidate
- /how-much-is-misoprostol-in-nigeria-2026 — price intent, but flagship withholds price
- /at-what-stage-of-pregnancy-can-misoprostol-be-used — clinical protocol content, needs a
  named clinician sign-off before anything else happens to it
- /can-abortion-pill-cause-hormonal-imbalance
- /mifepristone-price-in-lagos-nigeria — publishes ₦9,000–₦30,000+, inconsistent with flagship
- /buy-mifepak-misoprostol-mifepristine-lagos
- /mariprist-combipack — product
- /misoprostol-cytotec-200-microgram-tablets-lagos — product

## Daily rank set

What `rank-watch` checks every day. Kept deliberately short — this runs 365 times a year and
the cost scales with the list. Everything else goes in the weekly long tail.

- online pharmacy lagos
- buy medicine online lagos
- pharmacy home delivery lagos
- online pharmacy nigeria
- where to get misoprostol in lagos
- misoprostol price nigeria
- cytotec lagos
- misofem
- mifepristone price lagos
- pharmacy ajao estate

## Weekly long tail

Everything in Tier A and Tier B not listed above, plus product-page terms.

## Citation prompts

What `citation-bot` checks for brand mentions. Written the way a person actually asks a model.

- "best online pharmacy in Lagos for home delivery"
- "which pharmacies in Lagos deliver medication same day"
- "where can I buy genuine medication online in Nigeria"
- "how do I know if medication bought in Nigeria is counterfeit"
- "what should I check before buying medicine from an online pharmacy in Nigeria"

Deliberately non-reproductive. These are the questions where a licensed Lagos pharmacy has a
defensible, citable answer and where being cited is commercially useful.

## Clinical topics

Subjects `health-desk` monitors monthly for new evidence and regulatory change.

- Misoprostol — licensed indications, NAFDAC registration status, counterfeit alerts
- Mifepristone — NAFDAC status, availability in Nigeria
- Antimalarials stocked (Coartem / artemether-lumefantrine) — resistance and guidance changes
- Metformin — NAFDAC recalls, impurity notices
- Rivaroxaban (Xarelto) — safety updates
- Bromocriptine (Parlodel) — safety updates
- Nigerian regulatory: NAFDAC recalls and PCN practice guidance affecting online dispensing
