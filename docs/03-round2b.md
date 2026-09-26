# 03 — Round 2b: Filling Slots 2 and 3

- **Date:** 2026-09-26
- **Input:** Orchestrator decisions for Round 2b + two addenda `[O]` (direct page reads and Reddit)
- **Rubric:** same T1–T10, same weights (T2, T4, T5 count double, max 130), same bands:
  - **Survive:** ≥ 70
  - **Conditional:** 64–69
  - **Kill:** ≤ 63, or a fatal T1/T2

---

## 0. TL;DR (honest answer)

**Nothing else clears 70.** I tested 6 ideas in full and pre-screened 5 more. The highest score was **65** (Pet Insurance Claims & Appeals as a standalone product), and it only gets there because it reuses the Card Claims engine.

| Idea | Weighted /130 | Verdict | Killer test |
|---|---|---|---|
| Pet Insurance Claims & Appeals (standalone) | **65** | ⚠️ Conditional band. **Build as a module of Finalist #1**, not a separate product | T1: petclaimappeal.com ($19), pawsandappeals (done for you) |
| College Aid Offer + Appeal (wildcard) | 64 | ❌ Kill (fatal T1) | TuitionFit + Road2College already own the crowdsourced-offer database |
| IEP Service-Minutes Tracker (reframed) | 62 | ❌ Kill (fatal T1) | IEPDesk tracks services; IEP Says writes compensatory-services letters |
| Car-Deal OTD Price Check (wildcard) | 61 | ❌ Kill (fatal T1) | CarEdge: 77k+ verified OTD quotes, $79 AI negotiator |
| New-Build Deal Desk (wildcard) | 59 | ❌ Kill | T2: the builder usually pays the buyer's agent, so there's no human cost to undercut; NewHomeSource shows incentives free |
| Security-Deposit Recovery Kit | 55 | ❌ Kill (fatal T1 + T2) | Free AI state-specific demand-letter generators + California courts' free tool + 6 move-in photo apps |

**Recommendation:**
1. Treat **Card Benefit Claims & Appeals as the only finalist.**
2. Build it as a **claims engine with verticals**: cards → pet insurance → travel disruption and rental-car CDW. Don't force two weak standalone products into slots 2–3.
3. If you still want three separate products, I propose a **Round 2c with a different search heuristic** (§6). The DP-culture heuristic has mostly been harvested: every big data-point community I checked (college aid, car deals, retention offers, vet prices) already has a product capturing its outcomes.

**Best two anyway** (as you asked; §5): **(1) Pet Insurance Claims & Appeals** and **(2) New-Build Deal Desk**, each with the conditions that would have to be true.

---

## 1. What I applied

- Finalist #1 approved; flat fee, no success fee (kept).
- Your direct reads are taken as fact `[O]`: total-loss car appraisal, HVAC quote checking, property tax and HeirloomDraft are dead; SaveOr is confirmed.
- **Access limits** (same as before): only WebSearch works here, so review counts and keyword volumes are snippets or estimates `(est.)`.
- **Search heuristic from your note:** communities with a data-point-sharing culture around a money decision, where no product captures and structures the outcomes, and ideally where the rules change by version.

---

## 2. The three candidates you named

### 2.1 IEP Service-Minutes Tracker (reframed) ❌ 62

**Reframed pitch:**
- Parents log the services actually delivered against the minutes the IEP promises.
- The app flags gaps like "missed 34 hours of speech this semester".
- It generates a **compensatory-services request** and a **service-log records request**, plus a meeting-prep packet.
- Annual price, since IEPs renew every year.

**T1 — Competitors (2, fatal):**

