# 01 — Research & Candidates (Round 1)

- **Date:** 2026-09-26
- **Phase:** Ideation only (no application code)
- **Goal:** 3 B2C products a solo builder with AI coding tools can ship as an MVP in 2–6 weeks, where consumers pay within ~90 days of launch.
- **This round:** research → 25 candidates → kill list → top 10.

---

## 0. TL;DR

**The main finding: in late 2026, almost every obvious "tracker/organizer for hobby X" niche already has 3–8 new apps.** AI coding tools make building cheap for everyone. For horses, beekeeping, reptiles, HSA receipts, nomad tax days, summer camps, Costco price drops, trail cams, Disney pins, wedding RSVPs and more, I found several 2025–26 apps each (links in §2.1). So "nobody has built this" is almost never true anymore. What still decides a winner:

1. **An outcome, not a log**: money back, a finished document or book, a fair result between people.
2. **Distribution built into the product**: other people must be invited, or there is a tight community or a high-intent search term.
3. **Something a weekend clone can't copy fast**: compiled rules or data, print or typesetting quality, trust in an emotional moment.

**Top 10 after the kill pass** (details in §6):

| Rank | Idea | One line |
|---|---|---|
| 1 | **HeirloomDraft** | Siblings split a parent's belongings fairly (estate or downsizing): photo inventory, then a blind "wish" round, then a turn-based draft. |
| 2 | **Family Cookbook** | Text relatives a link, they snap grandma's recipe cards, and you get a beautiful PDF or printed book. |
| 3 | **Card Benefit Claims Kit** | "Your flight was delayed 7h. Your card owes you up to $500. Here's the exact claim packet." |
| 4 | **Marriage Evidence Binder** ⚠️ | Photos, chats and joint documents become a dated, indexed exhibit PDF for I-130 / I-751 / K-1 filings (needs your ruling on hard constraint H4). |
| 5 | **Pet Move Planner** | A dated, step-by-step plan for moving a dog or cat to Japan, Hawaii, the UK, the EU or Australia. |
| 6 | **DIY Recruit** | Recruiting tracker for families who won't pay NCSA $2–6k. |
| 7 | **IEP Parent Binder** | Parent-side organizer for special-ed plans, services delivered, and meeting prep. |
| 8 | **PPM Companion** | Military do-it-yourself move: payout estimate, weight-ticket checks, receipts, 45-day deadline. |
| 9 | **Private-School Admissions Organizer** | For NYC/SF/LA/Boston K–12 applications. Consultants charge about $12k. |
| 10 | **Custom-Home Build Tracker** | Allowances, change orders and payment stages for homeowners building a house or barndominium. |

Kill list: **15 of the 25 candidates** (§5), plus about 20 ideas killed early (§7).

---

## 1. Method and limits

- **Sources used:** WebSearch and WebFetch (App Store listings, Etsy listings, competitor pricing pages, forums such as Bogleheads, Rokslide, Soapmaking Forum, Disney Pin Forum and MorphMarket Community, and blog comparisons).
- **Reddit was blocked** from this container (CONNECT 403). Search engines also barely index Reddit threads right now. Reddit and YouTube evidence therefore comes from the **orchestrator's parallel research** (§2.3). I treat it as second-hand: the revenue numbers there are self-reported or estimated, not verified by me.
- **Evidence labels used below:** `[S]` = found in this round's searches (link given). `[O]` = orchestrator input (unverified). `[K]` = my prior knowledge (not re-verified this round; flag it if it matters).
- **Competitor strength** is judged from what the search surfaced (age, pricing, funding, review snippets). I did **not** pull App Store review counts or keyword rankings for every competitor. That belongs in Round 2 for the finalists.

---

## 2. Research notes

### 2.1 The 2025–26 flood: niches that are now crowded

Every row below was a plausible "underserved niche" a year or two ago. Each now has multiple dedicated products, most launched in 2025–26.

