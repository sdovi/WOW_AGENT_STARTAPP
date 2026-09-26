# 06 — Round 3 Summary: Final 3 + Portfolio Execution

- **Date:** 2026-09-26 · **Start:** Mon **Sep 28, 2026** · **Horizon:** 12 weeks (to Dec 20) + seasonal follow-through to March
- **Plans:**
  - [`06-execution-plan-group-gift-decks.md`](06-execution-plan-group-gift-decks.md)
  - [`06-execution-plan-school-choice.md`](06-execution-plan-school-choice.md) (conditional)
  - [`06-execution-plan-card-claims.md`](06-execution-plan-card-claims.md)

---

## 1. Bourbon re-score (orchestrator review): Finalist #3 replaced

**New facts:**
- **Chasing the Unicorn:** a free national calendar with lottery deadlines, a "Worth the chase" label and a daily brief `[O]`.
- **Bourbon Signal:** release radar + state guides `[O]`.
- **OHLQ's app** now sends Ohio lottery notifications `[O]`.
- **NC Bourbon Insider:** $4.99/mo Pro `[O]`.
- **VABourbon:** inventory snapshots 5×/day, free Discord, **$2/mo Premier** `[O]`.
- **Cask Watch:** open-source VA + NC tracker `[O]`.
- **Also found:** an Apify VA ABC scraper and WhiskyDB (VA/MD/DC) ([Apify](https://apify.com/obsequious_lemonade/virginia-abc-liquor-scraper), [WhiskyDB](https://whiskydb.org/)).
- **Decisive:** since **Aug 6, 2024, Virginia ABC no longer notifies customers of limited-availability sales, removed that inventory from its website, bars staff from sharing it by phone, and sells the bottles at random stores and times** ([VA ABC](https://www.abc.virginia.gov/about/media-room/2024/20240806-virginia-abc-streamlines-allocated-product-sales), [Axios](https://www.axios.com/local/richmond/2024/08/21/virginia-abc-rare-liquor-bourbon-sales-random-system)).

| Framing | T1 | T2×2 | T3 | T4×2 | T5×2 | T6 | T7 | T8 | T9 | T10 | **/130** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| (1) Multi-state lottery desk | 3 | 3 | 7 | 5 | 4 | 6 | 4 | 6 | 6 | 5 | **61** |
| (2) Virginia "state insider" pivot | 2 | 2 | 6 | 5 | 3 | 6 | 3 | 4 | 5 | 4 | **50** |

**Why:**
- **(1):** the free calendar and the official apps already deliver deadlines plus a "worth it" label. What's left is an odds archive, which is too thin.
- **(2):** VABourbon covers Virginia at a **$2/mo** price anchor, an open-source tool exists, and the key data (limited-availability inventory) **is no longer public**.

**Verdict (per your rule): neither clears 70. Bourbon is out.** Finalist #3 becomes the highest-scoring remaining idea, **School-Choice Lottery Strategist, DC-first (69), labeled CONDITIONAL** with a 3-part validation gate on Oct 18. Other runners-up: Family Cookbook 66; pet insurance 65, but it's a module of #1 and so not eligible.

---

## 2. The final 3 at a glance

| | #2 Group Gift Decks | #3 School-Choice DC (conditional) | #1 Card Claims & Appeals |
|---|---|---|---|
| Score | 75 | 69 (gate) | 73 |
| Wedge | Gift formats + organizer nudges + printed deck; competitor MakeMyCards is party humor | Your odds + no-match risk on a capped 12-school list; competitors are scattered forum threads and official tables | Packet + appeal for your card version and denial reason, with outcome data; Kudos and CardPointers only say "you're covered" |
| Price | $39 printed · $15 PDF | $49 per child per season | $19 per claim · $49/yr Pass |
| Season | Holidays (print cutoff ≈ Nov 15) → Valentine's | Nov–Feb applications; results in March | Year-round; holiday travel peak |
| Launch | **Oct 26** | **≈ Nov 9–16** (if the gate passes) | **Dec 7** (free checker + SEO pages from Oct) |
| Budget to first revenue | ≈ $185 | ≈ $80–230 | ≈ $290 |

---

## 3. Build order and why

1. **Group Gift Decks first.** It has the hardest external deadline: holiday print cutoffs around mid-November mean it must launch by **Oct 26**. It's also the fastest to revenue (physical gift, clear pay moment) and the simplest build (3 weeks).
2. **School-Choice second, only if the gate passes (Oct 18).** The My School DC application window opens in early-to-mid November and closes in Feb/Mar. The build is small (3 weeks) and the data work starts in week 0 anyway.
3. **Card Claims third for the main build, but first for data.** It's the most durable business (year-round, compounding SEO + outcome data), and the benefits database needs weeks of careful transcription. So: **45 min/day of data and SEO work from week 0**, main build Nov 16–Dec 6, **launch Dec 7** just before holiday-travel disruptions.

**Focus rule:**
- At each day-30 checkpoint, if one product clearly beats its targets and another clearly misses, move **70% of build time** to the winner.
- If School-Choice fails its gate, its weeks go to Card Claims (earlier launch, around Nov 23).

---

## 4. Week 0 (Sep 28–Oct 4): validate all three in parallel

| Day | Group Gift Decks | School-Choice DC | Card Claims |
|---|---|---|---|
| **Mon** | Domain; Game Crafter account + **order 2 sample decks**; ask Claude Code to scaffold one shared landing template (Next.js) for all three | Download all My School DC / DME historical data; write down the rules | Download benefit guides (3 cards); hash + date them |
| **Tue** | Landing + template gallery + "Start your deck" fake door + $29 early-bird Stripe link | Landing + 5-school preview + $29 reservation link | Landing + mini-checker (3 rules) + $12 reservation link + Tally outcome form |
| **Wed** | Pinterest (15 pins), Etsy shop drafted, 10 seed-friend messages | Email 3 listserv moderators; start recruiting 8 interviews | 5 value-only Reddit answers (r/CreditCards, r/ChaseSapphire) |
| **Thu** | **Game Crafter API spike (2 h)**; 2 TikTok/Reels | Parse data to staging (Claude Code) | 5 more Reddit answers; r/churning weekly-thread comment |
| **Fri** | Facebook group promo-day posts | Backtest set: the 30 most oversubscribed programs | 2 blogger emails (data-story angle) |
| **Sat–Sun** | Review funnel data | Interviews | 5 more Reddit answers; review funnel data |

**Shared setup (Mon–Tue):** PostHog (one project per product, shared UTM convention), Stripe (one account, product-specific prices), Tally, a GitHub org with 3 repos from one template.

**Week-0 decision (Sun Oct 4):**
- **Decks:** pass if ≥ 10% start-deck clicks, ≥ 20 organizers with dates, ≥ 3 pre-orders, and sample quality OK.
- **Claims:** pass if ≥ 8% email capture, ≥ 6 reservations, ≥ 20 outcome stories. If it's in between, re-angle to appeals-only.
- **School:** continue to its full gate on **Oct 18** (G1 backtest ±10 pts on ≥ 70% of 30 programs; G2 ≥ 3% paid reservations on ≥ 300 targeted visitors; G3 ≥ 2 channel permissions + 8 interviews).

---

## 5. 12-week calendar (aligned to each product's season)

| Wk | Dates | Group Gift Decks | School-Choice DC | Card Claims |
|---|---|---|---|---|
| 0 | Sep 28–Oct 4 | **Validate** (landing, samples, API spike) | **Validate** (data, landing, interviews) | **Validate** (checker, Reddit, outcome form) |
| 1 | Oct 5–11 | Build: organizer + contributor flows | Model v0 + backtest | Data: 3→6 cards |
| 2 | Oct 12–18 | Build: renderer + preview + PDF | **Gate decision Oct 18** | Data: 6→9 cards · 5 SEO pages live |
| 3 | Oct 19–25 | Build: Stripe + print pipeline · Etsy live · 3 beta decks | Scaffold + data load (if the gate passed) | Data: 9→12 cards · 100 public data points |
| 4 | Oct 26–Nov 1 | **🚀 LAUNCH Oct 26** · gift-guide pitches | Explorer + program SEO pages | Data: 12→15 cards · 10 SEO pages |
| 5 | Nov 2–8 | Holiday countdown content · auto-nudges | Odds + list-risk + Stripe | Reddit answers continue |
| 6 | Nov 9–15 | **Holiday print cutoff ≈ Nov 15 (est.)** | **🚀 LAUNCH (application window opens)** | Attorney consult |
| 7 | Nov 16–22 | Switch to PDF + gift certificate | Listserv announcements | **Main build:** engine + wizard |
| 8 | Nov 23–29 | Day-30 check (Nov 25) | Deadline reminders | Build: result screen + Stripe |
| 9 | Nov 30–Dec 6 | Black Friday / Cyber Monday PDF promo | EdFEST content (Dec, est.) | Build: packet + appeal + reminders |
| 10 | Dec 7–13 | Valentine's templates (couples) | Day-30 check (≈ Dec 9–16) | **🚀 LAUNCH Dec 7** |
| 11 | Dec 14–20 | Pin 20/week for Valentine's | Holiday lull: SEO + guides | Storm-day posts · TikTok series |
| 12 | Dec 21–27 | Day-60 check (Dec 25) | Pre-deadline push planning | Holiday-travel disruption peak |
| → | Jan–Mar | Valentine's run (order-by ≈ late Jan) · final checkpoint Feb 20 | Deadlines (early Feb / ≈ Mar 1) · **results ≈ late Mar → waitlist watch** | Day-30 Jan 6 · r/churning data post (Jan 10) · bloggers |

---

## 6. Shared stack and fixed costs

- **One template for all three:** Next.js (TypeScript) PWA · Vercel Pro team (hosts all 3 projects) · Supabase (Postgres/Auth/Storage) · Stripe (Checkout + Portal + Tax where physical) · Resend (email) · PostHog · Sentry · Claude Code for build tasks · optional Claude Haiku 4.5 for small text features (≈ $0.001–0.01 per use).
- **Fixed monthly at full launch:** Vercel Pro $20 + Supabase Pro org $25 (+ ≈ $10 per extra project) → **≈ $55–75/mo total**, plus 3 domains (≈ $36/yr).
- **Cost to serve per user:** ≈ $0 digital. Decks pass print cost through (COGS ≈ $17–23 on a $39 order).

---

## 7. Portfolio budget and targets

| | Budget to first revenue | Week-12 target (after each product's launch) | Kill signal |
|---|---|---|---|
| Group Gift Decks | ≈ $185 | 200 paid orders · ≈ $7K cumulative | < 25 paid by day 30 |
| School-Choice DC | ≈ $80–230 | 160 families · ≈ $7.7K season | Gate fails · < 25 paid by day 30 |
| Card Claims | ≈ $290 | 220 packets + 40 Pass · ≈ $3K/mo run-rate | < 20 paid by day 30 |
| **Portfolio** | **≈ $555–705 total (each < $500)** | — | — |

**Honest expectation:**
- **Decks** are the most likely to show revenue inside 90 days (holidays + Valentine's).
- **School-Choice** is a seasonal side bet that must pass its gate.
- **Card Claims** is the slowest start but the most durable compounding asset (SEO + outcome data), and it's the best candidate to grow past $10K/mo over 12+ months.

---

## 8. Top portfolio risks

1. **Solo bandwidth (three products in 12 weeks).** Staggered launches, shared template, focus rule at day-30 checkpoints, and School-Choice is gated.
2. **Seasonality misses** (print cutoffs, the DC window). Hard dates are in the calendar; decks fall back to PDFs and gift certificates.
3. **Community channels restrict promotion.** Value-first answers, owned SEO pages, Etsy/Pinterest for decks, editorial and listserv routes for DC.
4. **Data accuracy for #1 and #3 destroys trust if wrong.** Versioned sources, public methodology, conservative wording, refunds.
5. **Legal edges** (claims: public adjuster / unauthorized practice of law; decks: user content and IP; DC: affiliation implications). The checklists are in each plan; one attorney hour before the Claims launch.

---

## 9. First 10 actions on Monday, Sep 28 (portfolio)

1. Pick 3 working names; check trademarks; buy 3 domains.
2. Create a Stripe account + 3 reservation/pre-order Payment Links ($29 deck, $29 DC plan, $12 claim packet).
3. Ask Claude Code to build **one** Next.js landing template, then fork it three times.
4. Order 2 Game Crafter sample decks; request a developer API key.
5. Download all My School DC / DME historical data into `/data/raw`.
6. Download and hash the benefit guides for Sapphire Reserve, Sapphire Preferred and Amex Platinum.
7. Set up PostHog (3 projects), Tally (outcome form), and a UTM convention.
8. Post 5 value-only answers in card-claim threads; save them as reusable snippets.
9. Message 10 friends with upcoming occasions (free seed decks) + 3 DC listserv moderators.
10. Put the 3 decision dates in the calendar: **Oct 4** (week-0 results), **Oct 18** (DC gate), **Oct 26** (deck launch).
