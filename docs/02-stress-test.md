# 02 — Stress Test (Round 2)

- **Date:** 2026-09-26
- **Input:** `docs/01-research-and-candidates.md`, orchestrator rulings, orchestrator Reddit addendum `[O]`
- **Job this round:** try to KILL each idea. Only survivors go to the finals.

---

## 0. TL;DR

- **Of the 8 ideas tested (5 from Round 1 + 3 new wildcards), only 1 survives cleanly: Card Benefit Claims & Appeals.** It scores 73/130. It is the only idea where no product does the exact job, where the pain is loud and recent, and where we can build a moat: card benefit terms that change over time, plus data on which claims get paid.
- **Family Cookbook (66) is a conditional survivor.** Demand is proven, but ReciScan and Family Cookbook Project already do the exact job. A printed book by Dec 25 isn't realistic for a mid-November launch, so it must be digital-first.
- **DIY Day-of Wedding Coordinator (63) is the best wildcard, but 63 is technically in my kill band.** I'm keeping it only as a **slot-3 placeholder** behind a stricter kill-switch test, because nothing else scored higher.
- **Killed:** HeirloomDraft (SaveOr already does it), Pet Move Planner (7+ competitors plus liability), PPM Companion (free apps plus the off-season), DIY Estate Sale Kit (sale-day point-of-sale tools already exist), Property-Tax Appeal Kit (5+ flat-fee tools at $29–100 plus Ownwell).
- **Main lesson from this round:** the AI-built-app flood has also reached the "DIY tool undercuts a human service" lens (property-tax tools, estate-sale checkout tools). Having no competitors is no longer the deciding factor. What decides now is **T10 (what stops a copy)** and **T4 (reaching the user when the problem hits)**.

**Proposed FINAL 3** (details in §5):

| Slot | Idea | Status |
|---|---|---|
| 1 | **Card Benefit Claims & Appeals** (trip delay, baggage, rental-car CDW, purchase protection, extended warranty, return, phone protection) | ✅ SURVIVES |
| 2 | **Family Cookbook** (digital-first, relatives contribute) | ⚠️ CONDITIONAL: must pass a 1-week smoke test |
| 3 | **DIY Day-of Coordinator** for budget weddings | ⚠️ PLACEHOLDER (63, kill band): must pass a strict smoke test, or gets replaced |

**Steelman of the best idea I killed:** HeirloomDraft (§6).

---

## 1. Rulings applied and ground rules

- **Marriage Evidence Binder:** OUT (orchestrator ruling). Not tested.
- **Web-first** (responsive web app / PWA) is assumed in every build estimate.
- **Seasonality:** Cookbook is judged on whether a *printed* book can realistically ship before Dec 25 with a ~mid-Nov launch. Answer: no for most users (§3.4), so I judged it as digital-first.
- **DIY Recruit / Private-School / Custom-Home:** I accept all three kills. The only one close to "unfair" is DIY Recruit (strongest pay signal: NCSA costs $2–6k). But FieldLevel and NextCommit are free and have network effects, so it stays dead.

