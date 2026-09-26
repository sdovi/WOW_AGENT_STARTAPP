# 06 — Execution Plan #1: Card Benefit Claims & Appeals

- **Working name:** *ClaimCard* (placeholder; check trademarks before buying a domain)
- **Score:** 73/130 (Round 2)
- **Model:** $19 per claim (includes 1 appeal) + $49/yr Claims Pass
- **Start:** week of **Mon Sep 28, 2026**
- **Target launch:** **Mon Dec 7, 2026**, before holiday-travel disruptions. A free checker and SEO pages go live earlier (week of Oct 12).
- **Build order in the portfolio:** 3rd to launch. The benefits database is built a little each day from week 0 (see `06-summary.md`).

---

## 1. Pitch, user, wedge

- **One line:** "Your card's insurance said no, or you don't know where to start? Get the exact claim packet and appeal for your card, benefit and denial reason."
- **Target user:** holders of premium travel and rewards cards (Chase Sapphire Preferred/Reserve, Amex Platinum/Gold, Capital One Venture X, Citi Strata Premier, Bilt, the major airline co-brands) after:
  - a trip delay or cancellation, or a delayed or lost bag
  - a broken or stolen purchase (purchase protection)
  - a failed product (extended warranty)
  - later: rental-car damage (CDW) or a broken phone
- **Primary persona:** a non-hobbyist cardholder (r/CreditCards type, not r/churning power users) with $150–$2,000 at stake, often holding a denial email.
- **Wedge vs. the nearest competitors:**
  - Kudos and CardPointers tell you *whether* you're covered.
  - Blogs tell you *how claims work in general*.
  - **We produce the packet and the appeal for *your* card version and *your* denial reason, using real claim outcomes.**
  - Pine AI (a funded agent that makes calls for you) is generic and phone-first; we are benefit-terms-first and self-serve.

---

## 2. Pre-build validation (week 0: Sep 28–Oct 4)

**Assets (about 1 day with Claude Code):**
- A one-page site ("Card insurance said no? Get your claim packet in 10 minutes") with 3 sections: how it works, supported cards, FAQ ("not a lawyer, not an insurer").
- A **free "Am I covered?" mini-checker** for 3 cards × 2 benefits (Sapphire Reserve trip delay, Amex Platinum trip delay, Sapphire Preferred baggage delay), with rules hard-coded from the official benefit pages.
- A **fake-door pre-order**: "Reserve your claim packet — $12 early price (charged at launch)", using a Stripe Payment Link in *authorize-later* mode or a refundable deposit. Be transparent: "launching Dec 7".
- A **"Share your claim outcome" form** (Tally): card, benefit, what was denied, what worked. This seeds the outcome database.

