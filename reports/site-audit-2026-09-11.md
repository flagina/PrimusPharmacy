Bot:      manual (interactive session)
Run:      2026-09-11 15:2x UTC
Sources:  Firecrawl map + scrape of primuspharmacy.com (pulled 15:2x UTC) ·
          DataForSEO UNAVAILABLE (HTTP 402, out of credits) ·
          Semrush UNAVAILABLE (subscription active, API units exhausted)
Verdict:  7 items need Alex · 35 URLs mapped · 2 pages read in full

# Primus Pharmacy — opening site audit

No ranking, volume or traffic figures appear in this report. Both paid data sources returned
payment errors, and inventing numbers is worse than leaving holes. Everything below is
observed directly in the live HTML.

## What changed

Nothing — this is the baseline. Future runs compare against it.

## What I found

### The site

35 URLs. Built on Hostinger AI Builder (Zyro). Physical pharmacy at 14 Awoniyi Elemo Street,
Ajao Estate, Lagos; trading since 2015; WhatsApp-led ordering on +234 816 617 7733.

Content splits three ways:

- **~11 pages on misoprostol / mifepristone / medical abortion.** This is the site's main SEO
  thrust by a wide margin.
- **~15 product pages** — supplements (Wellwoman, Perfectil, glutathione, probiotics) and
  prescription items (Xarelto, Parlodel, lactulose).
- **~9 service and utility pages** — services, family planning, store, contacts, blog, legal.

The flagship (`/where-to-get-misoprostol-in-lagos`) is genuinely well-built: licensed
indications first, POM status stated, NAFDAC framing, counterfeit guidance, contraindications,
a real "when to seek urgent care" list, and a substantial FAQ. It is not thin content. The
defects below are template and consistency failures sitting on top of decent writing.

### Defects, most damaging first

**1. The blog template is leaking into the flagship page.** `/where-to-get-misoprostol-in-lagos`
renders *two* `H1`s, the literal placeholder string **"My post content"**, and a raw `<a href>`
tag as escaped visible text. A YMYL money page with visible placeholder text is the single
worst signal on the site.

**2. Contradictory authorship on the same page.** One block says "Alex Obi · 4/2/2026 · 1 min
read"; another says "Primus Pharmacy Team · Updated April 2026 · 8 min read". Two authors, two
dates, and a 1-minute read time on an 8-minute article. For YMYL, contradictory authorship
undercuts the exact signal the page is trying to earn.

**3. The reviewer is a team, not a person.** "Reviewed by the Primus Pharmacy Team, Licensed
Pharmacists" with no named individual and no PCN registration number. The pharmacy has the
harder assets already — a physical address, a 2015 trading history, 344 Google reviews. Naming
the superintendent pharmacist and their PCN number is the highest-leverage fix on this list and
costs nothing.

**4. Titles are duplicated site-wide.** Every title gets the site name appended to an already
complete title: `Where to Get Misoprostol in Lagos | Primus Pharmacy (Same-Day Delivery) |
Online Pharmacy Lagos Nigeria: Primus pharmacy` — roughly 110 characters, brand twice. Meta
descriptions are duplicated the same way, the same sentence comma-joined to itself.

**5. A competitor is named in a Primus meta description.** The SERP snippet for
`/where-can-i-get-misoprostol-in-nigeria` reads "Reputable online pharmacies that deliver
across Nigeria include HealthPlus Pharmacy…". Primus is advertising a competitor in its own
search result.

**6. Keyword cannibalisation across the misoprostol cluster.** Eleven pages compete for
overlapping intent — `where-to-get-…-in-lagos`, `where-can-i-get-…-in-nigeria`,
`do-pharmacies-have-misoprostol`, `what-is-the-pharmacy-name-of-misoprostol`,
`how-much-is-…-2026`, plus two product pages and the combipack pages. They will split signals
against each other rather than compounding.

**7. Inconsistent pricing policy inside one cluster.** The flagship withholds all prices
("Confirm via WhatsApp" three times) while `/mifepristone-price-in-lagos-nigeria` publishes a
₦9,000–₦30,000+ range. A page targeting price intent that shows no price will not hold that
query.

**8. Stale headings.** The flagship is dated April 2026 and titled 2026, but carries a section
headed "Misoprostol Price in Lagos (2025)".

**9. Every image is Unsplash stock.** The flagship's `og:image` alt text is literally "white
concrete building during daytime". A pharmacy claiming a named street address and 344 reviews
has real premises and real staff, and is instead sharing stock photography as its social
preview. For YMYL this is a wasted trust asset, not a cosmetic issue.

**10. No structured data observed.** No `Pharmacy`, `MedicalWebPage` or `FAQPage` schema. The
flagship has a fully-formed FAQ block sitting unmarked — free rich-result eligibility going
unclaimed.

**11. Local coverage is text, not pages.** Sixteen Lagos areas (Ikeja, Lekki, VI, Surulere,
Yaba, Festac, Mushin, Agege, Apapa, Lagos Island, Amuwo-Odofin, Eti-Osa, Somolu, Lagos
Mainland, Ajah, Ikorodu) and six other cities appear as comma lists on several pages. None has
a page.

**12. Obsolete meta keywords tag, with a typo.** The homepage carries
`keywords="… Where can i buy misprostol in Lagos …"` — misspelled, and the tag has been ignored
by Google for many years.

**13. Homepage H1 does not match its title.** H1 is "Reproductive Health and Mental Health:
Navigating Your Most Private Decisions with Confidence"; the title sells "Best Online Pharmacy
Store in Nigeria". Only two internal links run from the homepage into the money cluster.

## What it means

The writing is better than the plumbing. Nobody needs to rewrite this content — it needs a
template fix, a named reviewer, and consolidation. That ordering matters: fixing the template
lifts every page at once, and it is the cheapest work on the list.

The site's commercial centre of gravity is medical abortion. That is legitimate pharmacy
practice — misoprostol is on the WHO Essential Medicines List and has licensed indications in
ulcer prevention, miscarriage management, postpartum haemorrhage and labour induction, all of
which the flagship covers properly. It is also the most scrutinised category on the open web,
and Nigerian law here is restrictive. Two consequences for how we work:

- The concentration is a commercial risk regardless of the law. One algorithm update aimed at
  this category takes most of the site's visibility with it. The non-reproductive side of the
  business — chronic care, supplements, delivery, the licensed-pharmacy-in-Lagos proposition —
  is barely built out and is where diversification sits.
- No bot writes in this cluster. See below.

## What needs a human

1. **Fund DataForSEO and Semrush**, or the measurement half of the bot team cannot run at all.
2. **Name the superintendent pharmacist and PCN number** for the reviewer block.
3. **Fix the blog template** — placeholder text, duplicate H1, duplicate title and description.
4. **Decide the pricing policy** across the misoprostol cluster: publish ranges or withhold, but
   not both.
5. **Approve a consolidation plan** for the 11-page cluster before any new page is written.
6. **Rewrite the `/where-can-i-get-misoprostol-in-nigeria` description** to stop promoting
   HealthPlus.
7. **Confirm the clinical review position on `/at-what-stage-of-pregnancy-can-misoprostol-be-used`.**
   Its snippet gives gestational-age and protocol guidance. That is clinical content and needs a
   named clinician's sign-off on the page, not a team byline.

## Standing rule added for the bots

`content-bot` is barred from the reproductive-health cluster entirely. It may not draft, extend
or revise any page about misoprostol, mifepristone, abortion, gestational limits or dosing
protocols. That work is human-written and clinician-reviewed. The bar is recorded in
`bots/content-bot.md` and in `config/targets.md`.