| Competitor | What it does | Price | Notes |
|---|---|---|---|
| **IEPDesk** `[O]` | "Private records organizer… **track services**, goals & school communications" | **$39.99 lifetime** (iOS) | Indie; promoted on r/AppGiveaway, Sep 2026 |
| **[IEP Says](https://www.iepsays.com/)** | Upload the IEP and get a free analysis in under 5 minutes, a report card, a meeting guide, and **advocacy letters**. State-specific guides on **"IEP says 30 min, my child gets 15"**, **service-log requests**, and **compensatory services** | One-time analysis pass (price at checkout); free Learning-domain tier | Owns our exact search terms ([30 vs 15 min](https://www.iepsays.com/learn/iep-says-30-minutes-child-gets-15), [service logs](https://www.iepsays.com/learn/how-to-request-service-logs), [comp services](https://www.iepsays.com/learn/compensatory-services-special-education)) |
| **[My IEP Hero](https://myiephero.app/)** | AI IEP analysis, red flags, IDEA compliance check, **smart letter generator**, progress tracking, plus paid human advocates | Free; $29–49/mo Premium; $99/mo Hero | 50-state guides |
| **[Undivided](https://undivided.io/resources/undivideds-new-iep-assistant-common-parent-questions-3609)** (funded) | AI "IEP Assistant" (HIPAA-compliant), human Navigators, California focus | Membership | Strong California brand |
| **[Kidvokit](https://kidvokit.com/pricing/)** | AI IEP binder, timeline, Gmail import | $59–99/yr | Massachusetts pilot |
| Others | [IEP Advocate.ai](https://iepadvocate.ai/), [Arloa](https://www.arloa.ai/lp/iep), AdvocateIQ, SPED Goals app, [AbleSpace](https://www.ablespace.io/) (teacher side, gives families visibility) | — | — |

**T2 — Substitute (4).** IEP Says gives a free analysis plus the service-minutes explainers. Its own advice is "a notebook, a spreadsheet, or a notes app will work" for logging. ChatGPT drafts the compensatory-services letter from IEP Says' template.

**T3 — Demand (7).**
- ~7.5M students on IEPs `[K]`.
- Communities `[O]`: r/Autism_Parenting 107K, r/specialed 55K, r/Dyslexia 40K, r/ADHDparenting 33K.
- High-engagement posts (206↑/120 comments; 104↑/150).
- The creator post "IEP Service Minutes: The Math Nobody Taught You" confirms the pain.

**T4 — Reach (6).** Strong parent communities and Instagram/TikTok SPED creators. But IEP Says already ranks on the service-minutes keywords.

**T5 — Economics (4).** $49/yr → ~61 new subscribers/mo for $3k/mo in cash (and $3k *MRR* would need ~735 active subscribers).
- **The pay trigger needs weeks of logging, or the school's service logs, before "34 hours missed" can appear.** Most payments would land after the 90-day window.
- Marginal cost: low without AI; ~$0.05–0.20 per IEP parse with AI.

**T6 — Pay trigger (6).** In session 1 the only honest result is "Here's what the IEP promises per week, and here's the letter to request service logs." The strong "you're owed X hours" screen only arrives later.

**T7 — Pre-mortem (4):**
1. IEP Says and IEPDesk already fill the gap.
2. Parents stop logging after two weeks.
3. Schools delay the service logs, so there's nothing to show.

**T8 — Risk (4).**
- Advocacy itself is fine: there's no license for special-ed advocates in any state, and letters and record organizing are recognized non-legal activities ([COPAA](https://www.copaa.org/page/GuidelinesAdv), [research](https://pmc.ncbi.nlm.nih.gov/articles/PMC5560650)).
- **But** disability and diagnosis data about a child is "consumer health data" under laws like **Washington's My Health My Data Act**. That means separate opt-in consent, strict sharing limits, and a **private right of action** (users can sue directly) ([IAPP](https://iapp.org/resources/article/washington-my-health-my-data-act-overview), [Goodwin](https://www.goodwinlaw.com/en/insights/publications/2024/03/alerts-technology-hltc-my-health-my-data-act-mhmda)). That's heavy compliance for a solo founder.

**T9 — Build (6).** 3–4 weeks. Hardest piece: parsing IEP PDFs (formats vary by state and district) into per-week service minutes.

**T10 — Moat (5).** A "district X granted N comp-ed hours for Y" outcome dataset would be valuable, but it would be sparse, sensitive, and slow to build.

**Weighted:** 2 + 8 + 7 + 12 + 8 + 6 + 4 + 4 + 6 + 5 = **62 → KILL.**

**Nearest-competitor wedge (if forced):** "IEPDesk plus automatic weekly service-minute math plus district-level outcome data." Too thin to justify.

---

### 2.2 Security-Deposit Recovery Kit ❌ 55

**Pitch:** timestamped move-in/move-out photo evidence, a state-by-state rules engine (deadlines, itemization, 2–3× penalties), a demand letter, and a small-claims packet. **Pay trigger:** "Your landlord missed the 21-day deadline; you may be owed $1,850 plus up to 2×."

**T1 — Competitors (2, fatal):**
- **Free AI state-specific demand letters:** [Deposit Deadline](https://www.depositdeadline.com/tools/demand-letter-generator) ("references your state's exact deposit return laws, deadlines, and penalty statutes"), [AI Formatter](https://aiformatter.net/tools/security-deposit-demand-letter-generator) (free, unlimited), [terms.law widget](https://terms.law/Demand-Letters/ai-security-deposit-widget.html).
- **Paid:** [Ezel](https://ezel.ai/templates/security-deposit-demand) ($99 drafting, plus free state templates), Depositron (NYC, featured by Thomson Reuters) `[O]`, Pine AI ([guide](https://www.19pine.ai/blog/write-demand-letter-for-deposit)).
- **Official and free:** California Courts' "Demand letter for security deposit" program `[O]`.
- **Move-in/move-out evidence apps:** [TenantInspect](https://apps.apple.com/us/app/tenant-inspect-rental-report/id6450515110), [RentCheck](https://apps.apple.com/us/app/rentcheck/id1134017691), [MoveSnap](https://movesnap.app/), ViziSmart, [MoveInSnap](https://moveinsnap.com/), Tenby.
- Landlords already say "your renters are using AI to fight deposit deductions" (Aptly) `[O]`.

**T2 — Substitute (2, fatal).** A free state-specific letter plus phone photos plus the court's self-help center covers more than 80%.

**T3 — Demand (8).**
- Enormous pain `[O]`: "Ex-landlord claiming I owe an additional $1,790" (952↑ / 1,197 comments). Deposits of $5,200 and $3,200 withheld.
- Communities: r/Renters 183K, r/Tenant 93K.
- ~44M renter households `[K]`.

**T4 — Reach (5).** r/legaladvice (3.6M) bans promotion; "landlord kept deposit" search results are saturated.

**T5 — Economics (3).** $29 one-time against free rivals. Conversion would be tiny.

**T6 — Pay trigger (7).** The "you may be owed $X plus 2×" screen is strong, but the free tools show it too.

**T7 — Pre-mortem (3):** free generators win; big states have official free tools; we can't rank in search.

**T8 — Risk (4).**
- DoNotPay's FTC order (Feb 2025: $193k, a ban on "AI lawyer" claims, required notice to past subscribers) ([FTC](https://www.ftc.gov/news-events/news/press-releases/2025/02/ftc-finalizes-order-donotpay-prohibits-deceptive-ai-lawyer-claims-imposes-monetary-relief-requires)) shows the line.
- Self-help document prep is generally OK if we make **no** lawyer-equivalence claims, but unauthorized-practice-of-law rules vary by state.
- **An outcome database keyed by landlord name** (the only real moat) brings user-content moderation and defamation risk, which violates H4.

**T9 — Build (7).** 2–3 weeks; the 50-state rules table is the work.

**T10 — Moat (4).** Rules tables are public and copyable, and the landlord-outcome data is legally risky.

**Weighted:** 2 + 4 + 8 + 10 + 6 + 7 + 3 + 4 + 7 + 4 = **55 → KILL.** Commoditized, exactly as your addendum predicted.

---

### 2.3 Pet Insurance Claims & Appeals ⚠️ 65 (standalone) → **decision: MODULE of Finalist #1**

**Pitch:** policy-version terms per insurer + denial reason → rebuttal playbook (pre-existing, bilateral conditions, waiting periods, "curable") + a vet-records evidence packet + appeal deadlines + an outcome dataset.

**T1 — Competitors (3):**
- **petclaimappeal.com**: $19 one-time appeal letter, insurer-specific landing pages (e.g. "Fight your Trupanion denial for pre-existing condition"), claims 48% of appeals succeed and 0.2% of people file `[O]`.
- **pawsandappeals.com**: done-for-you appeal service `[O]`.
- Pine AI (generic disputes).
- **No one has a structured, policy-version-aware outcome dataset.**

**T2 — Substitute (4).** ChatGPT plus the policy PDF plus a Reddit playbook ("Best Practices for Appealing Pre-Existing Condition Denials" `[O]`).

**T3 — Demand (6).**
- **7.6M insured pets** in North America at end-2025, up 9% YoY ([dvm360/NAPHIA](https://www.dvm360.com/view/us-pet-insurance-enrollment-increased-9-in-2025-but-more-than-95-of-cats-and-dogs-remain-uninsured)).
- About 18% of recent claimants reported problems (82% had none; MarketWatch via [Money](https://money.com/pet-insurance-claim-denied-what-to-do/)).
- Real playbook culture on r/petinsurancereviews, and emotional posts like "lost my baby boy… now they're denying claims" (190↑) `[O]`.

**T4 — Reach (5).** r/petinsurancereviews, breed subreddits (Frenchies and bulldogs have the most claims), vet-clinic front desks (later).

**T5 — Economics (4).** $19–29 per appeal. The market is smaller than cards (fewer claimants, rarer denials).

**T6 — Pay trigger (7).** "Your denial cites 'pre-existing'. Your policy's version defines it as X; the vet note from [date] says Y. Appeals on this reason are often won by adding Z."

**T7 — Pre-mortem (4):** petclaimappeal owns the insurer-specific search terms; the market is small; grief makes it hard to market.

**T8 — Risk (6).** Animal records aren't human health data. Keep the flat fee and self-help (same public-adjuster logic as #1).

**T9 — Build (7).** Standalone it's 3 weeks. **As a module it's about 1 week**, since it reuses #1's engine (terms database, evidence packet, deadline reminders, rebuttal playbook, outcome capture).

**T10 — Moat (6).** Policy versions per insurer (~15 insurers) plus outcomes compounds the same way #1 does.

**Weighted:** 3 + 8 + 6 + 10 + 8 + 7 + 4 + 6 + 7 + 6 = **65.**

**Standalone vs. module: MODULE.**
- As a standalone it only scores 65 and competes head-on with a $19 incumbent.
- As a second vertical of #1 it costs about a week, shares the outcome engine, and opens a second search cluster and community. It also **proves the engine generalizes**.
- Ship it in month 2–3 after card claims validates.

---

## 3. My wildcards (data-point-culture heuristic)

**Pre-screen** (killed quickly, one line each):
- **Credit-card retention offers:** free data-point databases already exist ([Travel on Points](https://travel-on-points.com/current-retention-offers-amex-chase-citi/), [Miles to Memories](https://milestomemories.com/retention-offer-amex-chase-citi/), [Thrifty Traveler's free tool](https://thriftytraveler.com/news/credit-card/amex-platinum-credits-tracker/)). At most a feature inside #1.
- **Vet procedure prices:** [VetPrice](https://getvetprice.com/), [Vet Receipt](https://vetreceipt.com/) (verified-invoice database), Veterinary Cost Guide, PawFig.
- **Nanny rates, contracts and payroll:** Poppins ($49/mo, 4.9 from Forbes Advisor), HomePay, NannyKeeper ([comparison](https://fitsmallbusiness.com/best-nanny-payroll-service/)).
- **Severance negotiation, VA disability, PSLF/IDR, health-insurance appeals:** legal, accreditation, or debt-relief regulation (H4).
- **Travel disruption (airline commitments, DOT refund rules, goodwill compensation):** strong data-point culture, but it overlaps #1. **Folded into #1 as a vertical.**

### 3.1 College Aid Offer Compare + Appeal ❌ 64 (fatal T1)
**Pitch:** upload aid offers, compare them against crowdsourced outcomes by school and student stats, see which schools "match" competing offers, and generate an appeal packet.

**Why it looked right:** high stakes ($20–80k a year × 4 years), a strong data-point culture (College Confidential, r/ApplyingToCollege), rules that change by version (the FAFSA SAI formula, each school's CSS/institutional methodology, the Common Data Set every year), and the season falls inside our window (early-decision offers arrive in December).

**T1 (2, fatal):**
- **[TuitionFit](https://tuitionfit.org/how-it-works/)**: anonymized award letters, crowdsourced "what similar students got", free comparison, $49 services.
- **[Road2College](https://www.road2college.com/)**: Paying for College 101 Facebook group with **~254K members**; R2C Insights at $24.99/mo *including crowdsourced offers*; My College Offers.
- [College Aid Pro](https://collegeaidpro.com/mycap-premium-new-pricing/) ($4.99/mo, appeals); [SwiftStudent](https://formswift.com/swift-student) (free appeal letters); MeritMore; [CollegeLens](https://collegelens.ai/resources/aid-appeals/financial-aid-appeal-success-rates-what-the-data-sh) (appeal success data).

**The rest:** T2 4, T3 8, T4 5 (the biggest community is owned by a competitor), T5 5, T6 7, T7 3, T8 7, T9 5, T10 4 (the database already exists elsewhere).

**Weighted:** 2 + 8 + 8 + 10 + 10 + 7 + 3 + 7 + 5 + 4 = **64 → KILL.** It technically lands in the 64 conditional band, but the fatal T1 overrides that.

### 3.2 Car-Deal OTD Price Check ❌ 61 (fatal T1)
**T1 (1):** **[CarEdge](https://caredge.com/reports/state-of-dealer-fees)** has 77,000+ *verified* out-the-door quotes (extracted from quote images) with dealer ratings for 23,000+ dealers. It offers a $79 AI negotiator, Pro at $49/mo, and a $999 human concierge ([pricing](https://www.carwhere.com/guides/caredge-review)). TrueCar and Edmunds are also there. The data-point database this heuristic looks for already exists at scale.

**The rest:** T2 4, T3 9, T4 4, T5 5, T6 7, T7 3, T8 7, T9 5, T10 3.

**Weighted:** 1 + 8 + 9 + 8 + 10 + 7 + 3 + 7 + 5 + 3 = **61 → KILL.**

### 3.3 New-Build Deal Desk ❌ 59
**Pitch:** for production-builder buyers (Lennar, D.R. Horton, Pulte…):
- a buydown vs. price-cut vs. closing-credit calculator
- advertised incentives plus **negotiated outcomes** by builder, community and month
- a negotiation email/packet
- a preferred-lender vs. outside-lender comparison

**Why it looked right:**
- 679k new homes were sold in 2025, and the top 10 builders closed 43.6% of them ([NAHB Eye on Housing](https://eyeonhousing.org/2026/07/top-ten-builder-market-share-falls-in-2025/)).
- Incentives are worth $10–40k and change monthly or quarterly (a versioned rule set).
- **I found no crowdsourced tracker of negotiated outcomes.**

**T1 (5):**
- [NewHomeSource](https://www.newhomesource.com/communities/tx/houston-area?hotdeals=true) "Hot Deals" shows *advertised* incentives per community for free.
- [Conrad](https://www.theconradapp.com/blog/home-builders-offering-low-interest-rates) routes buyers to specialized agents and lenders.
- Agent-built scorecards exist ([LRG Realty](https://lrgrealty.com/lrg-blog/new-build-deal-scorecard/)).
- Negotiated outcomes are **uncaptured**.

**T2 (3):** in new construction **the builder usually pays the buyer's agent**, so the "human service" costs the buyer nothing. ChatGPT handles the buydown math.

**T3 (5):** real money at stake, but I could only find data-point threads on Blind, not Reddit (needs your Reddit check).

**T4 (4):** hyperlocal community Facebook groups; agents dominate the channel.

**T5 (4):** $79 one-time per purchase → ~38/mo for $3k.

**T6 (6):** "Builder offered a $15k buydown; the same money as a price cut saves you $X over 7 years; buyers in this community got $Y more in Q3."

**T7 (4):** we can't collect outcomes fast enough; agents give better free help; there's no community with a data-point culture.

**T8 (6):** calculators and information are fine; we must not act as a broker.

**T9 (5):** per-community incentive data (scraping builder sites is fragile).

**T10 (6):** the negotiated-outcomes database would compound, but only if we can collect it.

**Weighted:** 5 + 6 + 5 + 8 + 8 + 6 + 4 + 6 + 5 + 6 = **59 → KILL.**

---

## 4. Round 2b scorecard (all ideas tested)

| Idea | T1 | T2×2 | T3 | T4×2 | T5×2 | T6 | T7 | T8 | T9 | T10 | **/130** | Verdict |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **Card Claims & Appeals** (Round 2, for reference) | 6 | 4 | 7 | 5 | 5 | 8 | 5 | 6 | 7 | 6 | **73** | ✅ Finalist #1 |
| Pet Insurance Claims & Appeals | 3 | 4 | 6 | 5 | 4 | 7 | 4 | 6 | 7 | 6 | **65** | ⚠️ → Module of #1 |
| College Aid Compare + Appeal | 2 | 4 | 8 | 5 | 5 | 7 | 3 | 7 | 5 | 4 | **64** | ❌ (fatal T1) |
| IEP Service-Minutes Tracker | 2 | 4 | 7 | 6 | 4 | 6 | 4 | 4 | 6 | 5 | **62** | ❌ (fatal T1) |
| Car-Deal OTD Check | 1 | 4 | 9 | 4 | 5 | 7 | 3 | 7 | 5 | 3 | **61** | ❌ (fatal T1) |
| New-Build Deal Desk | 5 | 3 | 5 | 4 | 4 | 6 | 4 | 6 | 5 | 6 | **59** | ❌ |
| Security-Deposit Kit | 2 | 2 | 8 | 5 | 3 | 7 | 3 | 4 | 7 | 4 | **55** | ❌ (fatal T1+T2) |

---

## 5. Best two anyway, and what would have to be true

### 1) Pet Insurance Claims & Appeals (65), strongest as vertical #2 of Finalist #1
**Wedge vs. petclaimappeal.com:** they sell a one-off letter. We would sell **policy-version-aware coverage checks, vet-record evidence packets, deadline tracking, and a denial-outcome dataset**, shared with the card engine.

**What would have to be true:**
1. petclaimappeal's traffic and conversions are real but its letters are generic; its reviews complain about weak letters. We can check this with direct page reads.
2. r/petinsurancereviews and breed subreddits let us share a free "Is this denial beatable?" checker.
3. At least 20 users submit their denial outcome in the first 60 days, so the dataset starts compounding.
4. Enough appealers per month exist. There are 7.6M insured pets and ~18% of recent claimants report issues, but petclaimappeal says only ~0.2% of people file appeals today `[O]`. So the reachable pool is probably low tens of thousands of appeals a year. That's plausible for $1–3k/mo, not $10k (estimate, low confidence).

### 2) New-Build Deal Desk (59), the only one with a truly uncaptured dataset
**Wedge vs. NewHomeSource and Conrad:** they list *advertised* incentives or sell agent referrals. We would publish **negotiated** outcomes by builder, community and month, plus buydown math that exposes the true cost of preferred-lender incentives.

**What would have to be true:**
1. A data-point culture actually exists in builder-community Facebook groups and r/FirstTimeHomeBuyer (can you check Reddit?).
2. A meaningful share of new-build buyers go without an agent after the 2024 NAR settlement, or distrust the builder's preferred lender.
3. We can collect 100+ negotiated outcomes in one metro (e.g. Houston or DFW) within 60 days.
4. Buyers pay $79 despite free agent help.

I'd give it maybe a 1-in-5 chance.

---

## 6. What I recommend next

1. **Go to Round 3 (execution plan) with Finalist #1 only**, built as a **claims engine**:
   - **v1:** 15 cards × 4 benefit types (trip delay, baggage delay, purchase protection, extended warranty).
   - **v1.5:** rental-car CDW, cell-phone protection, and travel disruption (airline commitments, DOT refund rules).
   - **v2:** the pet-insurance vertical (about 1 week of work).
   - Each vertical is its own search cluster and community, sharing one outcome database.
   - This gives you "three bets" in effect, with one codebase and one compounding moat. That's the right shape for a solo builder.
2. **If you want three separate products**, run a **Round 2c with a different heuristic.** The data-point heuristic is mostly harvested; every big community I found already has an outcome product. Candidate heuristics:
   - **Rules that change by version where the official source is unusable**: state, federal or issuer rulebooks that change yearly and that consumers must decode themselves.
   - **Forced multiplayer plus physical fulfillment**: products where invites are the distribution and a printed or shipped item is the moat.
3. **To upgrade the evidence**, allow `reddit.com`, `apps.apple.com`, `trustpilot.com` and `ahrefs.com` in the network settings, or share direct-read results, especially petclaimappeal.com's reviews and traffic, and new-build data-point threads.