**Access limits (important for how much to trust the numbers):**
- Only WebSearch works from this container. WebFetch and curl are blocked for most sites (Trustpilot, the App Store's full review pages, fairsplit.com, ahrefs.com, Google Trends and autocomplete, Reddit). Review counts and ratings below come from **search snippets**.
- **Keyword volumes are my estimates** (`est.`), not tool-measured. Treat them as order-of-magnitude guesses and verify with Google Keyword Planner or Ahrefs if the network is opened up.
- Reddit numbers come from your addendum `[O]`. `[K]` means my prior knowledge, not re-verified this round.

**Scoring:** each test is scored 1–10, where **higher = better for us** (for T7 pre-mortem and T8 risk, higher = lower risk). T2, T4 and T5 count double, so the maximum is 130.
- **Survive:** ≥ 70 with no fatal test.
- **Conditional:** 64–69.
- **Kill:** ≤ 63, or a fatal T1/T2 (a well-reviewed product already does the exact job, or free tools deliver 80%+ of the value).

---

## 2. Scorecard

| Idea | T1 Comp | T2 Subst ×2 | T3 Demand | T4 Reach ×2 | T5 Econ ×2 | T6 Trigger | T7 Pre-mortem | T8 Risk | T9 Build | T10 Moat | **Weighted /130** | Verdict |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **Card Claims & Appeals** | 6 | 4 | 7 | 5 | 5 | 8 | 5 | 6 | 7 | 6 | **73** | ✅ SURVIVE |
| Family Cookbook | 3 | 5 | 7 | 6 | 4 | 7 | 4 | 7 | 5 | 3 | **66** | ⚠️ CONDITIONAL |
| W2 DIY Day-of Coordinator | 4 | 3 | 7 | 5 | 5 | 6 | 4 | 6 | 7 | 3 | **63** | ⚠️ PLACEHOLDER (kill band; kept only for slot 3) |
| HeirloomDraft | 3 | 5 | 4 | 4 | 4 | 7 | 4 | 7 | 7 | 3 | **61** | ❌ KILL |
| W1 DIY Estate Sale Kit | 3 | 5 | 6 | 4 | 5 | 6 | 4 | 6 | 5 | 3 | **61** | ❌ KILL |
| W3 Property-Tax Appeal Kit | 2 | 4 | 8 | 3 | 5 | 8 | 3 | 6 | 3 | 3 | **57** | ❌ KILL (fatal T1) |
| Pet Move Planner | 2 | 3 | 4 | 6 | 4 | 8 | 4 | 3 | 5 | 4 | **56** | ❌ KILL (fatal T1/T2) |
| PPM Companion | 3 | 3 | 5 | 6 | 2 | 5 | 3 | 7 | 9 | 2 | **56** | ❌ KILL (fatal T2/T5) |

Weighted = T1 + 2·T2 + T3 + 2·T4 + 2·T5 + T6 + T7 + T8 + T9 + T10.

---

## 3. The five Round-1 ideas

### 3.1 Card Benefit Claims & Appeals ✅ (73)

**Framing (I accept your broader hypothesis):** this isn't just a trip-delay kit. It's **"claims + denial appeals for the insurance-style benefits on your cards"**:
- trip delay, trip cancellation and interruption
- baggage delay and lost baggage
- **rental-car collision damage waiver (CDW)**, the highest-stakes type (added this round)
- purchase protection, extended warranty, return protection
- cell-phone protection

The MVP launches with a narrower slice (§5).

**T1 — Competitor teardown (score 6)**

| Competitor | What it does | Price | Rating / reviews | Does it do *our* job? |
|---|---|---|---|---|
| [CardPointers](https://upgradedpoints.com/credit-cards/cardpointers-review/) | Tracks offers and credits; filters "which of my cards has trip delay / primary rental coverage" | Free tier; CardPointers+ about $90/yr | ~4.7★ from ~9,500 iOS ratings ([thoughtcard](https://thoughtcard.com/cardpointers-review/)) | No. It tells you *which* card covers something, not how to file or appeal. |
| [Kudos](https://www.joinkudos.com/blog/hidden-perks) (funded; Samsung partnership) | "Hidden Perks" says things like "Flight booked! You're covered by travel delay insurance…" | Free (earns from affiliate card sign-ups) | ~4.2★ Chrome, ~4.8 elsewhere; complaints: benefit data "missing or wrong" ([stackeasy](https://www.stackeasy.ai/blog/kudos-review)) | Partly. It raises awareness only. No claim packet, no appeal. |
| [Pine AI](https://www.19pine.ai/) ($25M Series A) | An AI agent that calls companies to dispute, cancel, and chase refunds | Pay on success plus subscription credits; 53.7k users ([aiagentstore](https://aiagentstore.ai/ai-agent/19pine-ai)) | Claims a 93% win rate | Indirect. Generic, phone-first, not built around benefit terms. **Most likely to move into this space.** |
| AwardWallet, TPG, NerdWallet, UpgradedPoints, 10xTravel | Free "how to file" guides ([AwardWallet](https://awardwallet.com/blog/how-to-file-a-flight-delay-claim-with-chase/), [TPG on eClaimsline](https://thepointsguy.com/credit-cards/eclaimsline-insurance-issues/)) | Free | Rank #1 on Google | Guides only. They also **own the head keywords**. |
| "Flight & Train Claim" app ([App Store](https://apps.apple.com/app/id6748158725)) | EU-style airline compensation letters | ? | ? | No. Airline compensation, not card benefits. |
| Benefit administrators (eClaimsline/Allianz, Card Benefit Services/Asurion, Amex) | The claim portals themselves | — | Allianz A+ on BBB, but its complaint file is full of "requests for documents already submitted" ([BBB](https://www.bbb.org/us/va/henrico/profile/insurance-companies/allianz-global-assistance-0603-4001660/complaints?page=10)) | They are the opponent, not a competitor. |

**Nobody does "you've been hit, here's your packet, and here's your appeal" across benefit types.** Nearest threat: Pine AI adds card benefits, or Kudos adds claims.

**T2 — The 2026 substitute test (score 4)**
- A savvy user can get about 60% of the value for free in 30 minutes: Google the TPG/AwardWallet guide, download the benefit PDF, paste it plus the denial letter into ChatGPT, and get an appeal letter.
- **What they can't easily get:**
  1. **Current, versioned terms per card.** Terms change (Sapphire Reserve was overhauled in June 2025), and LLMs blend old and new versions.
  2. **Document checklists per administrator**, including known traps: "receipt rejected for no date", itemized hotel folios, the carrier delay letter, repair estimates for extended warranty, and for CDW the rental company's damage report, photos, and the **loss-of-use / fleet log** that rental companies often refuse to hand over.
  3. **A denial-reason → rebuttal playbook** built from real outcomes. People post these because good information is scarce `[O]`.
  4. **Claim-window countdowns** (20–90 days; CDW up to 365 days, [Visa terms](https://usa.visa.com/content/dam/VCOM/regional/na/us/Solutions/documents/business-auto-rental-collision-damage-waiver-benefit-terms.pdf)).
  5. **A clean, compiled evidence packet.**
- **Is it worth paying for?** For a non-expert with $300–$2,000 at stake, $19 is easy. For hardcore churners, who build their own tools (the 1,008-upvote benefits spreadsheet `[O]`), maybe not. **Target the 1.56M-member r/CreditCards type of user, not r/churning.**

**T3 — Demand evidence (score 7)**
- **Pain `[O]`:** "Trip delay insurance is basically a scam" (420↑ / 251 comments, Jan 2026). A denial after Southwest cancelled twice (Sep 2026). "Denied twice, then paid on escalation" sagas. "$823 PAID" success story (172↑). An extended-warranty claim paid only on appeal (~$161). Baggage delay paying "only 30%, one receipt rejected for no date". Citi purchase protection "worthless".
- **Admin friction `[S]`:** eClaimsline claims stuck in loops asking for the same documents ([FlyerTalk](https://www.flyertalk.com/forum/chase-ultimate-rewards/1777854-anyone-else-unable-file-claims-eclaimsline.html), [TPG](https://thepointsguy.com/credit-cards/eclaimsline-insurance-issues/)). CFPB and BBB complaints about Card Benefit Services ([BBB](https://www.bbb.org/us/va/richmond/profile/aviation-services/card-benefit-services-0603-63412499/complaints)). Extended-warranty companies deny 30–50% of first claims, and many denials are reversible ([Pine AI blog](https://www.19pine.ai/blog/dispute-extended-warranty-claims)).
- **Awareness gap:** 62% of travelers misread their card's coverage ([PR Newswire](https://www.prnewswire.com/news-releases/new-data-shows-62-of-travelers-are-wrong-about-what-their-travel-credit-card-covers-302854100.html)). Kudos estimates people forget about $624/yr in benefits ([MWM](https://mwm.ai/apps/kudos-put-your-wallet-to-work/6443548838)).
- **Communities `[O]`:** r/CreditCards 1.56M, r/churning 674K, r/ChaseSapphire 211K, plus FlyerTalk.
- **How often the event happens:** in 2024, ~22% of US flights arrived late and ~1.4% were cancelled ([Experian citing DOT](https://www.experian.com/blogs/ask-experian/what-does-trip-delay-insurance-cover/)). With roughly 7M flights/yr from reporting carriers `[K]`, that's on the order of **~100k cancelled flights a year**, each stranding many passengers. Purchase, warranty and phone claims happen all year, independent of travel.
- **Keyword demand (est., low confidence):** "chase trip delay claim" ~1–3k/mo, "eclaimsline" ~5–15k/mo (mostly people navigating to the site), "trip delay insurance" ~5–10k/mo, "credit card extended warranty claim" ~1–3k/mo, "amex baggage delay claim" ~0.5–1k/mo. The long tail (card × incident × denial reason) is large, but each term is small.

**T4 — Reaching the user when the problem hits (score 5)**
- **Where the user is:** at the airport or a hotel during the delay, or 1–4 weeks later holding a denial email. They Google it (TPG and NerdWallet win) or post in r/ChaseSapphire or r/CreditCards.
- **First 90 days, no ads:**
  1. **Helpful replies** in r/CreditCards, r/ChaseSapphire, r/amex, r/VentureX and FlyerTalk claim threads, linking a **free coverage checker** (not the paid product).
  2. **One allowed front-page post in r/churning plus the weekly threads.** Their rules allow exactly one front-page promo per product; blog links must be text posts; new or negative-karma accounts are auto-removed ([rules](https://libredd.it/r/churning/wiki/rules), [Doctor of Credit](https://www.doctorofcredit.com/r-churning-kills-referral-threads-our-policy-going-forward/)).
  3. **Long-tail SEO pages** for denial reasons (e.g. "chase trip delay denied weather", "baggage delay receipt no date"), where the big blogs are thin.
  4. **Weather-disruption spikes:** storm days create hundreds of stranded travelers; publish "your card covers X" posts the same day.
- **Partners (later):** points bloggers (affiliate), AwardWallet-style newsletters.
- **Weakness:** we can't get in front of people *during* the delay without being installed or bookmarked beforehand. Most will find us after a denial. That makes **the appeal flow the real product**, not the first filing.

**T5 — Unit economics (score 5)**

| Item | Value |
|---|---|
| Pricing | **$19 per claim (includes one appeal)**, or **$49/yr Claims Pass** for unlimited claims across all cards |
| Success fee? | **No.** (1) A cut of the recovered money for helping with an insurance claim looks like **public adjusting**, a licensed activity in most states, with capped fees ([PA fee caps](https://publicadjusterauthority.com/public-adjuster-contingency-fee-limits-by-state), [UP](https://uphelp.org/claim-guidance-publications/questions-to-ask-before-hiring-a-public-adjuster/)). (2) We can't verify the payout. (3) Collecting after payout adds friction. Flat fee + self-help + we never contact the insurer = safest. |
| Conversion assumption | 3% of claim-page visitors pay; 8–10% of free coverage-check users pay |
| $3k/mo | ~158 claims/mo → ~5,300 visitors/mo (or ~1,700 checker users) |
| $10k/mo | ~526 claims/mo → ~17,500 visitors/mo |
| Marginal cost | About $0. Terms and rules are static data; PDF assembly runs in the browser; optional AI letter polish ≈ $0.01–0.05 per claim |
| Can T4 deliver it? | **$1–3k/mo by day 90 is plausible. $10k/mo by day 90 is unlikely.** Needs SEO to mature (6–12 months). |

**T6 — Pay trigger (score 8)**
1. The free **"Am I covered?"** check: pick card + incident + dates + expenses.
2. The result screen shows: **"Likely covered: up to $500/ticket · Est. reimbursable: $612 of your $680 · Deadline: Nov 14 (47 days) · 3 documents missing: itemized hotel folio, airline delay confirmation, card statement line."**
3. The paywall: **"Build my claim packet + deadline reminders + appeal letter if denied — $19."**

For people who were denied: they paste the denial reason, see "This denial reason is commonly reversed when you add X and Y" (from terms and outcome data), and the paywall offers the appeal packet.

**T7 — Pre-mortem: 3 likeliest ways to make $0 in 90 days (score 5)**
1. **Free substitutes win.** Users read the TPG guide, paste it into ChatGPT, and never pay. Many are exactly the DIY/spreadsheet type.
2. **We can't reach people when the problem hits.** SEO is too slow, Reddit threads remove our links, and the r/churning one-shot post flops.
3. **Data errors.** One wrong coverage statement or deadline gets screenshotted on Reddit and trust is gone. The benefit database is also larger than expected (issuer × network × card version).

**T8 — Risk (score 6)**
- **Liability if our information is wrong:** a denied claim or missed deadline. Mitigations: always show the source clause plus a link to the official benefit guide, date-stamp every term, add "not insurance advice", and require the user to confirm.
- **Licensing:** flat fee + self-help + no negotiating on the user's behalf. Get a one-hour lawyer review on public-adjuster and "insurance advice" risk before launch.
- **Privacy:** receipts and statements are sensitive. Default to **processing on the user's device**; don't store full card numbers; auto-delete after the packet is exported.
- **Platform dependency:** low (no APIs). Changes to administrator portals only affect our instructions.
- **Upkeep:** moderate. About 15 cards × 8 benefit types at launch; guides change about once a year per card. Budget 2–4 hours a week.

**T9 — Build reality (score 7):** 3–4 weeks for a solo dev with Claude Code.
- **Hardest piece:** building and checking the terms database accurately (LLM-assisted extraction from benefit PDFs + human review + version dates) and the "which card paid for it" edge cases (split payments, points bookings).
- **Everything else is standard web work:** a rules engine for coverage math, document checklists, drag-and-drop packet builder (in-browser PDF merge), email deadline reminders, templated appeal letters.

**T10 — What stops a weekend clone (score 6)**
1. **Versioned terms plus an outcomes dataset.** Every claim run through the product adds "denied for X → paid after Y" data that ChatGPT and blogs don't have. This is the only compounding asset among all 8 ideas.
2. **Long-tail SEO pages** built from that dataset.
3. **Reputation in 3–4 subreddits.**

Still clonable by Kudos, CardPointers or Pine AI if they decide it matters.

**Verdict: SURVIVE.**

---

### 3.2 HeirloomDraft ❌ (61)

**T1 — Competitors (score 3)**
- **[SaveOr](https://www.saveor.com/millennial-inheritance-management-app)** ($59.99/yr, 7-day trial; [App Store](https://apps.apple.com/us/app/saveor-home-inventory-app/id1575327496), positive reviews, count not visible). It already does: AI photo inventory with values, siblings privately marking what they want with **preferences revealed at the same time**, **"live, interactive distribution games for the whole family"**, court-ready PDFs, and estate-sale catalogs. It sells to senior move managers ([pro page](https://www.saveor.com/move-management-professionals)). **That is HeirloomDraft.**
- **[FairSplit](https://www.fairsplit.com/estate-division-solution/)** (since 2010): the free tier covers inventory and sharing only. The actual division rounds (interest review, emotional-points blind bidding, selection order) require paid plans at [$179.95/$289.95](https://www.fairsplit.com/plans/pricing-estate-division/). Distributed through Executorium and Estateably (estate-admin software used by professionals) ([Executorium](https://executorium.com/solutions/fair-split/)). Testimonials are strong.
- So FairSplit's free tier is *not* "good enough" for dividing items, but SaveOr fills that gap at a lower price.

**T2 — Substitute (score 5).** A shared Google Sheet with photos, a coin flip, and a **snake draft over Zoom** is standard advice from law firms ([Garrett Law](https://elderlawaustin.com/6-ways-to-divide-family-heirlooms-fairly/), [Estimonia](https://estimonia.com/blog/inherited-items/how-to-divide-inherited-items-fairly-between-siblings)). Blind point-bidding is the one part that's hard to do by hand.

**T3 — Demand (score 4).**
- 3.07M US deaths in 2024 ([CDC](https://cdc.gov/nchs/products/databriefs/db548.htm)).
- About 9,000 estate-sale companies × ~31 sales ≈ **~280k company-run estate sales a year** (derived from [EstateSales.net 2024 survey](https://www.estatesales.net/surveys/2024-industry-survey)).
- r/AgingParents has 84K members and r/inheritance 34K `[O]`. But **Reddit shows little direct "how do we split Mom's stuff" demand**; disputes there are mostly about money and real estate `[O]`.
- Keywords (est.): "how to divide personal property among siblings" ~500–1.5k/mo; "fairsplit" ~500–1k/mo.

**T4 — Reach (score 4).** The user is grieving and busy, and relies on the executor or an attorney. The fastest channels are B2B-ish (senior move managers, estate attorneys), which violate the B2C spirit and where SaveOr and FairSplit are already present.

**T5 — Economics (score 4).** $49 per estate → 62/mo for $3k, 205/mo for $10k. There's no fast channel to reach 200 families a month. Near-zero marginal cost (photo storage only).

**T6 (7):** after heirs are invited and have marked their interests, the paywall appears at "Run the draft".
**T7 (4):** (1) SaveOr is already there; (2) the executor never finds us; (3) families default to the free sheet + Zoom.
**T8 (7):** low liability (a family agreement, not legal distribution). Moderate privacy.
**T9 (7):** 2–3 weeks. Hardest piece: a real-time draft with fair ordering and handling ties in blind bids.
**T10 (3):** none. Invites spread the product but don't lock anyone in.

**Verdict: KILL.** SaveOr does the job and demand evidence is weak. Steelman in §6.

---

### 3.3 Pet Move Planner ❌ (56)

**T1 (score 2, fatal):** 7+ direct tools in 2026:
- [Passpaw planner](https://passpaw.com/pet-travel-planner): free, no account, personalized checklist; earns from health certificates.
- [Paws Abroad](https://www.pawsabroad.co/services): $147 DIY plan / $795 / $2,500+.
- [Pet Holiday Club](https://www.petholidayclub.com/blog/pet-travel-international-complete-guide-2026/): AI, 194 countries.
- [PawVoyage](https://apps.apple.com/us/app/pawvoyage/id6764784157): 30 countries.
- [Pet Passport: US-JP](https://apps.apple.com/us/app/pet-passport-us-jp-travel/id6762554040): bilingual, built for exactly our best route.
- [PadsPass](https://apps.apple.com/us/app/padspass/id6751719905), Animal Passport.
- The official [USDA APHIS country pages](https://www.aphis.usda.gov/pet-travel/us-to-another-country-export/pet-travel-us-japan).

**T2 (3, fatal):** APHIS pages plus a free Passpaw plan plus ChatGPT for date math cover 80%+ of the value.
**T3 (4):** Hawaii took in 8,804 dogs and cats in FY2007 (latest public figure found) ([HDOA](https://dab.hawaii.gov/blog/news-releases/news-release-nr07-18-september-7-2007/)). International volume is unknown. r/movingtojapan 149K, r/expats 260K `[O]`.
**T4 (6):** clear communities. Vets and military overseas-move groups.
**T5 (4):** $29–39 per move → ~90/mo for $3k. Plausible but capped by the small market.
**T6 (8):** the dated timeline with the "earliest possible travel date" is a strong result screen.
**T7 (4):** a free competitor, a small market, and a rules mistake that turns into a Reddit horror story.
**T8 (3):** **high liability.** A wrong rule means quarantine or a denied flight (the "$2k+ can't bring my dog to Japan" story `[O]`).
**T9 (5):** the rules database for 20+ countries plus airline rules is ongoing work.
**T10 (4):** only the rules database, and competitors already have one.

**Verdict: KILL.**

---

### 3.4 Family Cookbook ⚠️ CONDITIONAL (66)

**T1 — Competitors (score 3)**

| Competitor | Model | Price | Signals |
|---|---|---|---|
| [ReciScan](https://reciscan.app/) | Scan handwritten cards on your phone, then print or PDF | Free app; print from ~$18 (50 pages); $4.99/mo lowers to ~$13/book | Strong App Store reviews ("detected intricate writing") ([App Store](https://apps.apple.com/us/app/reciscan-cookbook-maker/id6478405196)) |
| [Family Cookbook Project](https://www.familycookbookproject.com/price_to_print_a_family_cookbook.asp) | Collaborative: invite relatives + AI recipe conversion + print from 1 copy | $7.95/mo or $99.95 lifetime + print | "Tens of thousands" of books printed; 33 Trustpilot reviews ([Cape Cod Life](https://capecodlife.com/create-family-cookbook/)) |
| [CreateMyCookbook](https://createmycookbook.com/books/pricing) | Designer templates + **"We Type It" from $5** | $19.95 spiral, $34.95 hardcover (100 pages) | Positive quality reviews |
| Mixbook, Heritage Cookbook, Morris Press | Photo-book editors / fundraiser printers | from $14.99 | Established |
| [Savor Custom Cookbooks](https://savorcookbooks.com/detailed-pricing) | Human luxury service (photoshoot + design) | **$2,900 base** (50% deposit $1,450), 4+ months | The "human service" we would undercut |

The exact job (collect from relatives + scan handwriting + print) is **already done by at least two products.**

**T2 — Substitute (score 5).** Etsy Canva template ($5–15) + ChatGPT to transcribe handwriting + a Google Form for relatives + print at Mixbook. That's 80% of the result but **5–15 hours of layout work**. A better product saves time and looks better. Worth $29? For some people, yes.

**T3 — Demand (score 7).** r/Old_Recipes has 551K members, plus real "how do I make grandma's recipe book" posts `[O]`. Many Etsy templates exist. FCP has printed tens of thousands of books. Keywords (est.): "family cookbook" ~5–10k/mo (seasonal Q4), "make your own cookbook" ~5–10k/mo, "recipe book template" ~10–20k/mo.

**T4 — Reach (score 6).** Relatives must contribute, so every contributor sees the product. Pinterest and TikTok gift content. The trigger moments are gifts (Q4), a death (the inherited recipe box), and bridal showers. r/Old_Recipes self-promo rules are unverified.

**Printed by Dec 25?**
- Lulu's print API takes 3–5 business days normally, **7–10+ in the holidays**, plus shipping ([Lulu](https://help.api.lulu.com/en/support/solutions/articles/64000254637-what-is-the-production-time-for-an-order-), [Lulu Jr](https://lulujr.com/blogs/lulu-junior-blog/holiday-shopping-production-delays)). So orders are due by about Dec 4–8.
- If we launch ~Nov 15, a customer has ~3 weeks to collect recipes from relatives and finish the book. **Unrealistic for most projects** (typical collection takes 2–6 weeks).
- **→ Digital-first** (PDF gift + "print coming in January" card).

**T5 — Economics (score 4).** Digital $29, print margin +$8–15 when ordered. Blended ~$32 → ~94 books/mo for $3k, ~313 for $10k. Marginal cost: handwriting OCR ~$0.01–0.03 per card via API (or on-device), print passed through. **The 90-day window (Nov–Jan) is mostly digital and gift-driven, with a post-holiday cliff.**

**T6 (7):** after 5+ recipes are in, a live preview of a real page with **grandma's handwriting kept beside the typeset recipe**. The paywall is "Unlock full book + PDF".
**T7 (4):** (1) projects stall while waiting on relatives, so payment slips past 90 days; (2) ReciScan and FCP are "good enough"; (3) post-holiday demand collapse.
**T8 (7):** low liability. Print-quality support burden. Family photos are only mildly sensitive.
**T9 (5):** 3–5 weeks. **Hardest piece: typesetting quality** (pagination, long recipes, image and handwriting layout) plus the print-API integration.
**T10 (3):** design taste and brand only. Easy to copy.

**Verdict: CONDITIONAL.** Only if a differentiated angle pulls real pre-orders in a 1-week test (§5).

---

### 3.5 PPM Companion ❌ (56)

**T1 (score 3):**
- [PCS Navigator](https://apps.apple.com/us/app/pcs-navigator/id6757585561): **100% free, no premium tier**; calculates PPM, DLA (dislocation allowance), TLE (temporary lodging expense), MALT (mileage allowance) and BAH (housing allowance) from 2026 JTR rates (the official travel regulations).
- [NextStation](https://nextstationapp.com/): 100+ task checklist, expense logging, **receipt upload**.
- Military PCS Calculator (Android, free, no ads) ([Play](https://play.google.com/store/apps/details?id=com.langsyslab.pcscalculator&hl=en_US)).
- [MyBaseGuide estimator](https://mybaseguide.com/tools/pcs-entitlements-estimator), [Garrison Ledger](https://www.garrisonledger.com/dashboard/tools/pcs-planner), [pcscalculator.net](https://www.pcscalculator.net/), [militarytoolkit](https://www.militarytoolkit.com/ppm-calculator).
- **MilMove** is the official channel for uploading weight tickets and receipts ([USMC fact sheet](https://www.iandl.marines.mil/Portals/85/Docs/LPD/Fact%20Sheet%20PPM%20Using%20MilMove.mil%20GHC%20JAN%202025.pdf)).

**T2 (3, fatal):** free apps plus official tools cover it. The pain is confusion `[O]`, which free content and helpful Facebook groups already handle.
**T3 (5):** real confusion posts `[O]`; r/MilitaryFinance 68K `[O]`. PPM volume isn't public (roughly ~300k DoD household-goods moves/yr `[K]`).
**T4 (6):** military-spouse groups are large and active.
**T5 (2, fatal):** free alternatives mean weak willingness to pay, and **peak season is May–Sep**, so a Nov–Jan window can't show payment.
**T6 (5):** the payout estimate is free elsewhere, so there's no unique result to paywall.
**T7 (3):** off-season; free apps; military users are price-sensitive.
**T8 (7):** low.
**T9 (9):** easiest build.
**T10 (2):** none.

**Verdict: KILL.** Revisit only as a free lead magnet or a spring-2027 side project.

---

## 4. New wildcard ideas (lens: one-off high-stakes event + DIY tool undercuts a $150–3,000 human service + finished outcome)

I pre-screened about 12 ideas and fully tested the 3 strongest.

**Pre-screen kills:**
- **Contractor-bid comparison:** [BidCompareAI](https://resident.com/tech-and-gear/2025/08/15/thwarting-home-renovation-regret-pioneering-ai-tool-transforms-bid-comparison) is free; EstimateHawk and Etsy tools exist.
- **Home-warranty denial appeals:** handled by law firms, JustAnswer and Pine AI. Out of scope.
- **Interstate moving-damage claims:** the FMCSA process is free and there's no pay evidence ([FMCSA](https://www.fmcsa.dot.gov/protect-your-move/resources/consumer-advisory-loss-and-damage)).
- **Health-insurance appeals and financial-aid appeal letters:** funded players already exist `[K]`.
- **Funeral programs and slideshows:** Etsy templates plus free phone slideshows.
- **Rental-car CDW claims:** folded into Card Claims (it's a card benefit).

### 4.1 W1 — DIY Estate Sale Kit ❌ (61)

- **Pitch:** a phone-first kit to run your own estate sale: photos → price suggestions → printable QR price tags → sale-day tally → end-of-sale report for the executor.
- **The undercut:** estate-sale companies charge about **40% commission** on average (up from 37% in 2021), average gross sales are ~$19.6k (2021), and companies turn down estates under **$5–10k** ([EstateSales.net 2024](https://www.estatesales.net/surveys/2024-industry-survey), [2021](https://www.estatesales.net/surveys/2021-industry-survey), [HomeLight](https://www.homelight.com/blog/estate-sale-company-faqs/)).
- **T1 (3):** [EstateSail](https://apps.apple.com/us/app/estatesail-estate-sale-manager/id6741873963) (AI pricing, barcode labels, checkout), [PROSALE](https://prosale.com/estate-sale-software) (labels + point-of-sale + payments), [StickerPrice](https://www.stickerpriceapp.com/) (QR point-of-sale for rummage and estate sales), [SaveOr estate sales](https://www.saveor.com/estate-sales), Squarea, Flippd, [MaxSold](https://support.maxsold.com/hc/en-us/articles/203144484-Is-there-a-fee-to-use-Maxsold) seller-managed (30% or $99 minimum), EstateSales.org private listings ($50).
- **T2 (5):** masking tape + a sheet + Facebook Marketplace + a $50 listing.
- **T3 (6):** the "too small for a company" segment is real.
- **T4 (4):** grieving families again, and no community gathered around this moment.
- **T5 (5):** $49–79 per sale.
- **T6 (6):** first printed tag sheet.
- **T7 (4):** people pay companies for the **labor and buyer lists**, not software.
- **T8 (6):** optional AI pricing mistakes could cost users money.
- **T9 (5):** label printing and sale-day mode.
- **T10 (3):** none.
- **Verdict: KILL.**

### 4.2 W2 — DIY Day-of Wedding Coordinator ⚠️ CONDITIONAL (63)

- **Pitch:** "A coordinator in a box" for couples who can't afford one:
  - a vendor-confirmation flow (arrival times, contacts, needs)
  - an auto-built minute-by-minute run-of-show (sunset, photo shot list)
  - **helper crew cards** (e.g. "Aunt Sue: gift table + card box, 4:30 pm")
  - a **live day-of mode** that pings helpers and vendors ("grand entrance in 5 min")
  - setup and teardown checklists
- **The undercut:** day-of coordinators cost $800–3,500, averaging ~$1,170–1,800 ([Fash](https://fash.com/costs/wedding-coordinator-cost), [Zola](https://zola.com/expert-advice/how-much-do-wedding-coordinators-cost)). ~2M US weddings/yr, averaging $34k ([Knot 2026 study](https://www.theknotww.com/press-releases/the-knot-worldwide-unveils-2026-real-weddings-study)).
- **T1 (4):**
  - For planners (B2B): [Timeline Genius](https://www.timelinegenius.com/) (includes day-of text reminders), That's The One ($55/mo), [TimelinePro](https://timelineproapp.com/).
  - For couples: [VowConnection](https://vowconnection.com/best-wedding-day-timeline-tools/) (free, dynamic timeline), [Perfect Wedding Timeline](https://www.perfectweddingtimeline.com/), and Zola/Joy/Knot planning tools.
  - **No one owns "helper crew + live day-of mode" for couples.**
- **T2 (3):** ChatGPT writes a wedding-day timeline in 60 seconds, and a shared Google Doc does the rest. Our live-cue and helper layer is the only real value beyond that.
- **T3 (7):** a huge market. r/Weddingsunder10k has 229K members ([GummySearch](https://gummysearch.com/r/Weddingsunder10k/)). The budget-wedding segment is exactly who skips a coordinator.
- **T4 (5):**
  - Budget-wedding communities and TikTok ("DIY wedding day timeline").
  - **Helpers and vendors invited into the tool** (each wedding exposes 10–20 people, many soon to plan their own weddings).
  - Wedding SEO is brutally competitive.
- **T5 (5):** $59 per wedding (one-time) → ~51/mo for $3k, ~170 for $10k. SMS cues cost ~$1–4 per wedding via Twilio (or free web push). **Timing:** Nov–Jan is engagement season, not wedding season. People buy 1–3 months before the wedding, so the 90-day window catches only Dec–Mar weddings (low season).
- **T6 (6):** after entering ceremony time and venue, the generated run-of-show plus helper cards appear; the paywall sits on "Share with crew + live day-of mode".
- **T7 (4):** (1) ChatGPT + Google Doc is "good enough"; (2) off-season launch; (3) couples who care about day-of logistics can already afford a coordinator.
- **T8 (6):** if the app fails on the day (a notification doesn't fire), that's a meltdown with the bride blaming us. Needs offline and printed backups.
- **T9 (7):** 2–4 weeks. Hardest piece: a reliable real-time live mode (push, SMS fallback, offline).
- **T10 (3):** helper invites spread the product but there's no data moat.
- **Verdict: technically KILL (63).** Kept only as a slot-3 placeholder with a strict kill-switch test (§5), because it's the highest-scoring wildcard and the "helper crew + live mode" gap is real.

### 4.3 W3 — Property-Tax Appeal Kit ❌ (57)

- **The undercut:** Ownwell takes 25–35% of savings; it ran 550k+ appeals in 2025, has 4.7★ from 3,000+ Google reviews, and raised a Series B in Feb 2026 ([College Investor](https://thecollegeinvestor.com/46127/ownwell-review/), [AppealDesk](https://www.appealdesk.com/blog/ownwell-pricing-review)).
- **T1 (2, fatal):** at least five flat-fee DIY tools already exist: [TaxFightBack](https://taxfightback.com/articles/competitor-comparisons/ownwell-alternatives) $79, [AppealMyTax](https://appealmytax.dev/vs/ownwell-alternatives) $49 (or $29 kits, all 50 states), [AppealDesk](https://www.appealdesk.com/compare/diy-appeal-alternative) $49 (3,100+ counties), [AppealSeal](https://www.appealseal.com/content/docs/appealseal-vs-ownwell) $100, HomeTaxAppeal, Abode Money.
- **T3 (8):** strong demand.
- **T4 (3):** SEO is saturated, and our window is off-season for most counties (Texas protests run April–May).
- **T9 (3):** county data per jurisdiction is hard.
- **Verdict: KILL.** It shows the DIY-undercut lens is being farmed too.

---

## 5. Proposed FINAL 3

### Slot 1 — Card Benefit Claims & Appeals ✅
- **MVP scope (3–4 weeks):**
  - **Cards (~15):** Chase Sapphire Preferred/Reserve, Amex Platinum/Gold, Capital One Venture X, Citi Strata Premier, Bilt, plus the major airline co-brands.
  - **Benefit types (4):** trip delay, baggage delay, purchase protection, extended warranty.
  - Rental-car CDW comes second (highest stakes, but the most complex documents).
  - Cell-phone and return protection follow.
- **Product:**
  1. Free "Am I covered?" checker.
  2. $19 claim packet (includes one appeal).
  3. $49/yr Claims Pass.
  4. Denial-reason → rebuttal playbook.
  5. Claim-window reminders.
- **Positioning:** "When the card's insurance says no." Lead with appeals, because that's when the pain and intent are highest `[O]`.
- **Open risks to test first:**
  1. Will r/CreditCards / r/ChaseSapphire allow links to a free checker?
  2. A one-hour legal check on public-adjuster and "insurance advice" rules.
  3. Build terms for 3 cards first and have 5 real claimants use it.

### Slot 2 — Family Cookbook ⚠️ (conditional)
- **Kill-switch test (1 week, before any build):** a landing page for one sharper angle than ReciScan or FCP. The best candidate: **"Grandma's handwriting, kept"**: a scanned-card-first, designed heirloom PDF, with relatives contributing via a text link (no account), $29 digital.
- **Pass bar:** ≥ 3% of visitors click "pre-order" from Pinterest, r/Old_Recipes and gift-idea traffic.
- **If it fails → drop the slot.**

### Slot 3 — DIY Day-of Coordinator ⚠️ (placeholder: score 63 is in the kill band)
- **Kill-switch test:** a landing page aimed at r/Weddingsunder10k and budget-wedding TikTok for "helper crew + live day-of mode". **Pass bar:** ≥ 3% pre-order click rate *and* ≥ 5 couples with weddings before March 2027 agreeing to try it.
- **If it fails**, I'd rather run a Round 2b wildcard search built around **T10 (a compounding data asset)** than fill the slot with a weak idea. The adjacent space with the best shape is other **"claims where outcome data helps"** in consumer finance.

**My honest recommendation:** commit to **Slot 1** now. Treat Slots 2–3 as experiments to run in parallel during Slot 1's build weeks, not as equal bets.

---

## 6. Steelman of the best idea I killed: HeirloomDraft

**The best case for it:**
- SaveOr is really a **home-inventory subscription app** ($59.99/yr, iOS, sold to senior move managers). Division is one feature among many.
- FairSplit is a **2010-era platform sold through attorneys and estate software**.
- **Neither owns the consumer moment "we have to split Mom's things this weekend"** as a brand.
- A **web link that needs no install for heirs**, a **one-time $49**, and a **"draft night" live experience** built for a video call (reveal animations, a fair-order explainer everyone trusts, a signed-off PDF for the executor) is a clear product.
- The market renews every year (3.07M deaths plus downsizing), and every heir is a new user who will face this again.
- It needs no data upkeep, is nearly free to run, and there's no liability.

**Why I still killed it:**
1. SaveOr already markets "live, interactive distribution games" and simultaneous preference reveal, so the only difference would be price and install friction.
2. Direct consumer demand is thin on Reddit `[O]`, and the reachable channels are professional (attorneys, move managers) where the incumbents already sit.
3. There's no moat; a clone is a weekend's work.

**What would change my mind:**
- SaveOr's App Store reviews show the division feature is weak or unused.
- **And** a landing-page test for "family draft night" gets ≥ 3% pre-order clicks from r/AgingParents and downsizing Facebook groups.

---

## 7. What I'd like from you before Round 3

1. **Approve Slot 1** (Card Claims & Appeals) as the primary finalist, or push back.
2. **Choose:** run the 1-week smoke tests for Slots 2–3, or have me do a Round 2b search for stronger wildcards (focused on ideas that build their own data over time).
3. **Optional:** if you can open network access to `trustpilot.com`, `apps.apple.com` (full review pages), `ahrefs.com` or Google Keyword Planner, and `reddit.com`, I can replace the estimated keyword volumes and review counts with measured ones.