**Channels (no ads):**
1. **Reddit, value first, no links in week 0:** answer 15 recent claim threads in r/CreditCards, r/ChaseSapphire, r/amex and r/VentureX with specific, correct document lists. Put the site link only on your profile.
2. **r/churning:** one comment in the weekly "Discussion/Question" thread: "I'm collecting trip-delay and extended-warranty claim data points; form here; results shared back publicly." Per their rules: blog links only as text posts, no link shorteners, and accounts under 7 days old or with negative karma are auto-removed ([rules](https://libredd.it/r/churning/wiki/rules)).
3. **FlyerTalk** (Chase and Amex claim threads): participate only; no promotion.
4. **2 cold emails to points bloggers** (Frequent Miler, Doctor of Credit tipline) offering the aggregated outcome data as a story.

**Copy angle to test (A/B headline on the landing page):**
- A: "Your card owes you up to $500 for that delay. Here's the exact packet."
- B: "Claim denied? Most card-benefit denials can be appealed. Here's how, for your card."

**Pass/kill thresholds (end of week 1):**

| Metric | Pass | Kill |
|---|---|---|
| Landing visitors | ≥ 300 | — |
| Free-checker use rate | ≥ 25% of visitors | < 10% |
| Email capture | ≥ 8% | < 3% |
| Paid reservations ($12) | ≥ 6 | 0–1 |
| Outcome-form submissions | ≥ 20 | < 5 |

If it's in between, keep going but change the headline or angle to appeals-only.

---

## 3. MVP scope

**Must-have (v1):**
1. **Coverage engine** for ~15 card versions × 4 benefit types (trip delay, baggage delay, purchase protection, extended warranty). Each rule is date-stamped, with a link to the source PDF.
2. **Free "Am I covered?" check** (card + incident + dates + expenses) → estimated reimbursable amount, deadline, missing documents.
3. **Claim Packet builder ($19):**
   - A per-administrator checklist (eClaimsLine/Allianz, Card Benefit Services/Asurion, Amex).
   - Drag-and-drop upload that merges everything in the browser into one labeled PDF.
   - A pre-filled cover letter and a timeline page.
   - A "what the adjuster will ask next" list.
4. **Appeal builder** (included in the $19): pick the denial reason → a clause-cited rebuttal letter + the evidence to add.
5. **Deadline reminders** (email): claim window, document window, appeal window.
6. **Outcome capture:** 30 and 60 days later, "Did you get paid? How much? What worked?" feeds the playbook.
7. **Claims Pass ($49/yr):** unlimited claims across all cards + "benefit expirations" digest (a retention feature absorbed from the household-deadlines idea).

**Explicitly NOT in v1:**
- No success fee.
- No contacting insurers on the user's behalf.
- No Gmail or bank connections.
- No native app.
- No CDW, cell-phone or return protection (v1.5).
- No pet insurance (v2).
- No AI chat.
- No storing card numbers.

**First-session pay-trigger screen (wireframe):**
```
Chase Sapphire Reserve · Trip Delay · UA 1432, 7h 40m delay, Dec 22
✅ Likely covered (6h+ delay, paid with card). Guide version: Jun 23 2025
Estimated reimbursable: $612 of $680 entered (up to $500/ticket × 2 travelers)
⏰ Claim window: notify within 60 days → by Feb 20 · docs within 100 days
Missing for approval: ① itemized hotel folio ② airline delay confirmation ③ statement line
[ Build my claim packet + appeal if denied — $19 ]   [ Claims Pass $49/yr ]
Source: benefit guide §3.2 (link) · Not insurance or legal advice.
```
*(Illustrative numbers.)*

**Pricing + Stripe setup:**
- Stripe Checkout: one-time price `claim_packet_19`, subscription price `claims_pass_49_yearly`.
- Customer Portal enabled.
- Stripe Tax off at first (digital service; check your state's nexus rules).
- Receipts via Stripe.
- Promo code `EARLY12` for week-0 reservers.

---

## 4. Tech stack and architecture

- **Web-first PWA:** Next.js (App Router, TypeScript) on **Vercel Pro** ($20/mo, shared across the portfolio; the Hobby tier is non-commercial).
- **Database and auth:** **Supabase** (Postgres + Auth magic links + Storage), free tier during build, **Pro $25/mo** at launch (shared org).
- **Email:** **Resend** (free up to 3k/mo) for reminders. Scheduling via Vercel Cron.
- **PDF:** `pdf-lib` in the browser. Uploaded documents stay in the browser by default; only the final packet is optionally stored (user opt-in), encrypted in Supabase Storage with auto-delete after 90 days.
- **Optional AI:** Claude Haiku 4.5 to polish cover and appeal letters (≈ $0.001–0.01 per claim). Every letter is template-first, so AI is optional.
- **Analytics:** PostHog (free tier). **Errors:** Sentry (free).

**Data model (sketch):**
```
card(id, issuer, network, product, version_label, effective_from, effective_to, source_url, source_sha256)
benefit(id, card_id, type, trigger_rule jsonb, limits jsonb, covered_items[], exclusions[],
        notify_days, docs_days, administrator, portal_url, clause_refs jsonb)
doc_requirement(id, benefit_id, doc_type, required, pitfall_note)
denial_reason(id, benefit_type, administrator, code, label, rebuttal_template, evidence_to_add[])
claim(id, user_id, card_id, benefit_type, incident_at, amount_claimed, deadlines jsonb,
      status, denial_reason_id, amount_paid, outcome_reported_at)
outcome(id, claim_id|null, source['user','public_dp'], benefit_type, administrator, denied_for, paid_after, amount, date)
user(id, email, plan, stripe_customer_id)   reminder(id, claim_id, send_at, kind, sent_at)
```

**Upkeep workflow for versioned rules (≈ 2–3 h/week):**
1. A weekly cron downloads each source benefit PDF or page, computes a hash, and opens a GitHub issue on any change.
2. A human reviews the diff, creates a new `card` version row with `effective_from`, and never overwrites old versions (claims use the version in force on the incident date).
3. Monthly: re-read r/CreditCards and FlyerTalk claim threads; add new public data points to `outcome` (anonymized, with no usernames).
4. Quarterly: re-rank denial reasons by frequency and update rebuttal templates.

**Costs:**
- Per user: ≈ $0.00–0.02 (email + optional AI). Stripe takes ~$0.85 per $19.
- Fixed: domain $12/yr + a share of Vercel Pro and Supabase Pro (≈ $15–25/mo attributable).

---

## 5. Week-by-week build plan (Claude Code-sized tasks)

*Weeks 0–2 run as a background track (≈ 45 min/day) while Group Gift Decks is built. The main build is weeks 7–10.*

| Week | Dates | Tasks |
|---|---|---|
| 0 | Sep 28–Oct 4 | Landing page + mini-checker (3 rules) · Tally outcome form · Stripe Payment Link · Reddit answers (15) |
| 1–6 (background) | Oct 5–Nov 15 | **Database:** transcribe 15 card versions × 4 benefits into `benefit` JSON (≈ 1 card/day), each with a source link and hash · collect 100 public data points into `outcome` · **SEO:** publish 10 of the 20 pages (§6) as static MDX with the mini-checker embedded |
| 7 | Nov 16–22 | Next.js app skeleton, Supabase schema + migrations, magic-link auth · coverage-engine function (pure TS, unit-tested against 30 fixtures) |
| 8 | Nov 23–29 | Claim wizard UI (card → incident → expenses) · result screen (pay trigger) · Stripe Checkout + webhooks → `claim.status=paid` |
| 9 | Nov 30–Dec 6 | Packet builder (upload, reorder, client-side PDF merge, cover letter + timeline templates) · appeal builder (denial-reason picker + template) · Resend reminders + Vercel Cron · outcome-capture emails at +30/+60 days |
| 10 | Dec 7–13 | **Launch.** Privacy policy/ToS/disclaimer pages · PostHog funnels · 5 beta users from the week-0 list run real claims · fix list |
| 11–12 | Dec 14–27 | Holiday disruption playbook pages (storm-day posts) · Claims Pass digest · v1.5 backlog (CDW, cell phone) |

---

## 6. Go-to-market (first 90 days after launch)

**Channel by channel:**

| Channel | Size | Rules (verify before posting) | Plan |
|---|---|---|---|
| r/CreditCards | 1.56M `[O]` | Self-promo rules unverified; assume no promotional posts | Answer claim/denial threads with complete checklists; link only when asked or allowed. 3 answers/day in weeks 10–13 |
| r/churning | 674K `[O]` | One front-page promo post per product; otherwise weekly threads; text posts only | Week 12: a **data post** ("What 300 trip-delay/warranty claims taught us: top 5 denial reasons & fixes") as the single allowed front-page post, with the checker link at the end |
| r/ChaseSapphire | 211K `[O]` | Unverified | Help with denial threads (the "scam" thread had 420↑/251 comments, so demand is proven) |
| r/amex, r/VentureX, r/awardtravel, r/delta, r/unitedairlines | — | Unverified | Storm-day posts: "If your flight is delayed today, here's what each card covers" (no link unless allowed) |
| FlyerTalk (Chase UR, Amex MR forums) | — | No commercial posting | Participate; profile link only |
| Points blogs (Frequent Miler, Doctor of Credit, One Mile at a Time) | — | Editorial | Pitch the aggregated outcome data as a story in week 12 |
| TikTok/YouTube Shorts | — | — | 30-second "Your card owes you $500 for this delay" explainers (card-specific), 3/week during December storms |

**20 SEO / programmatic pages** (target keyword → page):
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
18. "common carrier delay letter how to get [united/delta/american/southwest]" (4 pages)
19. "credit card claim appeal letter template [trip delay/warranty]"
20. "[airline] cancelled flight what does my credit card cover"

**Partnerships:** points bloggers (a data story, not paid); later, an affiliate program at 30% of first-year Pass revenue for travel creators.

**Launch sequence:**
- Dec 7: soft launch to the week-0 list (≈ 50–150 emails).
- Dec 10: Reddit answers resume with the checker live.
- Dec 14–Jan 5: storm-day posts plus the TikTok series.
- Jan 10: the r/churning data post.
- Jan 20: blogger pitches.

**Seeding the outcome database:**
- 100 public data points before launch (anonymized).
- Every paid user gets a 30/60-day outcome email.
- The "share your outcome, get a free packet" offer runs until we reach 500 outcomes.

---

## 7. Metrics and kill criteria

**Weekly targets (weeks after the Dec 7 launch):**

| | Week 2 | Week 4 | Week 8 | Week 12 |
|---|---|---|---|---|
| Visitors (cumulative) | 1,500 | 4,000 | 10,000 | 18,000 |
| Free checks | 350 | 1,000 | 2,500 | 4,500 |
| Paid packets (cumulative) | 15 | 45 | 120 | 220 |
| Claims Pass subscribers | 2 | 8 | 20 | 40 |
| Outcomes collected | 120 | 180 | 300 | 500 |

**Unit economics:**
- Average order value ≈ $22 (packets + Pass mix).
- Cost to serve ≈ $1 (Stripe) + ~$0.02.
- Gross margin ≈ 95%.
- Customer acquisition cost ≈ $0 (organic).
- Month-3 revenue at target ≈ $2.5–3.5K/mo.

**Kill/pivot criteria:**
- **Day 30:** < 20 paid **and** < 500 free checks → pivot the message to **appeals-only**, and move effort to SEO pages for denial reasons.
- **Day 60:** < 60 paid → narrow to the top 3 cards + 2 benefits and reconsider a $9 price.
- **Day 90:** < $1,500/mo run-rate **and** < 300 outcomes → stop active development; keep the SEO pages up as a lead magnet.

---

## 8. Legal and compliance checklist

- [ ] **No success fee, ever.** Flat fees only. We never contact or negotiate with insurers or administrators for the user (the **public-adjuster** licensing line). The user files.
- [ ] Clear copy: "Self-help document tool. Not insurance advice, not legal advice, not affiliated with any issuer or insurer." Never claim "AI lawyer" (DoNotPay FTC order, Feb 2025).
- [ ] Show the **source clause + guide version** on every coverage statement; the user confirms before building a packet.
- [ ] One-hour review by an insurance/consumer attorney (≈ $250) before launch: public adjuster, unauthorized practice of law, and "insurance advice" questions in the top 5 states.
- [ ] **Privacy:** documents processed in the browser by default; opt-in storage auto-deleted after 90 days; no full card numbers (auto-redact digits in uploads); a privacy policy that covers sensitive financial documents.
- [ ] Trademarks: issuer and card names used only to describe (nominative fair use); no logos.
- [ ] Outcome data: anonymized; public data points summarized without usernames.
- [ ] Refund policy: 14-day no-questions refund on packets (builds trust; low abuse risk).
- [ ] CAN-SPAM-compliant reminders with one-click unsubscribe.

---

## 9. Top 5 risks and mitigations

| Risk | Mitigation |
|---|---|
| Free guides + ChatGPT are "good enough" | Lead with appeals and denial-specific playbooks backed by outcome data; show "what works for this denial reason (n=37)" |
| Wrong rule or deadline → a user loses money, Reddit backlash | Version + source link on every rule; weekly change detection; conservative wording; refund promise |
| Can't reach users when the problem hits | SEO for denial terms; storm-day posts; outcome-data stories that bloggers link to |
| Kudos, CardPointers or Pine AI add a claims feature | Speed + outcome-data moat; the Pass bundles expiry digests; later, pet insurance and CDW verticals |
| Legal challenge (public adjuster, UPL) | Flat fee, no representation, attorney review, disclaimers, no negotiation |

---

## 10. Budget to first revenue (target < $500)

| Item | Cost |
|---|---|
| Domain | $12 |
| Vercel Pro (2 months, portfolio share ⅓) | ~$15 |
| Supabase Pro (1 month at launch, share ⅓) | ~$10 |
| Resend, PostHog, Sentry | $0 (free tiers) |
| Attorney review (1 h) | $250 |
| Tally, Stripe | $0 (fees per transaction) |
| **Total** | **≈ $290** |

**First 10 actions on Monday (Sep 28):**
1. Pick a working name; check USPTO/TESS and domain availability; buy the domain.
2. Create a Stripe account and a $12 reservation Payment Link.
3. Ask Claude Code to scaffold a Next.js landing page + mini-checker for the 3 hard-coded rules.
4. Download the current benefit guides for Sapphire Reserve, Sapphire Preferred and Amex Platinum; save them with a hash and date.
5. Build the Tally "share your claim outcome" form.
6. Draft the 5 best "document checklist" answers as reusable notes.
7. Post 5 value-only answers in r/CreditCards / r/ChaseSapphire claim threads.
8. Set up PostHog + a UTM convention.
9. Create a GitHub repo with an `/rules` folder and a rules JSON schema (versioned).
10. Book the 1-hour attorney consult for week 6.
