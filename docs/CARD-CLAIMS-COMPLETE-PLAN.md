# Card Benefit Claims & Appeals: The Complete Plan

- **Product name:** **ClaimCard** (a placeholder working name; check the trademark and domain before using it)
- **Status:** approved by the founder as the product to build
- **Plan date:** Sep 26, 2026 · **Start:** Mon Sep 28, 2026 · **Target launch:** Mon Nov 2, 2026
- **Who this is for:** anyone who needs to understand this idea without having read the research. Everything here comes from the research docs (`docs/01`–`06`) and the planning session.
- **Rule for this document:** anything not confirmed from a primary source is marked **(needs checking)**.

---

## 0. Words used in this plan

| Word | Simple meaning |
|---|---|
| **Card benefit** | Free insurance that comes with some credit cards, for example money back if your flight is delayed. |
| **Claim** | Asking the insurance company behind your card to pay you back. |
| **Benefit administrator** | The company that handles claims for the card, for example eClaimsLine (Allianz) for Chase, or Card Benefit Services (Asurion) for many Mastercard cards. |
| **Guide to Benefits** | The official PDF that lists the exact rules for each card benefit. |
| **Denial** | The administrator says no to your claim. |
| **Appeal** | Asking them to look again, with more proof or a better explanation. |
| **Claim packet** | One neat PDF with every document the administrator needs, in the right order, plus a cover letter. |
| **Outcome** | What happened to a claim: paid, denied, or paid after appeal, and why. |
| **DP (data point)** | A real person's report of what happened, often posted on Reddit. |
| **SEO** | Getting found on Google for free by having useful pages. |
| **Merchant of record (MoR)** | A company that sells your product for you legally, handles taxes, and pays you. We use **Paddle**. |
| **MRR** | Monthly recurring revenue: money that comes in every month from subscriptions. |

---

## 1. The problem

### 1.1 What goes wrong