| Niche | What I found | Links |
|---|---|---|
| Horse care records | HorseBook ($9.99/mo), HorseKeeper, EquineGo (free), My Cheval, Horse Tracker | [HorseBook](https://apps.apple.com/us/app/horsebook-equine-records/id6759075592), [EquineGo](https://www.equinego.com/), [My Cheval](https://www.mycheval.com/) |
| Beekeeping logs | HiveTracks (~$24/yr, long-running), HiveBook, HiveSense, ApiNote, Apiary Book | [comparison](https://tryhivesense.com/blog/best-beekeeping-apps-2026), [HiveTracks](https://apps.apple.com/us/app/hivetracks/id1667408004) |
| Reptile husbandry | Husbandry.Pro (MorphMarket-linked), Shed, ReptiCare, Monty | [Husbandry.Pro](https://husbandry.pro/), [Shed](https://apps.apple.com/us/app/shed-reptile-feeding-tracker/id6761770562) |
| HSA "shoebox" receipts | Shoebox ($120/yr), HSA Store ExpenseTracker, Reimbursable, HSA Trackr, HSA Monster, TrackHSA… | [roundup](https://triplapp.com/blog/best-hsa-tracker-apps), [HSA Store PR](https://www.prnewswire.com/news-releases/still-saving-paper-receipts-in-a-shoebox-simplify-your-tax-free-health-savings-account-hsa-funds-with-the-hsa-expensetracker-app-from-hsa-store-302602816.html) |
| Nomad tax / Schengen day counter | Days of Stay, iReside, Nomad Tracker, NomadDays, Domicile365, TrackingDays… | [Days of Stay](https://apps.apple.com/us/app/days-of-stay-tax-schengen/id6753990603), [iReside](https://www.ireside.ai/) |
| Summer-camp planner | summer-camp-planner.com (free, 19,500 camps catalogued) plus many sheets | [site](https://summer-camp-planner.com/) |
| Costco price adjustments | CostPal, CostLow, CostRefund | [CostPal](https://www.costpal.app/), [CostRefund](https://costrefund.com/blog/costco-online-price-adjustment-form) |
| Disaster contents claims | Bevel (free), ClaimSight, Contents360, CostCam, HomeZada AI | [NBC LA on Bevel](https://www.nbclosangeles.com/news/local/bevel-new-app-helps-document-belongings-disaster-palisades-fire/3800554/), [ClaimSight](https://claimsight-ai.vercel.app/) |
| Campsite cancellation alerts | Campnab ($10–90/mo), Campflare, Outdoorithm, HutAlert, OpenCampsite; also Recreation.gov's own alerts | [Campnab](https://campnab.com/), [comparison](https://www.opencampsite.com/alternatives) |
| Trail-cam photo sorting | onX Hunt, DeerLab, BuckSort, BuckOracle, Trakkdown | [Trakkdown](https://www.trakkdown.com/), [DeerLab](https://deerlab.com/) |
| Disney pins | Pin Trading Scan & Collect, MagicPin, My Pin Tracker, Pin&Pop, iCollect Everything | [Disney Pin Forum](https://www.disneypinforum.com/threads/alternative-to-pinpics.75303/) |
| Hot Wheels (after Mattel's app shut down) | Diecast ID, Hunt64 | [Mattel FAQ](https://shop.mattel.com/pages/hot-wheels-id-faqs), [Hunt64](https://apps.apple.com/app/id6757083316) |
| South Asian multi-event weddings | Joy, Invyt, The Curated Knot (free), Wedd.ai, itsmy.wedding | [Curated Knot](https://thecuratedknot.com/blog/best-rsvp-apps-indian-weddings-2026), [Joy](https://withjoy.com/blog/how-to-manage-multiple-wedding-events-with-different-guest-lists-for-indian-weddings/) |
| Maker recipe costing (soap/candle) | Craftybase ($24–49/mo), Ardent Seller (free, all features), Inventora | [Ardent Seller](https://www.ardentseller.app/compare/craftybase-alternatives/), [MicroGaps](https://www.microgaps.com/blog/craftybase-alternative-etsy-sellers-cogs-tracking) |
| Dog-sport titles | AgilityNerd tracker, Dog Title Tracker, Agility Coach | [AgilityNerd](https://www.agilitynerd.com/blog/agility/web/sites/akc-title-and-event-goal-tracker-released/) |
| Metal detecting | Aureal, WhereToDetect, Rodek, FieldFinders | [WhereToDetect](https://wheretodetect.com/), [Aureal](https://aureallabs.com/) |
| Star-note / fancy-serial checkers | 6+ free sites plus the MyCurrencyCollection app | [starnotecheck](https://starnotecheck.com/), [lookupstarnote](https://www.lookupstarnote.com/) |
| Cross-stitch PDF markup on iOS | Markup R-XP, Cross Stitch Club, Stitchberry, GourdCraft | [Lordlibidan roundup](https://lordlibidan.com/the-best-apps-for-cross-stitchers/) |
| Embroidery file organizers | 2stitch (27k users), Embroidery Grove, StitchBuddy | [2stitch](https://www.2stitch.com/) |
| Nurse multi-state CE tracking | CE Broker, Nursa (free), License Tracker (free), CeMe | [Nursa](https://nursa.com/blog/best-ce-tracker-app-for-nurses) |
| Daycare waitlists (parent side) | WaitNest | [WaitNest](https://apps.apple.com/ca/app/waitnest-daycare-waitlist-app/id6761996670) |
| Hotel price-drop rebooking | Pruvo went B2B-only in June 2026; Rebookly, HotelPriceTracker (free), StaySaavy… | [Rebookly](https://rebookly.ch/pruvo-alternative) |

**What this means:**
- A plain tracker in a hobby niche is now a commodity. Several apps are one-time purchase or free, so there is little price room left.
- Most new entrants are **thin** (few reviews, no community presence). That does *not* fail your C6 by itself (C6 = a *well-reviewed app dominates the keyword*). But it means we need a wedge the clones lack: distribution, data/rules, output quality, or trust.
- Ideas that survive in §6 mostly share one trait: **the user walks away with a result** (a fair split, a book, a claim packet, an exhibit PDF, a dated plan), not just a place to type things.

### 2.2 Where the real pay signals are

Four kinds of evidence showed up repeatedly as "people already spend money here":

1. **Etsy and Gumroad templates for a painful one-off job.** Editable Canva family cookbooks ([example](https://www.etsy.com/listing/1655650136/canva-cookbook-template-family-recipe), [market](https://www.etsy.com/market/cookbook_template)), parent IEP binders ([example](https://www.etsy.com/listing/4475456303/parent-iep-binder-printable-special)), "in case of death" binders (one seller reports 5,000+ sold: [market](https://www.etsy.com/market/death_binder)), college-recruiting spreadsheets ([listing](https://www.etsy.com/listing/1405716628/the-best-college-recruiting-spreadsheet)), marriage-evidence templates for USCIS ([listing](https://www.etsy.com/listing/4328945789/marriage-evidence-immigration-template)), wedding vendor-payment trackers ([listing](https://www.etsy.com/listing/1222359758/wedding-vendors-contact-and-payment)). Spreadsheets overall are a big Etsy category. One 2026 seller guide says "The Weekly Crew" made 62,000+ sales from 29 listings. That comes from search summaries of these guides ([Sellfy](https://sellfy.com/blog/sell-excel-google-spreadsheets/), [Insight Agent](https://www.insightagent.app/guides/how-to-sell-spreadsheets-on-etsy)), not from a primary source.
2. **An older paid tool with customers who could switch.** FairSplit ($179.95–$289.95 per estate since 2010, [pricing](https://www.fairsplit.com/plans/pricing-estate-division/)). Craftybase ($24–49/mo). Evans/KinTraks desktop pedigree software for rabbit breeders ([Everbreed comparison](https://everbreed.com/blog/rabbit-pedigree-software/)). HiveTracks. goHUNT ($120–150/yr).
3. **A human service with a big price tag (a DIY tool can undercut it).** NCSA recruiting ($2,000–6,000+, [NextCommit](https://www.nextcommit.ai/blog/ncsa-cost)). NYC private-school consultants ($12,000/child, [School Search NYC](https://schoolsearchnyc.com/services/individual-consultations/)). Pet relocation (Paws Abroad concierge $795, white-glove $2,500+, but a **DIY plan at $147**: [pricing](https://www.pawsabroad.co/services)). Immigration lawyers. Special-ed advocates.
4. **"Money that already belongs to you."** Credit-card protections go unused: 62% of travelers are wrong about what their card covers ([PR Newswire](https://www.prnewswire.com/news-releases/new-data-shows-62-of-travelers-are-wrong-about-what-their-travel-credit-card-covers-302854100.html)), and 2 in 5 don't know their travel benefits ([WalletHub](https://wallethub.com/blog/credit-card-travel-benefits-survey/51766)). Military PPM payouts get lost to missing weight tickets or receipts ([Half Price Movers](https://www.halfpricemovers.com/blog/common-ppm-mistakes-cost-service-members-reimbursement)). HSA reimbursements. Costco price adjustments.

### 2.3 Indie revenue patterns: orchestrator input, with my pushback

Orchestrator input `[O]`, summarized:
- **25 iOS apps at $10k+ MRR (2025):** niche audience, then an instant personalized result, then the paywall on that result. "Found money" apps (Settlemate ~$700K, PayMe ~$300K). Niche collector scanners (VinylSnap, NoteSnap, AntiqSnap, Cardly) at $2–3+ per download. Forced-multiplayer party game (Imposter Who). TikTok as the funnel. Zero-variable-cost apps net ~2× what AI-wrapper apps net.
- **Escape** (solo iOS): about $6k/mo by month 5. The driver was ranking #1 for a high-intent App Store keyword. About 10% of downloads became paid.
- **DayZen:** Reddit hated a subscription on a simple utility. A lifetime price converted better.
- **App factory:** 74 apps earning ~$7k MRR, heavily top-heavy; the founder could not predict which apps would win.
- **Generic apps** (timers, water trackers) struggled. Niche down hard.
- **Counter-signal:** a Claude-built app got 100k views and made $0.
- **HoloDex** (TCG scanner): $5.8M gross in 12 months, but EBITDA −$172k because of paid-ads dependency and a TCGPlayer data dependency. An M&A expert would pass at $10M.

Other data points I found `[S]`:
- **PreQuilt** (quilt design, two-person team: a quilter plus a developer). Subscription $7.50/mo or $50/yr. Their success target was 1,000 subs at $5/mo ([IH](https://www.indiehackers.com/post/55d96e57af), [plans](https://app.prequilt.com/plans)). Pattern: a founder from the hobby, a visual result, and a small subscription.
- **Seedtime** (garden planner): bootstrapped. The Kickstarter was funded in 10 minutes. Now 400k+ users ([Tracxn](https://tracxn.com/d/companies/seedtime/__7-cyXuIHlg-4URHn3ZW74egrEMvkuwBqP4uJrnMG6yI), [The Packer](https://www.thepacker.com/news/packer-tech/breaking-ground-how-seedtime-app-revolutionizing-agtech)). Pattern: a community-funded launch inside a tight hobby.
- **Solo app portfolio** (Sebastian Roehl): $602K in 2025, $28K MRR from ~25k subscribers. It took 2.5 years to reach $10k MRR ([buildmvpfast](https://www.buildmvpfast.com/blog/602k-revenue-solo-indie-hacker-app-portfolio-breakdown-2026)). Reality check on timelines.
- **Paws Abroad** sells a $147 DIY plan next to $795–$2,500 services. This is the "DIY tier undercuts the human service" pattern, live.

**Where I push back on the orchestrator input:**
1. **The collector-scanner pattern breaks your C3.** VinylSnap, NoteSnap, AntiqSnap and HoloDex pay per scan for cloud vision calls and rely on price data they don't own. HoloDex is the proof that this growth runs on paid ads. Also, **this exact pattern is being farmed right now**: I found scanner or tracker apps for Disney pins, Hot Wheels, Pyrex ([PyrexVault](https://pyrexvault.com/), free), antiques ([Antique Identifier](https://antique-identifier.app/blog/vintage-pyrex-identification-guide)) and ornaments ([iCollect Everything](https://www.icollecteverything.com/ornaments/)). If we do a collector app, it must use on-device models or barcode/catalog lookup and own its data. I didn't find one that clears the bar (§7).
2. **Settlemate/PayMe numbers are unverified**, and the category is already copied. It also sits close to legal claims. I kept the transferable part, the *"money that belongs to you" hook*, and used it in the Card Benefit Claims Kit and PPM Companion.
3. **Party games spread for free but monetize weakly** (ads, one-off unlocks, hit-driven). That's a poor fit for "consumers pay within 90 days". I kept the transferable part, **forced multiplayer**, in tools where inviting others is the job itself (HeirloomDraft: every heir must join; Family Cookbook: every relative contributes).
4. **Search ranking (Escape) is great but slow.** App Store ranking and Google SEO usually take 3–6+ months, which is longer than our 90-day pay window. For the first 90 days, **community channels and built-in invites are faster**. That's why I weighted C2 toward "tight community or built-in invites" over "SEO alone".
5. **Agree strongly with DayZen and C4.** Most survivors are one-off events, so they're priced per project or per event (one-time), not as monthly subscriptions.

### 2.4 Timing note (today is 2026-09-26)

A 2–6 week build means launching around **mid-Oct to early Nov 2026**. The 90-day pay window then runs to about **Jan–Feb 2027**. Ideas whose buying season lands in that window get a real boost:
- **Family Cookbook:** holiday gift season. ✅
- **Private-school admissions:** NYC/SF applications run Sep–Dec. ✅
- **Card claims:** holiday travel delays in Dec–Jan. ✅
- **PPM moves:** peak season is May–Sep. ❌ Off-season, so it probably can't prove payment within 90 days.
- **Estate/heirloom division:** year-round (deaths peak in winter). Neutral to slightly positive.

---

## 3. Scoring rubric

**Hard constraints (pass/fail)**
- H1 B2C: individuals pay with their own card.
- H2 Not saturated or hype-driven, and not in the auto-reject list.
- H3 Not already done well (C6 below).
- H4 Easy execution: no licensed-profession risk, no marketplace cold start, no hardware, no heavy user-content moderation, low cost per user.
- H5 A distribution channel that needs no ad budget.
- H6 Evidence people already pay.

**Scoring criteria (1–5 each; higher = better)**
- **Pay:** strength of existing-spend evidence (H6).
- **C1:** pay trigger in session 1 (a personalized result, a found-money number, a finished artifact).
- **C2:** an ownable channel (tight community, built-in invites, or high-intent keyword).
- **C3:** near-zero marginal cost (no per-use AI/API, no licensed data).
- **C4:** pricing matches usage (one-off → one-time; ongoing → annual).
- **C5:** big enough for $3–10k MRR, small enough that incumbents ignore it.
- **C6 open:** 5 = no real competitor; 1 = a well-reviewed app dominates.
- **Build:** 5 = MVP in about 2 weeks; 1 = more than 6 weeks.
- **Adj:** penalty or bonus for risk or timing (stated per idea).

---

## 4. The 25 candidates (full detail)

Format per idea: pitch · target user · pain + evidence · what they pay or do today · competitors and why they fall short · price · channel · build difficulty (1 = easy, 5 = hard).

### C01 — HeirloomDraft (fair division of a parent's belongings)
- **Pitch:** A calm, fair way for siblings to split Mom and Dad's things. Photo inventory, a blind "what matters most to me" round, then a turn-based draft on a video call. Ends with a signed-off list for the executor.
- **Target user:** Adult children (40–65) settling an estate or helping a parent downsize. Secondary: executors.
- **Pain + evidence:** Jewelry and personal possessions are the #3 cause of estate disputes, and in 30% of disputes family members stop speaking ([LLPH stats](https://www.llphlegal.com/blog/2018/05/10-important-statistics-about-sibling-estate-disputes/)). Elder-law firms recommend structured draft methods ([ElderLawAnswers](https://www.elderlawanswers.com/six-ideas-for-distributing-an-estates-personal-property-in-a-fair-way--15223)). FairSplit's own survey of "thousands of heirs" ([link](https://www.fairsplit.com/survey-insights-from-thousands-of-heirs-dividing-estates/)).
- **Today:** Sticky notes, spreadsheets, round-robin picks over Zoom, estate-sale companies, mediators, FairSplit.
- **Competitors:** **FairSplit** (since 2010; $179.95 / $289.95 per estate plus a free tier; sold through attorneys and senior move managers; web-platform feel) ([home](https://www.fairsplit.com/), [pricing](https://www.fairsplit.com/plans/pricing-estate-division/)). Estimonia (content/appraisal), myend.com (end-of-life content). **Gap:** mobile-first, fast "draft night", a sentimental note per item, cheaper one-time price, sibling-friendly tone.
- **Price:** $49 per estate (up to 6 heirs), $99 for large estates. Free to invite heirs.
- **Channel:** Every heir must be invited (built-in referral). Long-tail SEO ("how to divide parents' belongings", "round robin inheritance items"). Downsizing and caregiver Facebook groups. Later: affiliate links with estate-sale companies and senior move managers.
- **Build:** 2 (inventory + photos + bidding/draft logic + invites + PDF summary).

### C02 — Card Benefit Claims Kit
- **Pitch:** "Your flight was delayed 7 hours. Your card owes you up to $500. Here's the exact packet." Pick card + incident, see coverage, get a document checklist, assemble the packet, track the claim deadline.
- **Target user:** Holders of premium travel/rewards cards (Sapphire, Amex Platinum/Gold, Venture X…) after a trip delay, delayed bag, broken phone, damaged purchase, or failed product (extended warranty).
- **Pain + evidence:** 62% of travelers are wrong about their card's coverage ([PR Newswire](https://www.prnewswire.com/news-releases/new-data-shows-62-of-travelers-are-wrong-about-what-their-travel-credit-card-covers-302854100.html)). Many "how I filed my Chase trip delay claim" guides exist, listing documents and denial reasons ([AwardWallet](https://awardwallet.com/blog/how-to-file-a-flight-delay-claim-with-chase/), [Million Mile Secrets](https://millionmilesecrets.com/guides/how-to-file-chase-trip-delay-insurance-claim/), [10xTravel](https://10xtravel.com/how-to-submit-a-chase-trip-delay-claim-my-experiences/)). Coverage is up to $500 per ticket ([Chase benefits](https://cardbenefits.chase.com/chase-sapphire-preferred/trip-delay-reimbursement)).
- **Today:** Reading 40-page benefit PDFs and blog posts, filing on eClaimsLine or Amex portals, or never claiming at all.
- **Competitors:** **Kudos** (funded, free; "Hidden Perks" reminds you of coverage) ([blog](https://www.joinkudos.com/blog/hidden-perks)). CardPointers and MaxRewards (focused on earning rewards). Free blog guides. **Gap:** the moment *after* something goes wrong: per-card document checklist, packet assembly, claim-window countdown.
- **Price:** $12 per claim, or $29/yr for unlimited.
- **Channel:** Long-tail SEO per card × incident (hundreds of pages). r/CreditCards, r/churning, r/amex, FlyerTalk.
- **Build:** 2 (the work is compiling benefit data for about 40 cards).

### C03 — Family Cookbook
- **Pitch:** Text relatives a link, they snap grandma's recipe card or type their dish, and the app typesets a designer-quality cookbook (keeping the handwritten card as an image). Download a PDF or order prints.
- **Target user:** The family organizer (often 30–65) making a holiday gift, bridal-shower book, reunion book, or memorial collection.
- **Pain + evidence:** Many Etsy editable Canva cookbook templates ([1](https://www.etsy.com/listing/1655650136/canva-cookbook-template-family-recipe), [2](https://www.etsy.com/listing/1693295511/family-cookbook-canva-template-38-page)). Family Cookbook Project has run for years on printing revenue ([FCP](https://www.familycookbookproject.com/)). Mixbook recipe books from $14.99 ([Mixbook](https://www.mixbook.com/recipe-cookbook-photo-books)). Storyworth proves people pay $99 for family keepsake books ([Wikipedia](https://en.wikipedia.org/wiki/Storyworth)).
- **Today:** Canva templates plus chasing relatives by text, Google Docs, FCP, Mixbook, local fundraiser printers ([Morris Press](https://www.morriscookbooks.com/fundraising/family-cookbook.cfm)).
- **Competitors:** **Family Cookbook Project** (established, dated interface, recently added AI recipe conversion). **Mixbook/Shutterfly** (good editors, but no way to collect from relatives). **Reunly** (reunion-focused). **Gap:** phone-first collection from relatives plus auto-layout that looks professionally designed.
- **Price:** $29 for the digital book. Print at cost plus margin ($25–45 per copy through a print-on-demand API).
- **Channel:** Every contributor sees the product (built-in invites). Pinterest and TikTok gift content. SEO ("family cookbook gift", "bridal shower recipe book").
- **Build:** 3 (typesetting quality and print integration are the work).

### C04 — Marriage Evidence Binder ⚠️
- **Pitch:** Drop in photos, chat exports and joint documents. Get a dated, chronological, indexed exhibit PDF for I-130, I-751 or K-1 filings. Processing happens on the device.
- **Target user:** Couples filing marriage-based immigration paperwork themselves.
- **Pain + evidence:** Etsy marriage-evidence templates ([Etsy](https://www.etsy.com/listing/4328945789/marriage-evidence-immigration-template)). Buy Me a Coffee photo templates ([BMC](https://buymeacoffee.com/kseniya/e/333226)). Law-firm evidence checklists ([CitizenPath](https://citizenpath.com/i-751-evidence-list-proof-of-marriage/)). EvidenceGen users report officers praising their organized logs ([EvidenceGen](https://www.evidencegen.com/)).
- **Today:** Canva, manual PDF merging, or lawyers.
- **Competitors:** **EvidenceGen** (focused, positive community reviews), [uscisphotos](https://uscisphotos.netlify.app/) (free), Etsy templates, Boundless (full service). **Gap:** small. Mostly price, polish, and I-751-specific flows.
- **Price:** $49 per filing.
- **Channel:** r/USCIS, r/immigration, r/K1Visa, VisaJourney forums. SEO ("I-751 evidence").
- **Build:** 2.
- **⚠️ Flag:** Close to hard constraint H4 (legal adjacency). It only passes if it is **strictly a formatter**: no advice on what to submit or which form to use. There's also political and policy volatility around US immigration in 2025–26.

### C05 — Pet Move Planner
- **Pitch:** Enter pet, origin, destination and move date. Get a dated step plan (microchip → rabies shots → titer test → wait period → health certificate → USDA endorsement), a vet-visit packet, and reminders.
- **Target user:** Expats, military families moving overseas, people moving to Hawaii, Japan, Australia, the UK or the EU.
- **Pain + evidence:** Plan 7–9 months ahead. Japan requires two rabies shots, a titer test from an approved lab, and a 180-day wait ([Petworks](https://www.petworks.com/articles/dog-move-usa-to-japan-timeline/), [USDA APHIS](https://www.aphis.usda.gov/pet-travel/us-to-another-country-export/pet-travel-us-japan)). Paws Abroad sells a **$147 DIY plan** next to $795–$2,500+ services ([pricing](https://www.pawsabroad.co/services)).
- **Today:** USDA pages, vets, Facebook groups, or $2–10k relocation companies.
- **Competitors:** **Passpaw** free planner (lead generation for its health-certificate service) ([planner](https://passpaw.com/pet-travel-planner)). **Paws Abroad** ($147 DIY, 14+ countries). Relocation-company guides. **Gap:** cheaper than Paws Abroad, broader routes, military overseas and Hawaii flows, vet-ready printouts.
- **Price:** $29–39 per move.
- **Channel:** SEO per route ("dog US to Japan timeline"), r/expats, r/movingtojapan, military-spouse overseas groups.
- **Build:** 3 (a rules database per country plus ongoing upkeep).

### C06 — IEP Parent Binder
- **Pitch:** One place for a child's IEP, evaluations, progress reports and school emails. Track goals and services actually delivered. Get a one-page meeting-prep sheet.
- **Target user:** Parents of the roughly 7.5M US students with IEPs `[K: NCES]`.
- **Pain + evidence:** Etsy parent IEP binders ([1](https://www.etsy.com/listing/4475456303/parent-iep-binder-printable-special), [2](https://www.etsy.com/listing/1579248108/editable-parent-iep-binder-printable-iep)). A binder guide from Understood.org ([link](https://www.understood.org/en/articles/how-to-organize-your-childs-iep-binder)). Kidvokit charges $59–99/yr ([pricing](https://kidvokit.com/pricing/)). Paid special-ed advocates exist.
- **Today:** Paper binders, Google Drive, advocates.
- **Competitors:** **Kidvokit** (new; early-access pilot in Massachusetts; has an AI "rights" assistant). AbleSpace (teacher side). Free printables. **Gap:** a simpler parent tool without the AI legal Q&A.
- **Price:** $59/yr.
- **Channel:** r/specialed, r/Autism_Parenting, special-ed parent (SEPTA) groups, Instagram special-needs parent creators.
- **Build:** 3. Risks: child data privacy, cost of AI document parsing, staying out of legal-rights advice.

### C07 — PPM Companion (military do-it-yourself move)
- **Pitch:** Estimate your PPM payout and taxes. Capture receipts on the road. Check weight tickets (both empty and full, certified scale). Get a 45-day deadline countdown and a packet ready for MilMove upload.
- **Target user:** Service members and spouses doing a PPM (personally procured move).
- **Pain + evidence:** Claims are due within 45 days. Money is lost to a single weight ticket or missing receipts ([Half Price Movers](https://www.halfpricemovers.com/blog/common-ppm-mistakes-cost-service-members-reimbursement), [Military Wallet](https://themilitarywallet.com/pcs-reimbursement-guide/)). DoD's HomeSafe moving contract was terminated in 2025 and PPM pay rose temporarily to 130%, then went back to 100% ([WeVett](https://wevett.com/2025/blog/military/pcs/ppm-reimbursement-increased-to-130-for-summer-2025-pcs-season/), [moving-hub](https://moving-hub.net/ppm-military-move-guide-2026-earn-more-stress-less/)).
- **Today:** Free calculators ([pcscalculator.net](https://www.pcscalculator.net/), [militarytoolkit](https://www.militarytoolkit.com/ppm-calculator)), MilMove's official upload ([USMC fact sheet](https://www.iandl.marines.mil/Portals/85/Docs/LPD/Fact%20Sheet%20PPM%20Using%20MilMove.mil%20GHC%20JAN%202025.pdf)), envelopes.
- **Competitors:** No dedicated tracker found. MilMove covers submission and calculators are free. **Gap:** preparation and error-proofing before submission.
- **Price:** $19 per move.
- **Channel:** Military-spouse Facebook groups (large), r/army, r/navy, r/AirForce, r/USMC, PCS-season SEO.
- **Build:** 1–2. Risks: weak evidence anyone pays; peak season is May–Sep (outside our 90-day window).

### C08 — DIY Recruit (college athletic recruiting)
- **Pitch:** A recruiting tracker for families: target-school list, coach contact log, email templates, camp calendar, follow-up reminders, and a timeline by sport and graduation year.
- **Target user:** High-school athletes (and their parents) who want a college roster spot without paying NCSA.
- **Pain + evidence:** NCSA packages run $2,000–6,000+, with complaints about value ([NextCommit](https://www.nextcommit.ai/blog/ncsa-cost)). Etsy recruiting spreadsheets ([listing](https://www.etsy.com/listing/1405716628/the-best-college-recruiting-spreadsheet)). DIY guides tell families to keep a spreadsheet tab per school ([CaptainU](https://stacksports.captainu.com/how-to-organize-your-college-recruiting-process/)).
- **Today:** NCSA, spreadsheets, club coaches, showcases.
- **Competitors:** **NextCommit** (free AI tools), **FieldLevel** (free; coaches use it, so it has network effects) `[K]`, **SportsRecruits** (sold to clubs) `[K]`, NCSA free tier. **Gap:** a simple, private family tracker. Thin.
- **Price:** $9/mo or $79/yr (recruiting lasts 1–3 years, so a subscription fits).
- **Channel:** Club-sport parent Facebook groups by sport, TikTok recruiting creators, SEO ("how to email college coaches").
- **Build:** 3 (coach contact data needs upkeep).

### C09 — Custom-Home Build Tracker
- **Pitch:** For homeowners building a custom home or barndominium: allowances vs. selections, change orders, the payment (draw) schedule, and a "how far over budget are we" dashboard.
- **Target user:** Owner-builders and custom-build clients.
- **Pain + evidence:** Homeowner build-budget templates sell on Gumroad ([example](https://pikachuux.gumroad.com/l/wpojp)). Roundups list 12+ templates ([RBA](https://www.rbahomeplans.com/post/12-best-home-construction-budget-template-options-for-2025)).
- **Today:** Spreadsheets, or the builder's client portal if the builder uses one.
- **Competitors:** **BuildLedger** (free iOS app for homeowners) ([site](https://buildledger.app/)). Builder software (B2B). **Gap:** web + mobile, owner-builder mode with subcontractor bids.
- **Price:** $79 per build.
- **Channel:** r/Homebuilding, barndominium Facebook groups, YouTube build vloggers.
- **Build:** 2.

### C10 — Private-School Admissions Organizer
- **Pitch:** For NYC/SF/LA/Boston K–12 applications: school list, tour and interview calendar, essay drafts per school, test dates, deadline countdowns, and a decision matrix.
- **Target user:** Affluent parents applying to 6–12 private schools.
- **Pain + evidence:** Consultants charge $12,000/child, and an "application tracking spreadsheet" is part of the package ([School Search NYC](https://schoolsearchnyc.com/services/individual-consultations/)). A consultant membership hub is sold to mostly-DIY parents ([BK Admissions](https://www.bkadmissions.com/)).
- **Competitors:** **Ivy Row** (AI platform, NYC only) ([site](https://ivyrownyc.com/)). Consultant hubs. **Gap:** other cities, a lower price.
- **Price:** $149 per season.
- **Channel:** City parent forums, preschool parent groups, SEO per school.
- **Build:** 2. Risks: small total market and gated social networks.

### C11 — Daycare Waitlist Tracker
- **Pitch:** Track 5–15 daycare waitlists, fees, tours and follow-ups.
- **Evidence:** Parents juggle many waitlists and fees. **WaitNest** already does this (free tier up to 5 providers) ([App Store](https://apps.apple.com/ca/app/waitnest-daycare-waitlist-app/id6761996670)).
- **Price/channel/build:** $19 one-time · local parent groups · 1.

### C12 — Maker Recipe and Batch Costing (soap/candle/cosmetics)
- **Pitch:** Recipe costing, batch logs and pricing for small makers.
- **Evidence:** Craftybase at $24–49/mo is called overpriced ([MicroGaps](https://www.microgaps.com/blog/craftybase-alternative-etsy-sellers-cogs-tracking)). Forum users build their own Google Sheets ([Soapmaking Forum](https://www.soapmakingforum.com/threads/google-sheet-alternative-to-craftybase-or-soapmaker-pro.93510/)).
- **Competitors:** Craftybase, **Ardent Seller (free, every feature)**, Inventora.
- **Price/channel/build:** $6/mo · r/candlemaking, r/soapmaking, Facebook groups · 2.

### C13 — HSA Shoebox
- **Pitch:** Log medical receipts and see your "tax-free reimbursement bank".
- **Evidence:** Bogleheads threads ([1](https://www.bogleheads.org/forum/viewtopic.php?t=144165), [2](https://www.bogleheads.org/forum/viewtopic.php?t=462462)) and a White Coat Investor guide ([link](https://www.whitecoatinvestor.com/the-best-way-to-track-your-hsa-receipts/)).
- **Competitors:** Shoebox ($120/yr), HSA Store app, Reimbursable, HSA Trackr, HSA Monster, and more.
- **Price/channel/build:** $29/yr · Bogleheads, r/personalfinance · 2.

### C14 — Premium Card Credits Tracker
- **Pitch:** Never miss Amex Platinum/Gold monthly and quarterly credits.
- **Evidence:** Uber Cash and quarterly credits are commonly missed ([CardStack](https://cardstack.money/articles/credit-card-reviews/amex-platinum-credits-list-2026), [Upgraded Points](https://upgradedpoints.com/credit-cards/reviews/american-express-platinum-card/how-to-activate-use-benefits/)).
- **Competitors:** CardStack, **Kudos** (funded; automated credit tracking), CardPointers `[K]`.
- **Price/channel/build:** $19/yr · r/amex · 2.

### C15 — Costco Price-Adjustment Watcher
- **Pitch:** Scan your receipt and get told when you can claim a price drop within 30 days.
- **Competitors:** CostPal, CostLow, CostRefund. Also depends on Costco price data.
- **Price/channel/build:** $3/mo · r/Costco · 3.

### C16 — Disaster Contents-Claim Builder
- **Pitch:** Rebuild a room-by-room contents inventory with prices after a fire.
- **Evidence:** United Policyholders sample spreadsheets ([UP](https://uphelp.org/claim-guidance-publications/household-inventory-sample-spreadsheet/)). Paid total-loss inventory services exist ([Precision](https://www.precisionenv.com/services/total-loss-inventory)).
- **Competitors:** Bevel (free), ClaimSight, Contents360, CostCam, HomeZada AI. Also, some states and insurers now pay part or all of contents limits after total-loss disasters *without* an itemized inventory ([UP](https://uphelp.org/ask-an-expert/question/is-there-a-standard-payout-of-personal-property-loss-due-to-fire/)).
- **Price/channel/build:** $99/claim · survivor groups · 3.

### C17 — Campsite Cancellation Alerts
- **Pitch:** Get a text when a sold-out campsite opens.
- **Competitors:** Campnab ($10–90/mo), Campflare, several free alternatives, Recreation.gov's own alerts.
- **Price/channel/build:** $10/mo · r/camping · 3.

### C18 — Western Big-Game Draw and Points Planner
- **Pitch:** All ~75 western tag-application deadlines plus preference-point strategy.
- **Competitors:** **goHUNT** (dominant, about $120/yr for maps and points; [Rokslide](https://rokslide.com/forums/threads/gohunt-insider-worth-it.296645/)), Huntin' Fool, Drawn West, HuntStand.
- **Price/channel/build:** $39/yr · Rokslide, HuntTalk · 3.

### C19 — Horse Care Records
- **Pitch:** Farrier, vet, deworming and Coggins tracking per horse.
- **Competitors:** 5+ apps (§2.1).
- **Price/channel/build:** $5/mo · barn and equestrian Facebook groups · 2.

### C20 — Beekeeping Inspection Log
- **Pitch:** Hive inspections, treatments and harvest records.
- **Competitors:** HiveTracks plus 5 more (§2.1).
- **Price/channel/build:** $24/yr · r/Beekeeping · 2.

### C21 — Reptile Husbandry Log
- **Pitch:** Feeding, shed and weight logs per animal.
- **Competitors:** Husbandry.Pro plus 4 more (§2.1).
- **Price/channel/build:** $5 one-time · r/ballpython, MorphMarket · 1.

### C22 — Nomad Tax-Residency Day Counter
- **Pitch:** 183-day rule, Schengen 90/180, and US substantial-presence tracking.
- **Competitors:** 8+ apps (§2.1).
- **Price/channel/build:** $29/yr · r/digitalnomad · 2.

### C23 — Trail-Cam Photo Sorter (on-device AI)
- **Pitch:** Sort SD-card photos into bucks, does and blanks, and build a buck "hit list".
- **Competitors:** onX, DeerLab, BuckSort, BuckOracle, Trakkdown (local, private).
- **Price/channel/build:** $39 one-time · hunting forums · 4.

### C24 — South Asian Multi-Event Wedding RSVP
- **Pitch:** Separate guest list and RSVP per event (mehndi, sangeet, wedding, reception), shared over WhatsApp.
- **Competitors:** Joy, Invyt, The Curated Knot (free), Wedd.ai, itsmy.wedding.
- **Price/channel/build:** $79 one-time · r/ABCDesis, TikTok · 2.

### C25 — Emergency / "In Case of Death" Binder App
- **Pitch:** A guided, shareable version of the viral Etsy "death binder".
- **Evidence:** Big Etsy demand; one binder reports 5,000+ sold ([Etsy](https://www.etsy.com/market/death_binder), [Savvy Sparrow](https://thesavvysparrow.com/emergency-binder/)).
- **Competitors:** incasebinder.com, Trusted Directive, Life Binder (local-first), plus funded vaults (Trustworthy, GoodTrust, Everplans `[K]`). Buyers visibly prefer paper or PDF.
- **Price/channel/build:** $29 one-time · TikTok, Pinterest · 2.

---

## 5. Kill list (one line each)

| # | Idea | Killed because |
|---|---|---|
| C11 | Daycare waitlist | People pay for daycare spots, not for tracking them; WaitNest already exists with a free tier; tiny price room. |
| C12 | Maker costing | H3: Craftybase is established and Ardent Seller gives every feature away free. |
| C13 | HSA shoebox | H3: 7+ apps, including a brand with distribution (HSA Store); nothing left to differentiate on. |
| C14 | Card credits tracker | H3: Kudos (funded) automates credit tracking, CardPointers and CardStack also exist. |
| C15 | Costco price adjustments | H3: 3 look-alike apps; C3: depends on Costco's price data. |
| C16 | Fire contents claim | H3: Bevel is free plus 3 AI competitors; some insurers now waive inventories on total losses. |
| C17 | Campsite alerts | H3: Campnab/Campflare dominate, free options plus Recreation.gov's own alerts. |
| C18 | Hunting draw planner | H3/C6: goHUNT dominates and is well regarded; its data depth is expensive to match. |
| C19 | Horse records | H2: 5+ apps, some free. |
| C20 | Beekeeping log | H2: HiveTracks plus 5 new apps. |
| C21 | Reptile log | H2: Husbandry.Pro (linked to the MorphMarket marketplace) plus 4 apps. |
| C22 | Nomad day counter | H2: 8+ look-alike apps. |
| C23 | Trail-cam sorter | H2: onX and DeerLab already own this user; 3 AI sorters; build is 4/5. |
| C24 | Desi wedding RSVP | H3: Joy handles multi-event weddings, and several free tools target this exact group. |
| C25 | Death binder app | H3: funded vaults exist, and the Etsy evidence shows buyers want paper/PDF, not an app. |

---

## 6. Top 10 survivors (ranked)

### 6.1 Scores

| Rank | Idea | Pay | C1 | C2 | C3 | C4 | C5 | C6 open | Build | Adj | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | HeirloomDraft (C01) | 4 | 4 | 4 | 5 | 5 | 3 | 3 | 4 | 0 | **32** |
| 2 | Family Cookbook (C03) | 4 | 4 | 4 | 4 | 5 | 4 | 3 | 3 | 0 (timing ✅) | **31** |
| 3 | Card Benefit Claims Kit (C02) | 3 | 5 | 4 | 5 | 4 | 4 | 2 | 4 | −1 (free guides compete) | **30** |
| 4 | Marriage Evidence Binder (C04) ⚠️ | 4 | 5 | 4 | 5 | 5 | 3 | 2 | 4 | −3 (H4 borderline, policy volatility) | **29** |
| 5 | Pet Move Planner (C05) | 4 | 5 | 4 | 5 | 5 | 2 | 2 | 3 | −1 (liability if rules are wrong) | **29** |
| 6 | DIY Recruit (C08) | 5 | 3 | 4 | 4 | 4 | 4 | 2 | 3 | 0 | **29** |
| 7 | IEP Parent Binder (C06) | 4 | 4 | 4 | 3 | 4 | 4 | 3 | 3 | −1 (child-data privacy) | **28** |
| 8 | PPM Companion (C07) | 2 | 4 | 4 | 5 | 5 | 3 | 3 | 5 | −3 (off-season for 90-day window; MilMove overlap) | **28** |
| 9 | Private-School Organizer (C10) | 5 | 3 | 2 | 5 | 5 | 1 | 3 | 4 | 0 (timing ✅ but tiny market) | **28** |
| 10 | Custom-Home Build Tracker (C09) | 3 | 2 | 3 | 5 | 4 | 2 | 3 | 4 | 0 | **26** |

Ties at 29 and 28 are broken by market size and how directly the pay signal applies (reasons below).

### 6.2 Why each one ranks where it does

1. **HeirloomDraft.** The strongest match to your criteria. It's a one-off, emotional, high-stakes job with a proven $180–290 incumbent. The **invite loop is built in** (each heir must join). There are no AI costs. The C1 moment is clear: siblings are invited and see the board, and the family pays to run the draft. FairSplit is the only serious player and feels like a platform sold through attorneys. A warm, mobile-first "draft night" is a real opening. Risk: grief-adjacent marketing needs care, and SEO takes time, so the first 90 days rely on communities and heir invites.
2. **Family Cookbook.** The most joyful market, and **perfect launch timing (holiday gifts)**. Contributors are invited by design. Proven spend (Etsy templates, FCP printing, Storyworth). Risks: print quality and support, Q4 seasonality, and FCP has an established base. The moat is design quality plus smooth collection from relatives.
3. **Card Benefit Claims Kit.** The best "found money" hook (C1 = 5) with zero marginal cost. Pay is less proven: people may just read the free TPG or AwardWallet guide, and Kudos is funded. Worth a cheap landing-page test for one card and one incident (Chase trip delay) before committing.
4. **Marriage Evidence Binder ⚠️.** Scores well on pure mechanics (clear artifact, one-time price, client-side processing, strong communities). But it needs **your ruling on H4**, and EvidenceGen is already well liked. If you rule "legal-adjacent = out", it drops off.
5. **Pet Move Planner.** Excellent C1 (a personalized dated plan appears instantly). There's proof of a $147 DIY price point. But Passpaw's free planner and the upkeep of a rules database weigh on it. The market is niche, though it could reach $3–5k MRR across routes plus military overseas moves.
6. **DIY Recruit.** Strongest raw pay signal (NCSA $2–6k), and a subscription genuinely fits. But FieldLevel's network effect and NextCommit's free tools crowd it. It would win on focus, not features.
7. **IEP Parent Binder.** Big, underserved parent side (about 7.5M kids), strong emotion, one early competitor. The product must stay a *binder* (not an AI advocate), which caps the value, and child data raises privacy stakes.
8. **PPM Companion.** The most open competitive field (no dedicated app) and the easiest build. But pay evidence is weak (free calculators feel "good enough"), and **peak season falls outside our 90-day window**. Better as a later bet (launch around March for the May–Sep season) or as a free lead magnet.
9. **Private-School Organizer.** Wealthy buyers and good timing (Sep–Dec season), but a **tiny total market** and gated parent networks. Ivy Row already owns NYC.
10. **Custom-Home Build Tracker.** Real stakes, but the weakest instant-value moment (C1) and a free competitor. Included as a wildcard. No other idea earned the 10th slot more clearly.

### 6.3 Common patterns among the survivors
- **7 of 10 are one-off events priced per event** (C4 alignment).
- **2 have invites built in** (HeirloomDraft, Cookbook), which is the free distribution from the orchestrator's multiplayer lesson.
- **None needs cloud AI in its core loop.** OCR or parsing is optional (Cookbook, IEP), and can run on the device or be capped per user.
- **Most are web-first** (links for invites, PDF output, SEO). iOS vs. web is a Round-4 decision. Web plus Stripe ships faster and avoids the 30% App Store cut. iOS gives App Store search.

---

## 7. Also considered and killed early (not in the 25)

- **Class-action settlement finder** (Settlemate/PayMe clone): already done and copied, legal-adjacent, revenue numbers unverified `[O]`.
- **Collector scanners/trackers:** Pyrex ([PyrexVault](https://pyrexvault.com/), free), Disney pins, Hot Wheels ([Diecast ID](https://apps.apple.com/app/id6747059081)), Hallmark ornaments ([iCollect Everything](https://www.icollecteverything.com/ornaments/); Hallmark's own wish list), star notes (6+ free checkers). Each is either farmed, or has copyrighted catalog images and price-data dependency (C3).
- **Summer-camp planner:** a free incumbent with 19,500 camps catalogued.
- **Nurse multi-state CE tracker:** CE Broker (mandated in some states) plus free Nursa and License Tracker.
- **DIY lawn program:** Yard Mastery (free, 100k+ users, run by a YouTuber) ([App Store](https://apps.apple.com/us/app/yard-mastery-lawn-care-app/id1502311686)).
- **Homeschool hours/transcripts:** Homeschool Planet, Homeschool Tracker, and free HomeTrail/Nautilus generators.
- **Dog-sport titles:** AgilityNerd and 2 others; tiny market.
- **Metal-detecting research:** Aureal, WhereToDetect, Rodek.
- **Rabbit/goat breeder pedigrees:** Everbreed (modern) plus legacy Evans/KinTraks.
- **Knitwear pattern grading:** Knitflow plus the free Pattern Grader.
- **Choir learning tracks:** ChoirMate, SightSinger, PlayScore, Soundslice.
- **Model-railroad layout planner:** AnyRail plus the web tools TrackPlanner.app and TRAX (free).
- **Embroidery / cross-stitch organizers:** see §2.1.
- **Fragrance collection:** Parfumo (large database plus wear calendar).
- **Genealogy:** RootsMagic, Reunion, FamilySearch (free), Gramps (free).
- **Adoption paperwork:** The Adoption App ($4.99) plus agency portals; tiny market.
- **Hotel price-drop rebooking:** several free trackers.
- **Wedding vendor-payment tracker:** Zola and The Knot are free and well made `[K]`.
- **Home-maintenance tracker:** 8+ apps (HomeOps, Homer, Upkeepy, HomeZada, House Manager…).
- **Caregiver coordination:** CircleCare, Caily, FamLove, CuroNow, eLivelihood; families rarely pay.
- **Immigration case trackers:** many free trackers ([MyCasesHub](https://mycaseshub.com/) etc.).

---

## 8. Open questions for Round 2 (stress test)

For each top-5 idea I'd like to test cheaply before picking the final 3:
1. **Competitor depth.** Pull App Store and Trustpilot review counts and read complaint text for FairSplit, Family Cookbook Project, Kudos, EvidenceGen, Passpaw and Paws Abroad. Look for "too expensive", "confusing", "outdated".
2. **Keyword demand.** Rough monthly search volume for the 5–10 money keywords per idea (e.g., "divide parents belongings", "family cookbook gift", "chase trip delay claim").
3. **Community reach.** Count the actual size and rules of 3–5 target communities per idea (self-promo rules matter).
4. **One-day smoke tests.** A landing page with price shown and a "pre-order / join waitlist" button per idea. Posting in 2–3 communities, measure click-to-email rates.
5. **Your rulings needed:**
   - Is **C04 (Marriage Evidence Binder)** inside or outside H4?
   - **Web-first vs. iOS-first**: should this constrain the finals?
   - Is a **seasonal launch** (Cookbook's holiday window) a plus you want to chase, or too risky as a first product?

---

## Sources (this round)

All links are cited inline above. Main clusters:
- Etsy/Gumroad demand: Etsy cookbook, IEP, death-binder, recruiting, marriage-evidence and wedding listings; [Sellfy on spreadsheet sales](https://sellfy.com/blog/sell-excel-google-spreadsheets/).
- Competitor pages: FairSplit, Family Cookbook Project, Mixbook, Kudos, EvidenceGen, Passpaw, Paws Abroad, Kidvokit, NextCommit, Ivy Row, BuildLedger, Craftybase alternatives, Campnab, HorseBook, HiveTracks, Husbandry.Pro, HSA roundups, CostPal, Bevel, WaitNest.
- Pain evidence: LLPH sibling-dispute stats, ElderLawAnswers, WalletHub and PR Newswire card-benefit surveys, Chase/AwardWallet claim guides, USDA APHIS pet-travel pages, PPM guides (Military Wallet, Half Price Movers, WeVett), School Search NYC pricing, NCSA cost analysis.
- Indie patterns: Indie Hackers (PreQuilt), Seedtime (Tracxn/The Packer), buildmvpfast (solo portfolio), plus orchestrator Reddit/YouTube input (unverified).
