# 06 — Execution Plan #3 (CONDITIONAL): School-Choice Lottery Strategist, DC-first

- **Working name:** *LotteryOdds DC* (placeholder; must not imply any affiliation with My School DC or DCPS)
- **Score:** **69/130: conditional.** It replaced the Bourbon Lottery Desk after the Round 3 re-score (see `06-summary.md` §1).
- **Model:** $49 per child per season (odds + list-risk + deadlines + waitlist watch through August). Free school pages.
- **Start:** week of **Mon Sep 28, 2026**
- **Gate decision:** **Sun Oct 18.** Build **only if the validation gate passes** (§2).
- **Target launch:** **≈ Mon Nov 9–16, 2026**, timed to the My School DC 2027–28 application opening. Historically it opens in early-to-mid November; the 2026–27 grades 9–12 deadline was Feb 2, 2026; results came out Mar 27, 2026. Exact 2027–28 dates are **not yet published** ([DCSchools.com](https://dcschools.com/dc-school-lottery), [Mayor's release](https://mayor.dc.gov/release/mayor-bowser-reminds-families-complete-my-school-dc-lottery-2026-27-school-year)).

---

## 1. Pitch, user, wedge

- **One line:** "See your child's real odds at every DC school you're considering, and a list that won't leave you unmatched."
- **Target user:** DC parents applying through **My School DC**, especially **PK3/PK4 and K** (the most contested entry grades), plus grades 5/6 and 9. DC has 10,000+ lottery applications a year ([DCmoms](https://dcmoms.com/ages-stages/school-age/the-daunting-dc-school-lottery-system/)).
- **Why DC first:** My School DC **caps lists at 12 schools** ([FAQ](https://www.myschooldc.org/faq/faqs)). With a capped list, the matching algorithm is **not strategy-proof**, so *which* schools to list is real strategy. DC also publishes **historical seats and waitlist data back to 2014–15** ([How waitlists work](https://www.myschooldc.org/how-waitlists-work), [DME EdSight](https://dme.dc.gov/node/1452086)).
- **Wedge vs. the nearest competitors:**
  - DCUM threads (e.g. "Lottery Nerd – Waitlist predictions" ([DCUM](https://www.dcurbanmom.com/jforum/posts/list/150/1320333.page))) and official tools give scattered, school-by-school numbers.
  - **We model *your* priorities (in-boundary, sibling, proximity) across *your* 12-school list and show the chance of being left with no match, and how to fix it.**
  - Consultants cost hundreds or thousands; we cost $49.

---

## 2. Validation gate (weeks 0–2: Sep 28–Oct 18). **Must pass all 3 to build.**

**G1: Can we predict? (desk work, ≈ 10 h)**
- Download historical My School DC data (seats offered, applicants and waitlist lengths by school/grade; preference-group breakdowns where published).
- Build a simple model on 2023–24 + 2024–25 data. **Backtest it against 2025–26 outcomes** for the **30 most oversubscribed PK3/PK4/K programs**.
- **Pass:** predicted match rate or waitlist position is within **±10 percentage points** for **≥ 70%** of those programs.
- **Kill:** if priority-group data is too sparse to estimate anything better than "high/medium/low".

**G2: Will parents pay? (landing + smoke test)**
- A landing page: "See your odds before you rank: DC school lottery 2027–28". A free odds preview for 5 sample schools; "$49 full plan, reserve now for $29", refundable, charged at launch.
- **Channels:** DCUM "Schools" forum participation (value-only answers, **no promotion**; DCUM is anti-commercial, and paid advertising is an option later), r/washingtondc (verify rules), 3 neighborhood parent listservs (ask moderators first), 2 preschool parent groups (PK3 feeders), a Washington Parent magazine contact ([Aug 2026 lottery article](https://washingtonparent.mydigitalpublication.com/publication/?i=868219&article_id=5188728&view=articleBrowser)).
- **Pass:** ≥ **300 targeted visitors**, ≥ **3% paid reservations** (≥ 9), ≥ **10% email signups**.

**G3: Can we reach them?**
- **Pass:** ≥ **2 channels** give explicit permission to post (moderator OK, newsletter placement, or a listserv announcement).
- **Plus:** ≥ **8 parent interviews** (15 min) confirming they would use odds + list-risk.

**If any gate fails → don't build.** The portfolio proceeds with 2 finalists; optionally keep a free DC deadline calendar as an SEO asset.

---

## 3. MVP scope (only if the gate passes)

**Must-have (v1):**
1. **Family profile (no child PII):** grade, home address → converted immediately to boundary school(s) + distance bands, **then the raw address is discarded**; sibling/staff priorities as checkboxes.
2. **School explorer:** programs eligible for that grade, with historical seats, waitlist lengths and trend (free).
3. **Odds per school for *this* family** (by priority group), with a confidence band and a short "why".
4. **List builder + list-risk score (paid):** order up to 12 schools. We show **P(no match)**, **expected best match** and a "swap suggestion" (e.g. "Adding X as school #9 cuts your no-match risk from 23% → 7%").
5. **Deadlines and tours:** application window, open houses, the EdFEST school fair (usually December), and the ranking deadline, with email reminders.
6. **Results & waitlist watch (included, Mar–Aug):** enter your results + waitlist numbers; see historical waitlist movement for those schools; outcome capture feeds next year's model.

**Explicitly NOT in v1:**
- Other cities (SF, NYC K, Boston come only after a successful DC season)
- Private schools
- School reviews or ratings (user-content moderation, defamation risk)
- Auto-submitting applications
- Any paid consulting
- A native app

**First-session pay-trigger screen:**
```
PK3 · In-boundary: [Your boundary ES] · Sibling: none · 8 schools listed
Your list: 23% chance of NO match ⚠️   Expected best match: #4 (est.)
School #1 [Program A]: ~6% (±4) · School #2 [Program B]: ~18% (±7) ...
Fix: add 2 "likely" programs at positions 9–10 → no-match risk 7%
[ See full odds, swap suggestions, deadlines & waitlist watch — $49 ]
Estimates from public My School DC data 2019–2026. Not affiliated with My School DC or DCPS.
```
*(Illustrative numbers and school names.)*

**Pricing + Stripe setup:** Stripe Checkout one-time `family_season_49` (per child per season); second child $29 (`sibling_29`); coupon `EARLY29`; 14-day refund; no subscription.

---

## 4. Tech stack and architecture

- **Next.js** PWA on **Vercel Pro** (shared); **Supabase** Postgres; **Resend** for deadline emails; PostHog.
- **Data pipeline:** Python or TypeScript scripts in `/data` pull My School DC / DME published tables (CSV/XLSX/PDF → parsed with pdfplumber if needed) into staging, then human-reviewed into production tables, **versioned by lottery year**.
- **Odds model v1 (transparent, calibratable):** for each program × grade × priority group, estimate the admit probability from historical offers ÷ applicants in that group, trend-adjusted. The list-risk estimate is P(no match) ≈ ∏(1 − pᵢ) over listed schools (independence approximation), **calibrated against the backtest**. v2: Monte Carlo simulation of deferred acceptance with priority tiers.
- **Geo:** DC boundary shapefiles (Open Data DC) → boundary lookup; distance bands computed server-side; the address is not stored.

**Data model (sketch):**
```
program(id, school_name, sector['DCPS','charter'], grade, program_type, address_geo, active_years)
seat_history(program_id, lottery_year, seats_offered, applicants, waitlist_at_results, by_priority jsonb, source_url)
priority_rule(lottery_year, sector, rule_code, description, source_url)      -- versioned yearly
family(id, grade, boundary_school_ids[], distance_bands jsonb, priorities jsonb, email)  -- no child name/DOB
list(id, family_id, program_ids[], risk_no_match, expected_rank, computed_at, model_version)
outcome(id, family_id|null, program_id, lottery_year, matched bool, waitlist_number, updated_at)
deadline(lottery_year, event, date, source_url)
```

**Upkeep workflow:**
- **Every Sep–Oct:** ingest the prior year's final data, re-fit the model, re-run the backtest, publish the model version + accuracy on a **public methodology page**.
- **Every Nov:** load new-year rules and deadlines.
- **Mar–Aug:** ingest user-reported waitlist movement weekly.

**Costs:** per user ≈ $0; fixed ≈ $15–25/mo (portfolio share) + domain.

---

## 5. Week-by-week plan

| Week | Dates | Tasks |
|---|---|---|
| 0 | Sep 28–Oct 4 | Download all historical data; landing page + 5-school preview; Stripe reservation link; start parent interviews |
| 1 | Oct 5–11 | Parse data into staging; build model v0; backtest notebook; listserv moderator outreach |
| 2 | Oct 12–18 | Finish backtest; G2 traffic push; **gate decision Sun Oct 18** |
| 3 | Oct 19–25 | *(only if the gate passed)* Next.js scaffold, schema, data load, boundary lookup |
| 4 | Oct 26–Nov 1 | School explorer + free program pages (programmatic SEO for ~150 programs) |
| 5 | Nov 2–8 | Family profile → odds → list builder + risk score; Stripe; reminders |
| 6 | **Nov 9–15 launch** | Launch aligned to the application opening; methodology page; privacy/disclaimer pages |
| 7–12 | Nov 16–Dec 27 | EdFEST content; "How many schools to list" guides; weekly model notes; December traffic push |
| After | Jan–Mar | Deadline push (early Feb for 9–12, ~Mar 1 for PK3–8, based on past years; confirm when published); **Mar: results → waitlist watch** |

---

## 6. Go-to-market (first 90 days after launch: Nov 9 → Feb 7)

| Channel | Rules / notes | Plan |
|---|---|---|
| **DC Urban Moms and Dads (DCUM)** Schools forum | Anonymous forum, very active (a "2025 kindergarten picks" thread hit 500 replies ([Brookings study](https://www.brookings.edu/wp-content/uploads/2021/03/Discussions_DC_public_school_options_online_forum_Brookings-Report.pdf) of the forum)); promotion is unwelcome | Value-only data answers ("historical waitlist for X"); consider a small DCUM ad in Dec–Jan if the gate showed willingness to pay |
| Neighborhood listservs (Capitol Hill, Petworth, Brookland, Shaw…) | Moderator approval | One announcement per list: "free DC lottery odds pages + deadline calendar" |
| Preschool & daycare parent groups | Director or room-parent sharing | A one-page PDF "PK3 lottery timeline + how to build a safe list" with our link |
| r/washingtondc | Verify rules | Helpful answers on lottery threads |
| Washington Parent, DCmoms.com, local newsletters | Editorial | Pitch "what the data says about DC's lottery" in November |
| **EdFEST** (DC's public school fair, usually December) | Public event | Post EdFEST prep guides; hand out QR flyers outside if allowed |

**20 SEO / programmatic pages:**
1. "My School DC lottery odds"
2. "My School DC how many schools to rank"
3. "My School DC waitlist movement"
4. "DC PK3 lottery odds"
5. "DC kindergarten lottery tips"
6. "DC charter school lottery odds [year]"
7. "in-boundary priority DCPS explained"
8. "sibling priority My School DC"
9. "My School DC deadline 2027"
10. "My School DC results date"
11. "what happens if you don't match My School DC"
12. "My School DC waitlist number good or bad"
13. "EdFEST DC guide"
14–20. **Per-program pages** for the ~150 most-searched programs ("[School name] lottery odds PK3", "[School name] waitlist"), programmatically generated from public data, each with the historical chart and a free odds preview.

**Seeding outcomes:** in March, invite all users (and DCUM readers) to report results and waitlist numbers anonymously → a public "waitlist movement tracker" (free) that is the hook for the next season.

---

## 7. Metrics and kill criteria

**Weekly targets (weeks after the ≈ Nov 9 launch):**

| | Week 2 | Week 4 | Week 8 | Week 12 |
|---|---|---|---|---|
| Visitors (cumulative) | 1,200 | 3,500 | 7,000 | 10,000 |
| Free odds checks | 250 | 700 | 1,500 | 2,200 |
| Paid families (cumulative) | 12 | 40 | 100 | 160 |
| Season revenue (cumulative) | $550 | $1,900 | $4,800 | $7,700 |

**Unit economics:** average order value ≈ $48 (with sibling add-ons); gross margin ≈ 97%; customer acquisition cost ≈ $0–5 (optional DCUM ad). **Seasonal:** most revenue falls in Nov–Feb.

**Kill/pivot criteria:**
- **Day 30:** < 25 paid → keep only the free SEO pages; stop paid-feature work.
- **Day 60:** < 80 paid → no multi-city expansion next year.
- **Day 90:** < $4K season revenue → sunset paid; keep the free waitlist tracker. If ≥ $6K **and** model accuracy is confirmed at results (Mar 27-ish) → plan SF + NYC K for the 2028–29 season.

---

## 8. Legal and compliance checklist

- [ ] **No affiliation:** "Not affiliated with My School DC, DCPS, DC PCSB or DME." No logos. School names used descriptively only.
- [ ] **Estimates only:** every number shows a confidence band + model version; a public methodology page; no guarantees.
- [ ] **Data sources:** public data only, with citations; respect site terms (download published files, no aggressive scraping).
- [ ] **Privacy:** no child name or birthdate; the address is converted to boundary + distance then discarded; minimal parent email; a privacy policy; deletion on request.
- [ ] **No user reviews of schools** (avoids moderation and defamation issues).
- [ ] **Consumer protection:** clear refund policy (14 days); no "beat the lottery" claims.

---

## 9. Top 5 risks and mitigations

| Risk | Mitigation |
|---|---|
| The model can't beat "high/medium/low" | Gate G1; publish accuracy; fall back to a free tool if it fails |
| One selling season per year → slow learning, small revenue | Treat it as a seasonal side product; waitlist watch builds year-2 data; expand cities only after proof |
| Community hostility to a paid product (DCUM) | Lead with free data; use editorial and listserv channels; small ads only if validated |
| Rule changes per year (priorities, dates) | Versioned `priority_rule` + `deadline` tables; November refresh checklist |
| Liability if a family goes unmatched | Clear probability language, confidence bands, a "safety school" recommendation always shown |

---

## 10. Budget to first revenue (target < $500)

| Item | Cost |
|---|---|
| Domain | $12 |
| Hosting share (2 months) | ~$25 |
| Optional DCUM ad test (Dec) | $0–150 |
| QR flyers for EdFEST | ~$40 |
| **Total** | **≈ $80–230** |

**First 10 actions on Monday (Sep 28):**
1. Download every published My School DC / DME lottery and waitlist dataset (2019–2026) into `/data/raw` with source URLs.
2. Write down DC's lottery rules (priorities, 12-school cap, tie-breaking) with citations in `/data/rules/2026.md`.
3. Ask Claude Code to parse the data into a single `seat_history` table (staging).
4. Pick the 30 most oversubscribed PK3/PK4/K programs for the backtest.
5. Scaffold the landing page with a 5-school free preview + $29 reservation link.
6. Email 3 neighborhood listserv moderators asking permission to share a free lottery-data resource.
7. Recruit 8 parents for 15-min interviews through preschool contacts and listservs (DCUM is anonymous, so it isn't a recruiting channel).
8. Draft the methodology page (how odds are estimated, known limits).
9. Set a calendar alarm for the My School DC 2027–28 dates announcement.
10. Put the gate criteria (G1–G3) into a one-page scorecard to decide on **Oct 18**.