Many credit cards include free travel and purchase insurance, but:
1. **People don't know they have it.** 62% of travelers are wrong about what their card covers ([PR Newswire](https://www.prnewswire.com/news-releases/new-data-shows-62-of-travelers-are-wrong-about-what-their-travel-credit-card-covers-302854100.html)). More than 2 in 5 don't know their card's travel benefits ([WalletHub](https://wallethub.com/blog/credit-card-travel-benefits-survey/51766)).
2. **When they do claim, it's hard.** The rules are buried in long PDFs. Administrators ask for specific documents (itemized receipts, a letter from the airline, card statements). One small mistake means a denial.
3. **Denials are common, and many can be won on appeal.** Warranty-type claims get denied at first 30–50% of the time, and many denials can be reversed ([Pine AI blog](https://www.19pine.ai/blog/dispute-extended-warranty-claims)).
4. **The claim systems are frustrating.** People report eClaimsLine asking for the same documents again and again ([FlyerTalk](https://www.flyertalk.com/forum/chase-ultimate-rewards/1777854-anyone-else-unable-file-claims-eclaimsline.html), [The Points Guy](https://thepointsguy.com/credit-cards/eclaimsline-insurance-issues/)). There are BBB and CFPB complaints about Card Benefit Services ([BBB](https://www.bbb.org/us/va/richmond/profile/aviation-services/card-benefit-services-0603-63412499/complaints)).
5. **People leave money on the table.** Kudos estimates the average person loses about $624 a year in benefits they forget or don't know they have ([MWM/Kudos](https://mwm.ai/apps/kudos-put-your-wallet-to-work/6443548838)).

### 1.2 Real evidence from Reddit (collected directly by the orchestrator)

- r/ChaseSapphire: **"Warning: Trip delay insurance is basically a scam"**: 420 upvotes, 251 comments (Jan 2026).
- r/CreditCards: "Southwest canceled my flight twice for 'operational challenges', **Chase denied my Trip Delay claim**" (Sep 2026).
- r/ChaseSapphire: **"Trip Delay Benefit Claim Saga: keep track and insist when you're right"** (denied twice, then paid after pushing).
- r/ChaseSapphire: **"Sapphire Reserve Trip Delay Claim Success Story: $823 PAID"**: 172 upvotes (May 2026).
- r/VentureX: "Successful Trip Delay claim data point". People post data points because good claim information is hard to find.
- r/CreditCards: "Citi/Mastercard denied my extended-warranty claim…" (Jul 2026).
- r/CreditCards: "Citi purchase protection worthless… evidence doesn't substantiate".
- r/CreditCards: "DP: Extended Warranty claim (Card Benefit Services by Asurion) **denied initially, paid on appeal** ~$161".
- r/CreditCards: "Extended warranty: how do you get a repair estimate?"
- r/CreditCards: "**BAGGAGE DELAY insurance giant fail: only paying 30%, one receipt rejected for no date**".
- r/ChaseSapphire: "Sapphire Reserve Benefits/Credits **Tracker Spreadsheet**": **1,008 upvotes** (May 2026). People build their own tools.

### 1.3 Who has this problem

- People with **premium travel and rewards cards**: Chase Sapphire Preferred/Reserve, Amex Platinum/Gold, Capital One Venture X, Citi Strata Premier, airline co-brand cards, and others.
- These cards cost a lot (Sapphire Reserve's fee went to **$795** in June 2025; Amex Platinum's to **$895** in 2026), so owners want the value they paid for ([point.me](https://www.point.me/insights/chase-sapphire-reserve/), [CNBC](https://www.cnbc.com/select/amex-platinum-card-2025-changes/)).
- **Our main customer:** a normal cardholder (not a points expert) with **$150–$2,000 at stake**, often holding a denial email.
- **Communities:** r/CreditCards (**1.56M** members), r/churning (**674K**), r/ChaseSapphire (**211K**), plus FlyerTalk.

### 1.4 How often it happens

- In 2024 about **22% of US flights arrived late** and about **1.4% were cancelled** ([Experian citing DOT](https://www.experian.com/blogs/ask-experian/what-does-trip-delay-insurance-cover/)). With roughly 7 million flights a year (needs checking), that's on the order of **100,000 cancelled flights a year**, each affecting many passengers.
- Bags get delayed; purchases break or get stolen; products fail after the maker's warranty ends. These happen all year, not just when traveling.
- Busy seasons: **Thanksgiving, Christmas/New Year, winter storms, summer storms.**

---

## 2. The solution (one paragraph)

**ClaimCard** is a web app that helps you claim, and if needed appeal, the insurance benefits that come with your credit card. You tell it your card and what happened (for example, "my flight was delayed 7 hours"). It checks the exact rules for *your* card and *the version* of the rules in force on that date. It tells you if you're likely covered, roughly how much you can get back, your deadlines, and which documents are missing. For a small flat fee it builds a clean claim packet you file yourself. If you're denied, it builds an appeal based on the denial reason and on what has worked for other people. We never contact the insurer for you, and we never take a cut of your payout.

---

## 3. How people will use it (user journey)

1. **Free check ("Am I covered?"):** pick your card → pick what happened (trip delay, bag delay, broken or stolen purchase, product failure) → enter dates, hours, what you paid with, and expenses.
2. **Result screen (the moment they decide to pay):** likely covered or not, estimated money back, deadlines, missing documents, and **the source rule and guide version**.
3. **Pay $19** (or $49/yr for the Claims Pass) through Paddle.
4. **Claim packet builder:** a checklist for your administrator; you drag in your files (receipts, boarding passes, statements). The app merges them **inside your browser** into one labeled PDF with a cover letter and a timeline page.
5. **You file it yourself** on the administrator's website (eClaimsLine, Card Benefit Services, Amex). We show exactly where to click.
6. **Reminders:** email reminders before each deadline (notify-by date, documents-by date, appeal-by date).
7. **If denied → appeal builder (included in the $19):** pick the denial reason → get a rebuttal letter that quotes the rule clause, plus a list of extra proof to add, based on what worked for others.
8. **Outcome follow-up:** at 30 and 60 days we ask "Did you get paid? How much? What worked?" This builds our outcome database, which makes the product better for the next person.
9. **Claims Pass holders** also get a "benefit expirations" digest (claim windows closing, warranty periods ending).

**Example result screen (illustrative numbers):**
```
Chase Sapphire Reserve · Trip Delay · UA 1432, 7h 40m delay, Dec 22
✅ Likely covered (6h+ delay, trip paid with this card). Rules version: Guide dated Jun 23 2025 (needs checking)
Estimated money back: $612 of $680 entered (up to $500 per covered traveler × 2)
⏰ Tell the administrator within 60 days → by Feb 20 · send documents within 100 days (needs checking)
Missing for approval: ① itemized hotel receipt ② airline delay letter ③ card statement line
[ Build my claim packet + appeal if denied — $19 ]   [ Claims Pass $49/yr ]
Source: Guide to Benefits, Trip Delay section (link). Self-help document tool. Not insurance or legal advice.
```

---

## 4. Features

### 4.1 v1 (at launch)

1. **Coverage engine** with versioned rules (see §7.4).
   - **Week 0:** 3 rules (Sapphire Reserve trip delay, Amex Platinum trip delay, Sapphire Preferred baggage delay).
   - **At launch:** ~10 card versions.
   - **By week 8 after launch:** ~15.
   - Up to 4 benefit types per card, where the card offers them: **trip delay, baggage delay, purchase protection, extended warranty**.
2. **Free "Am I covered?" check** with the result screen above.
3. **Claim packet builder ($19):** checklist per administrator, file upload, in-browser PDF merge, cover letter, timeline page, and a "what they will ask next" list.
4. **Appeal builder** (included in the $19): denial-reason picker → rebuttal letter that cites the rule + evidence to add.
5. **Deadline reminders** by email.
6. **Outcome capture** at +30 and +60 days, plus a public "share your claim outcome" form.
7. **Claims Pass ($49/yr):** unlimited claims on all your cards + the benefit-expiry digest.
8. **Legal pages:** Terms, Privacy, Disclaimer, Refund policy (Paddle needs these to approve us).

**Launch card list (target; each needs checking against its Guide to Benefits):** Chase Sapphire Reserve · Chase Sapphire Preferred · Amex Platinum · Amex Gold · Capital One Venture X · Citi Strata Premier · United Explorer/Quest · Delta Reserve/Platinum · a Chase Freedom card (purchase protection/extended warranty) · one popular Mastercard with Card Benefit Services (extended warranty).

### 4.2 Not in v1 (on purpose)

- **No success fee** (percent of payout), ever.
- **No contacting insurers or administrators for the user.**
- No Gmail or bank connections.
- No native mobile app (web app only; it can be installed as a PWA).
- No AI chat.
- No storing full card numbers.
- No rental-car, phone or pet benefits yet.

### 4.3 Later roadmap

- **v1.5 (≈ Dec 2026–Feb 2027):**
  - **Rental-car damage (CDW)** claims: the highest money at stake. The known pain is the rental company's damage report, repair estimate, and "loss of use" fleet log. The claim window can be up to 365 days on Visa terms ([Visa](https://usa.visa.com/content/dam/VCOM/regional/na/us/Solutions/documents/business-auto-rental-collision-damage-waiver-benefit-terms.pdf)).
  - **Cell-phone protection**, **return protection**.
  - **Flight disruptions:** what airlines themselves owe you (airline commitments + US DOT refund rules) next to what your card covers.
- **v2 (≈ spring 2027): pet insurance claims and appeals**, using the same engine (versioned policy terms per insurer, denial reasons such as "pre-existing condition", evidence packet, deadlines, outcomes). r/petinsurancereviews has a strong "share your playbook" culture. There are **7.6M insured pets** in North America ([dvm360/NAPHIA](https://www.dvm360.com/view/us-pet-insurance-enrollment-increased-9-in-2025-but-more-than-95-of-cats-and-dogs-remain-uninsured)). The competitor petclaimappeal.com sells a $19 appeal letter.

---

## 5. Pricing and why

| Product | Price | What you get |
|---|---|---|
| Free check | $0 | Coverage estimate, deadlines, missing-documents list |
| **Claim packet** | **$19 flat** | Packet builder + reminders + **one appeal** for that claim |
| **Claims Pass** | **$49/year** | Unlimited claims on all your cards + benefit-expiry digest |
| Week-0 early credit | $12 | One packet at launch + your claim checklist now; full refund on request |

**Why a flat fee, and never a success fee:**
1. **Legal safety.** Taking a cut of an insurance payout for helping with a claim looks like **"public adjusting"**, which needs a license in most US states, and fees are capped by law ([fee caps by state](https://publicadjusterauthority.com/public-adjuster-contingency-fee-limits-by-state), [United Policyholders](https://uphelp.org/claim-guidance-publications/questions-to-ask-before-hiring-a-public-adjuster/)). A flat-fee self-help tool where **the user files** stays on the safe side.
2. **Simple and honest.** We can't verify what people get paid, and chasing payment afterwards is messy.
3. **Easy yes.** $19 is small compared with $150–$2,000 at stake.

**Why one-time + an annual option:** claims happen now and then (a one-time price fits), but frequent travelers with many cards want an all-year option (the annual Pass fits).

---

## 6. Competitors and why we win

| Competitor | What they do | Why we're different |
|---|---|---|
| **Kudos** (funded, free; Samsung partnership) | "Hidden Perks" reminds you that a card covers something ([Kudos](https://www.joinkudos.com/blog/hidden-perks)). Ratings ~4.2 (Chrome), ~4.8 elsewhere; complaints that benefit data is missing or wrong ([review](https://www.stackeasy.ai/blog/kudos-review)) | They say "you're covered". We help you **get paid**: packet, deadlines, appeal |
| **CardPointers** ($90/yr Plus; ~4.7★ from ~9,500 iOS ratings) | Tracks offers and credits; can filter "which of my cards has trip delay insurance" ([UpgradedPoints](https://upgradedpoints.com/credit-cards/cardpointers-review/)) | Card picking and offers, not claims or appeals |
| **Pine AI** ($25M Series A; 53.7K users; says a 93% win rate) | AI agent that calls companies to dispute bills and chase refunds; pay on success ([Pine AI](https://www.19pine.ai/), [profile](https://aiagentstore.ai/ai-agent/19pine-ai)) | Generic and phone-first. We're built around **card benefit rules and denial reasons**, self-serve, flat fee. **Most likely to copy us.** |
| **RefundMe** | App for **airline** compensation (delays, cancellations, overbooking); files and negotiates **with the airline** for you; no win, no fee ([RefundMe](https://refundme.app/)) | Airline claims, not **card insurance** claims. We never act for the user |
| **Blogs** (The Points Guy, NerdWallet, AwardWallet, UpgradedPoints, 10xTravel) | Free "how to file" guides ([AwardWallet](https://awardwallet.com/blog/how-to-file-a-flight-delay-claim-with-chase/)) | Guides are general. We are **specific to your card version, your denial reason, your deadlines**, and we build the packet |
| **ChatGPT / Claude** | Can write a letter if you paste the rules | Chatbots often mix old and new rules, don't know each administrator's document quirks, don't track deadlines, and have no **outcome data** |

**Why we win (the moat, meaning what's hard to copy):**
1. **Versioned rules:** exact rules per card, per date, with sources. Rules change (for example, Sapphire Reserve changed in June 2025).
2. **Outcome database:** "denied for X → paid after Y". It grows with every user, and nobody else collects it in a structured way.
3. **Long-tail SEO pages** built from that data.
4. **Reputation** in a few Reddit communities.

---

## 7. How it will be built

### 7.1 Tech stack

- **Web app (PWA):** Next.js + TypeScript, hosted on **Vercel** (Pro plan, $20/mo, because the free plan is non-commercial).
- **Database + login + file storage:** **Supabase** (Postgres; magic-link email login; storage only if the user opts in). Free during the build, Pro $25/mo after launch.
- **Payments:** **Paddle** (merchant of record, see §7.5).
- **Email:** **Resend** (free up to 3,000 emails/month) for reminders and follow-ups; scheduled jobs via Vercel Cron.
- **PDFs:** `pdf-lib` **in the user's browser**, so files don't have to leave their computer.
- **Analytics:** PostHog (free tier). **Error tracking:** Sentry (free tier).
- **Optional AI:** Claude Haiku 4.5 only to polish letter wording (≈ $0.001–0.01 per claim). Every letter works from a template without AI.

### 7.2 Architecture (simple view)

```
Browser (Next.js pages)
  ├─ Free checker → coverage engine (rules JSON) → result screen
  ├─ Packet/appeal builder → pdf-lib merges files locally
  └─ Paddle.js checkout overlay
Server (Next.js API routes on Vercel)
  ├─ /api/paddle/webhook  → records payments in Supabase
  ├─ /api/outcomes        → saves "share your outcome" form
  └─ cron jobs            → reminders + 30/60-day follow-ups (Resend)
Supabase (Postgres + Auth + optional Storage)
/rules (versioned JSON files in the code repository, reviewed by a human)
```

### 7.3 Data model (sketch)

```
card(id, issuer, network, product, version_label, effective_from, effective_to,
     source_url, source_sha256, verification_status)
benefit(id, card_id, type, trigger_rule, limits, covered_items[], exclusions[],
        notify_days, docs_days, administrator, portal_url, clause_refs)
doc_requirement(id, benefit_id, doc_type, required, pitfall_note)
denial_reason(id, benefit_type, administrator, code, label, rebuttal_template, evidence_to_add[])
claim(id, user_id, card_id, benefit_type, incident_at, amount_claimed, deadlines,
      status, denial_reason_id, amount_paid, outcome_reported_at)
outcome(id, claim_id|null, source['user','public_dp'], benefit_type, administrator,
        denied_for, paid_after, amount, date)
user(id, email, plan, paddle_customer_id)
reminder(id, claim_id, send_at, kind, sent_at)
```

### 7.4 The versioned rules system

- **Where rules live:** one JSON file per card × benefit × version, for example `rules/chase-sapphire-reserve/trip-delay/2025-06-23.json`.
- **Each file includes:** the source URL, the guide's version or date, the date we checked it, a hash (fingerprint) of the source PDF, **`verification_status`** (`verified` or `needs_verification`), and the clause references.
- **Which version applies:** the one that was in force **on the date of the incident**. Old versions are never overwritten.
- **Unverified rules are labeled in the app**: "Rule pending verification against the official guide. Please double-check." Honesty first.

**How rules stay up to date (≈ 2–3 hours/week):**
1. **Weekly:** an automatic job downloads each source guide or page and compares its fingerprint. If it changed, it opens a task (GitHub issue).
2. **A human reads the change**, creates a new version file with a new `effective_from` date, and marks it verified.
3. **Monthly:** read new Reddit and FlyerTalk claim stories and add them to the outcome database (anonymized, no usernames).
4. **Quarterly:** rank denial reasons by how often they happen and improve the appeal templates.

**Rules status at planning time:**

| Rule | Key terms (from search results) | Status |
|---|---|---|
| Sapphire Reserve trip delay | 6+ hours or overnight; up to **$500 per covered traveler/ticket**; meals, lodging, toiletries, etc.; **notify within 60 days, documents within 100 days** ([Chase](https://www.chase.com/personal/credit-cards/education/basics/chase-trip-delay-insurance-what-to-know), [AwardWallet](https://awardwallet.com/blog/how-to-file-a-flight-delay-claim-with-chase/)) | **(needs checking)** against the current Guide to Benefits |
| Amex Platinum trip delay | 6+ hours; round-trip paid **entirely** with the card; up to **$500 per trip**; **max 2 claims per 12 months**; covered reasons include weather, carrier equipment failure, lost/stolen passport, terrorism; **notify within 60 days** ([Amex benefit page](https://global.americanexpress.com/card-benefits/detail/trip-delay-insurance/platinum), [NerdWallet](https://www.nerdwallet.com/travel/learn/amex-trip-delay-insurance)) | **(needs checking)**, especially the document deadline |
| Sapphire Preferred baggage delay | 6+ hours by a common carrier; **$100/day up to 5 days**; essentials (toiletries, clothing); exclusions include jewelry, electronics, glasses ([NerdWallet](https://www.nerdwallet.com/travel/learn/the-chase-sapphire-preferred-card-travel-insurance-benefits-explained)) | **(needs checking)**: whether the limit is per person, and the notice/document deadlines |

**PDFs the founder must download into `rules/sources/`** (my container can't download them):
1. **Chase Sapphire Reserve** Guide to Benefits, current version after the June 2025 changes (from the Chase account "Card benefits" page, or Chase's benefit PDF host `static.chasecdn.com`) **(needs checking: exact URL)**.
2. **Chase Sapphire Preferred** Guide to Benefits, `BGC11387_v2.pdf` ([link](https://static.chasecdn.com/content/services/structured-document/document.en.pdf/card/benefits-center/product-benefits-guide-pdf/BGC11387_v2.pdf)) **(needs checking: is it the latest)**.
3. **Amex Trip Delay Insurance Guide to Benefits** ($500 / 6 hours): [trip-delay-insurance-500-6hours.pdf](https://www.americanexpress.com/content/dam/amex/us/credit-cards/features-benefits/policies/trip-delay/trip-delay-insurance-500-6hours.pdf).
4. **Amex Platinum trip delay benefit page**, saved as PDF: [link](https://global.americanexpress.com/card-benefits/detail/trip-delay-insurance/platinum).
5. **Chase "Trip Delay Reimbursement: what to know"** page, saved as PDF, for cross-checking: [link](https://www.chase.com/personal/credit-cards/education/basics/chase-trip-delay-insurance-what-to-know).

### 7.5 Payments: Paddle (and why)

- **Why not Stripe directly:** Stripe does not accept businesses based in Turkey, and the founder may live there.
- **Why not Lemon Squeezy:** it still accepts signups and is simpler, but its future is being moved into Stripe's "Managed Payments", which **does not support Türkiye** (checked Aug 2026) ([Lemon Squeezy 2026 update](https://www.lemonsqueezy.com/blog/2026-update), [Dodo Payments](https://dodopayments.com/blogs/stripe-supported-countries-alternatives)).
- **Why Paddle:** an independent merchant of record that sells for us, handles US sales tax and VAT, supports **one-time ($19) and yearly ($49)** payments, and pays out to Turkish bank accounts **in USD/EUR (no TRY payout)** ([ceaksan](https://ceaksan.com/en/saas-payment-infrastructure-turkey)). Fees ≈ **5% + $0.50** per sale ([Dodo Payments](https://dodopayments.com/blogs/paddle-fees-explained)). There's no monthly fee.
- **Things to know:**
  - Paddle checks your website and product before approval (**3–7 business days**). It needs Terms, Privacy and Refund pages.
  - Describe the product as "web software for preparing claim documents" **(needs checking with Paddle's acceptable-use review)**.
  - The week-0 $12 early product must give something right away (the claim checklist) plus a credit for one packet at launch.
  - **Backup:** if Paddle says no, use Lemon Squeezy (checkout links are easy to swap).
- **How it's wired:** the Paddle.js checkout overlay (client token + price IDs) + a webhook (signed with a secret) that records each payment in Supabase. Test in Paddle's sandbox first.

### 7.6 Costs

- **Per user:** about $0.00–0.02 (email + optional AI).
- **Paddle fee:** $19 → about $1.45 → you keep about $17.55. $49 → about $2.95 → you keep about $46.05. There may also be a currency-conversion cost of ~2–3% when paying out in another currency.
- **Fixed per month after launch:** Vercel $20 + Supabase $25 = **~$45/mo**, plus a domain (~$12/year).

---

## 8. Week-by-week build plan

*This product is now the only focus, so the timeline is faster than in the portfolio plan (launch Nov 2 instead of Dec 7). That catches Thanksgiving (Nov 26) and the December holidays.*

| Week | Dates | Concrete tasks (each small enough for one Claude Code session) |
|---|---|---|
| **0: Validate** | Sep 28–Oct 4 | ① Landing page with 2 headline versions (A/B) ② free checker for 3 rules ③ Paddle $12 early-credit checkout (sandbox → live after approval) ④ "share your claim outcome" form saved in Supabase ⑤ Terms / Privacy / Disclaimer / Refund pages ⑥ apply to Paddle ⑦ 15 helpful Reddit answers |
| **1: Rules + engine** | Oct 5–11 | ① Verify the 3 rules from the downloaded PDFs ② add 3 more cards ③ coverage engine as pure functions + 30 unit tests ④ rules loader that checks each JSON file's format |
| **2: Wizard + pay** | Oct 12–18 | ① Magic-link login ② claim wizard (card → incident → expenses) ③ result screen ④ Paddle checkout for $19 and $49 + webhook → mark claim paid ⑤ 5 SEO pages live |
| **3: Packet + appeal** | Oct 19–25 | ① Upload + reorder files ② in-browser PDF merge ③ cover letter + timeline templates ④ appeal builder (denial reasons + templates) ⑤ card-number auto-redaction warning |
| **4: Reminders + beta** | Oct 26–Nov 1 | ① Reminder emails (Resend + cron) ② 30/60-day outcome follow-ups ③ ~10 card versions done ④ 5–10 beta users from the week-0 list run real claims ⑤ fix list ⑥ 10 SEO pages live |
| **🚀 Launch** | **Mon Nov 2** | Email the week-0 list; Reddit answers resume with the checker live |
| **5–8** | Nov 2–29 | Thanksgiving travel content; 20 SEO pages; Claims Pass digest; fixes; aim for 300 outcomes |
| **9–12** | Nov 30–Dec 27 | Holiday and winter-storm push; plan v1.5 (rental car, phone); first r/churning data post when there are ~300 outcomes |

---

## 9. Marketing

### 9.1 Channels and their rules

| Channel | Size | Rules | What we do |
|---|---|---|---|
| **r/CreditCards** | 1.56M | Self-promotion rules **(needs checking)**; assume no promo posts | Answer claim and denial questions with full document lists; share the link only if allowed or asked |
| **r/churning** | 674K | **One front-page promo post per product**; otherwise only in weekly threads; blog links only as text posts; no link shorteners; **accounts under 7 days old or with negative karma are auto-removed** ([rules](https://libredd.it/r/churning/wiki/rules)) | Weekly-thread comments asking for claim data points; **one** big data post later ("What 300 claims taught us") |
| **r/ChaseSapphire** | 211K | **(needs checking)** | Help people in denial threads |
| r/amex, r/VentureX, r/awardtravel, r/delta, r/unitedairlines, r/TravelHacks | — | **(needs checking)** | On storm days: "Delayed today? Here's what each card covers" |
| **FlyerTalk** | — | No commercial posting | Helpful replies only; link in your profile |
| **Points blogs** (Frequent Miler, Doctor of Credit, One Mile at a Time) | — | Editorial | Pitch our anonymized outcome data as a story |
| **TikTok / YouTube Shorts** | — | — | 30-second card-specific explainers ("Your card owes you $500 for this delay"), 3 per week in December |
| **Google (SEO)** | — | — | The 20 pages below, each with the free checker built in |

**Tip:** create or warm up your Reddit account **now** (real, helpful comments) so it's older than 7 days with positive karma before you post.

### 9.2 The 20 SEO pages (target search phrase → page)

1. "chase sapphire reserve trip delay claim documents"
2. "chase trip delay claim denied"
3. "eclaimsline claim stuck / requesting documents again"
4. "how long does eclaimsline take"
5. "amex platinum trip delay insurance claim"
6. "amex baggage delay claim receipts"
7. "venture x trip delay claim"
8. "chase sapphire preferred baggage delay reimbursement"
9. "credit card extended warranty claim how to"
10. "card benefit services extended warranty denied appeal"
11. "extended warranty repair estimate credit card claim"
12. "citi purchase protection claim denied"
13. "purchase protection claim documents"
14. "trip delay insurance weather does it count"
15. "trip delay vs trip interruption credit card"
16. "which credit card covers my flight delay" (interactive)
17. "trip delay itemized receipt rejected"
18. "how to get an airline delay letter [United / Delta / American / Southwest]"
19. "credit card claim appeal letter template [trip delay / warranty]"
20. "[airline] cancelled my flight: what does my credit card cover"

### 9.3 Launch sequence

1. **Week 0:** validation site live; 15 Reddit answers; outcome form open.
2. **Nov 2 launch:** email the week-0 list (goal: 50–150 emails) and offer the early credit holders their packet.
3. **Nov 2–25:** 3 Reddit answers per day; pre-Thanksgiving "know your card coverage" posts.
4. **Nov 26–Jan 5:** storm-day posts + short videos.
5. **~Jan 10:** the r/churning data post (only once there are ~300 outcomes).
6. **~Jan 20:** pitch points blogs with the data story.

### 9.4 How we collect claim outcomes

1. **Before launch:** gather ~100 public data points from Reddit and FlyerTalk, **anonymized** (no usernames; summarized facts only).
2. **The outcome form:** "Share your claim outcome, get a free claim packet" until we reach 500 outcomes.
3. **Every paying user:** automatic emails at +30 and +60 days.
4. **Show the data in the product:** for example, "What works for this denial reason (n = 37)".

### 9.5 How to get the first 100 users

1. 150 helpful Reddit answers over 6 weeks (with the link only where allowed) → week-0 email list.
2. The early credit ($12) for the first buyers.
3. The free-packet-for-your-story offer (people with past claims).
4. Friends and family with premium cards.
5. Storm-day posts when flights are cancelled in large numbers.
6. SEO pages for denial phrases (slower, but they compound).
7. One r/churning data post + one blogger story.

---

## 10. Numbers

### 10.1 Week-0 pass/kill test (Sep 28–Oct 4)

| Measure | Pass | Kill |
|---|---|---|
| Visitors | ≥ 300 | — |
| Use the free checker | ≥ 25% of visitors | < 10% |
| Leave email | ≥ 8% | < 3% |
| Buy the $12 early credit | ≥ 6 | 0–1 |
| Share an outcome story | ≥ 20 | < 5 |

In between → keep going, but switch the message to **appeals only** ("Claim denied? Here's how to fight it").

**Note:** if Paddle isn't approved yet in week 0, count "Reserve" clicks + emails instead of payments.

### 10.2 Targets after launch (Nov 2)

| | Week 2 (Nov 15) | Week 4 (Nov 29) | Week 8 (Dec 27) | Week 12 (Jan 24) |
|---|---|---|---|---|
| Visitors (total so far) | 1,500 | 4,000 | 10,000 | 18,000 |
| Free checks | 350 | 1,000 | 2,500 | 4,500 |
| Paid packets (total) | 15 | 45 | 120 | 220 |
| Claims Pass subscribers | 2 | 8 | 20 | 40 |
| Outcomes collected | 120 | 180 | 300 | 500 |

### 10.3 Unit economics

- **Average order:** ~$22 (packets + Passes).
- **You keep after Paddle:** ~90% ($17.55 of $19; $46.05 of $49).
- **Cost to serve:** ~$0.02 per user.
- **Cost to get a customer:** ~$0 (organic).
- **Revenue at the week-12 target:** ~$6K total so far; **~$2.5–3.5K per month** run-rate.
- **Longer term:** $10K/month needs ~450 packets/month or a larger Pass base. That's a 6–12 month goal driven by SEO and outcome data, not a 90-day one.

### 10.4 Kill / pivot rules (days after launch)

- **Day 30 (Dec 2):** fewer than **20 paid** *and* fewer than **500 free checks** → change the message to appeals only; focus on denial-reason SEO pages.
- **Day 60 (Jan 1):** fewer than **60 paid** → narrow to the top 3 cards and 2 benefits; test a $9 price.
- **Day 90 (Jan 31):** below **$1,500/month** *and* fewer than **300 outcomes** → stop building new features; keep the SEO pages and checker online as a free tool.

---

## 11. Legal guardrails (built into the product)

**Built in from day 1:**
1. **Flat fee only.** No percentage of any payout, anywhere.
2. **We never contact, negotiate with, or file with insurers or administrators for the user.** The user files. (This keeps us away from licensed "public adjuster" work.)
3. **Clear wording everywhere:** "**Self-help document tool. Not insurance advice. Not legal advice.** Not affiliated with any card issuer, network, insurer or benefit administrator."
4. **Every coverage statement shows its source clause + guide version + date checked**, and unverified rules are labeled "pending verification".
5. **Never claim to be an "AI lawyer"** or better than a lawyer (the FTC fined DoNotPay $193K in Feb 2025 for that ([FTC](https://www.ftc.gov/news-events/news/press-releases/2025/02/ftc-finalizes-order-donotpay-prohibits-deceptive-ai-lawyer-claims-imposes-monetary-relief-requires))).
6. **Auto-generated Terms, Privacy, Disclaimer and Refund pages**, filled from settings (business name, contact email, country).
7. **Privacy:** documents are merged in the browser; saving is opt-in and auto-deleted after 90 days; warn users to hide card numbers; no full card numbers stored; outcome data anonymized.
8. **Brand names used only to describe** (no logos).
9. **14-day no-questions refund** on packets.
10. **Email rules:** every reminder has a one-click unsubscribe (CAN-SPAM).

**Optional lawyer check:** deferred until **after the first paying customers**. A ~1 hour review (~$250) by an insurance/consumer attorney of: public-adjuster rules, "unauthorized practice of law", and "insurance advice" rules in the top 5 states.

---

## 12. Top risks and fixes

| Risk | Fix |
|---|---|
| People use free guides + ChatGPT instead of paying | Lead with **appeals** and denial-specific playbooks backed by outcome data ("what worked, n = 37") |
| A wrong rule or deadline costs a user money → anger on Reddit | Versioned rules with sources; weekly change checks; "pending verification" labels; careful wording; refunds |
| Can't reach people at the moment of need | SEO pages for denial phrases; storm-day posts; data stories that blogs link to |
| Kudos, CardPointers or Pine AI add claims features | Move fast; the outcome database is the moat; add verticals (rental car, pet insurance) |
| A legal complaint (public adjuster / practice of law) | Flat fee, user files, no negotiating, clear disclaimers, lawyer check after first customers |
| Paddle rejects the product or delays approval | Apply in week 0; describe it as software; backup: Lemon Squeezy |

---

## 13. Budget

| Item | Cost | When |
|---|---|---|
| Domain | ~$12/year | Week 0 |
| Vercel Pro | $20/month | From launch (free plan is fine for private testing) |
| Supabase | $0 → $25/month | Pro from launch |
| Resend, PostHog, Sentry | $0 | Free tiers |
| Paddle | $0 fixed (5% + $0.50 per sale) | — |
| **Total to first revenue** | **≈ $12–60** | — |
| Optional lawyer check | ~$250 | After the first paying customers |

---

## 14. The founder's step-by-step to-do list (starting today, Sat Sep 26)

**This weekend:**
1. **Choose the name.** Check "ClaimCard" (or your pick) for trademarks (USPTO search) and check the domain. Buy the domain.
2. **Reddit account:** use one that's older than 7 days with positive karma, or start now with helpful comments (r/churning removes new accounts).
3. **Download the 5 PDFs/pages** listed in §7.4 into `rules/sources/` (save web pages as PDF). Note the date you downloaded each.
4. **Create accounts** (all free to start): **GitHub** (you have the repo), **Vercel**, **Supabase**, **Paddle** (sandbox + start the live application), **Resend**, **PostHog**.

**Monday Sep 28 (week 0):**
5. **Paddle:** create a product "Early Claim Credit" priced **$12** (one-time). Later: "Claim Packet" $19 (one-time) and "Claims Pass" $49 (yearly). Copy the **client-side token** and **price IDs**. Create a **webhook** and copy its **secret key**.
6. **Supabase:** create a project; run the database setup (migration) file from the app; copy the **project URL** and **service role key** (keep it secret).
7. **Vercel:** connect the repo, set the app folder as the root directory, and paste all keys as environment variables. Connect your domain.
8. **Resend:** verify your domain (add the DNS records it shows you); copy the **API key**.
9. **PostHog:** copy the project key (optional but useful for the week-0 numbers).
10. **Check the 3 rules** against the PDFs; fix any number that's wrong; change the status to `verified`.
11. **Post 5 helpful Reddit answers** (no links), in r/CreditCards and r/ChaseSapphire claim threads.
12. **Email 2 points bloggers** about the outcome-data idea.

**By Sun Oct 4 (end of week 0):**
13. Reach 15 Reddit answers; ask for claim stories via the outcome form.
14. **Read the week-0 numbers** (§10.1) and decide: go, change the message, or stop.

**Weeks 1–4 (Oct 5–Nov 1):**
15. Download and check the Guide to Benefits for the rest of the ~10 launch cards (≈ 1 card per day).
16. Test the full flow in the Paddle sandbox, then switch to live once Paddle approves.
17. Invite 5–10 early-credit buyers to beta-test with real claims.

**Launch week (Nov 2):**
18. Email the list; resume Reddit answers with the checker live; publish the first 10 SEO pages.

**After first paying customers:**
19. Book the optional 1-hour lawyer check (~$250).
