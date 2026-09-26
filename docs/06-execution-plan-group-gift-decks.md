# 06 — Execution Plan #2: Group Gift Decks

- **Working name:** *GroupDeck* (placeholder; check trademarks)
- **Score:** 75/130 (Round 2c)
- **Model:** $39 printed deck incl. US shipping · $15 print-at-home PDF · extra copies $22
- **Start:** week of **Mon Sep 28, 2026**
- **Target launch:** **Mon Oct 26, 2026**, to catch the holiday-gift window (print cutoff ≈ mid-November) and set up for Valentine's.
- **Build order in the portfolio:** **1st to launch** (most time-sensitive).

---

## 1. Pitch, user, wedge

- **One line:** "Everyone adds a card through one link. We print a real deck: '52 reasons we love you', 'who knows Mom best' trivia, 'open when…' notes, or advice for the newlyweds."
- **Target user:** the **organizer** (often 25–55) of a group gift for a milestone birthday, retirement, bridal shower or bachelorette, graduation, going-away, Valentine's, or a family holiday game night.
- **Wedge vs. the nearest competitor (MakeMyCards):** they do party humor (Cards-Against-Humanity style). **We do gift formats with an organizer dashboard, contributor nudges, a deadline lock, gift-grade printing and packaging, and an Etsy/Pinterest storefront.** Etsy hand-makers are slow, manual and single-author; we're instant and group-made.

---

## 2. Pre-build validation (week 0: Sep 28–Oct 4)

**Assets:**
- A landing page with a **template gallery**: 5 occasions, with mockups of real card fronts and backs made in Figma or Canva.
- A **"Start your deck"** fake door. Ask for occasion, honoree, event date and organizer email, and say "We'll open your deck link on Oct 26."
- An **early-bird pre-order**: "$29 printed deck (launch price $39)" via a Stripe Payment Link, refundable.
- **Order 2 sample decks** from The Game Crafter's web UI (≈ $10 each + shipping) to check print quality and real turnaround.
- **A 2-hour API spike:** get a Game Crafter developer key, create a game, deck and cards via the API, and confirm whether ordering to a customer's address can be automated (see §4). If not, plan a concierge fallback.

**Channels (no ads):**
1. **Personal network + 3 relevant Facebook groups** (bridal shower/bachelorette planning, milestone party ideas). Read each group's rules; many allow posts on "promo days" only.
2. **Pinterest:** create a business account; pin 15 mockups ("52 reasons we love you deck", "who knows the bride best cards"). Pinterest is slow, so start now for later compounding.
3. **TikTok/Reels:** 3 videos: the concept + a mock reading-reaction.
4. **Etsy:** open the shop and prepare listings (publish in week 3).

**Copy angle (A/B):**
- A: "The gift everyone made together: 52 reasons we love you, printed and shipped."
- B: "Turn the group chat into a real deck of cards for Mom's 60th."

**Pass/kill thresholds (end of week 1):**

| Metric | Pass | Kill |
|---|---|---|
| Landing visitors | ≥ 300 | — |
| "Start your deck" clicks | ≥ 10% | < 4% |
| Organizers leaving event details | ≥ 20 | < 5 |
| Early-bird paid pre-orders | ≥ 3 | 0 |
| Sample deck print quality | Gift-worthy | Poor → switch vendor (MakePlayingCards manual) |

---

## 3. MVP scope

**Must-have (v1):**
1. **Organizer flow:** pick occasion → honoree name/photo → template (52 reasons · trivia · open-when · advice · inside jokes) → set the **lock date** → get a share link.
2. **Contributor flow (no account):** open the link → add 1–5 cards with a short prompt ("A reason you love Linda", "A question only real fans of Linda can answer + the answer") → optional photo on the card back (v1: one shared back design).
3. **Organizer dashboard:** who has contributed, card count (goal 52), **nudge** button (email/SMS link), approve/edit/delete, **AI prompt suggestions** to fill gaps (optional).
4. **Auto-typesetting:** text-fit to the card safe zone, 3 visual themes, a cover/dedication card, a box design; **live preview** of the full deck.
5. **Checkout:** printed deck $39 (US shipping included) · PDF $15 · extra copies $22 · address collection.
6. **Print pipeline:** generate print-ready PNGs at 300 dpi → submit to The Game Crafter (API or concierge) → order tracking email.
7. **Print-at-home PDF:** 9 cards per page, US Letter, with cut marks, for last-minute buyers.
8. **Etsy bridge:** each Etsy listing leads to a personalization link after purchase.

**Explicitly NOT in v1:**
- Custom per-card photo layouts beyond one back image
- International shipping
- A game-rules engine or app-based play mode
- Bulk / corporate orders (not B2C)
- Subscription
- Native app
- Live multiplayer editing

**First-session pay-trigger screen:**
```
"52 Reasons We Love Linda" · 31 of 52 cards · 14 contributors · locks Nov 12
[Preview: fanned deck image + 3 real card faces + the printed box with Linda's photo]
✔ Nudge 6 people who haven't added a card yet
Ships by ~Nov 20 if ordered today (US ground)
[ Lock & print — $39 incl. shipping ]   [ Print-at-home PDF — $15 ]
```
*(Illustrative.)*

**Pricing + Stripe setup:**
- Stripe Checkout with `shipping_address_collection` (US only).
- Prices: `deck_print_39`, `deck_pdf_15`, `extra_copy_22`.
- **Stripe Tax on** (physical goods).
- Coupon `EARLY29` for week-0 pre-orders.
- Refunds: reprint for print defects; no refund after the deck is locked and sent to print (stated at checkout).

---

## 4. Tech stack and architecture

- **Next.js** (TypeScript) PWA on **Vercel Pro** (shared).
- **Supabase** (Postgres, Storage for images, Auth magic link for organizers; contributors use signed tokens).
- **Card rendering:** a server-side renderer (e.g. `@vercel/og`/Satori + `resvg`, or `sharp` with SVG templates) produces PNGs at **poker size with bleed (≈ 825 × 1125 px at 300 dpi; confirm against The Game Crafter's template in week 0)**. Text-fitting uses binary search on font size with minimum and maximum limits.
- **Print partner: The Game Crafter** API: create game → deck → bulk-create cards with face images → add to cart → order ([Deck API](https://www.thegamecrafter.com/developer/Deck.html), [Card API](https://www.thegamecrafter.com/developer/Card.html), [API overview](https://help.thegamecrafter.com/article/150-developer-api)).
  - ≈ $9.99/deck ([TGC](https://help.thegamecrafter.com/article/48-custom-playing-cards)); a printed [Poker Tuck Box (54)](https://www.thegamecrafter.com/make/products/PokerTuckBox54) costs extra.
  - **Unknown to verify in week 0:** whether checkout and shipping to a customer address can be fully automated via the API. **Fallback:** a concierge flow. The app produces a ready-to-upload ZIP and you place the order in the Game Crafter UI (≈ 5 min/order). That's fine for the first ~50 orders.
  - Backup vendor: MakePlayingCards (full custom faces, manual ordering, ships from overseas).
- **Email/SMS nudges:** Resend (email); SMS optional later (Twilio ≈ $0.008/msg).
- **Optional AI:** Claude Haiku 4.5 for prompt suggestions (≈ $0.001/deck).
- **Analytics:** PostHog. **Errors:** Sentry.

**Data model (sketch):**
```
template(id, occasion, card_type, prompts jsonb, theme jsonb, card_count_default)
deck(id, organizer_id, template_id, honoree_name, honoree_photo, event_date, lock_at, status, theme, cover_text)
contributor(id, deck_id, display_name, email?, token, invited_at, last_nudged_at)
card(id, deck_id, contributor_id, kind, front_text, back_text?, image_url?, approved, position)
order(id, deck_id, stripe_session_id, kind['print','pdf','extra'], qty, ship_to jsonb,
      print_vendor, vendor_game_id, vendor_order_id, status, tracking_url, created_at)
```

**Upkeep workflow for "versioned rules":**
- **Print specs** (card template, box template, vendor price) live in a config table with an `effective_from` date.
- **The holiday-cutoff calendar** (per vendor, per shipping method) is updated every September and January.
- **Prompt library:** A/B test prompts; keep the ones with the highest completion rate (this is the outcome-data moat).

**Costs:**
- Per printed deck: vendor ≈ $10–14 (deck + printed box), US shipping ≈ $5–8, Stripe ≈ $1.45 → **COGS ≈ $17–23**. Gross profit ≈ $16–22 direct, ≈ $11–16 via Etsy.
- PDF: ≈ $0.75 Stripe → ≈ $14 gross profit.
- Fixed: domain + a share of hosting (≈ $15–25/mo).

---

## 5. Week-by-week build plan

| Week | Dates | Tasks |
|---|---|---|
| 0 | Sep 28–Oct 4 | Landing + gallery + fake door · sample decks ordered · Game Crafter API spike · Etsy shop created |
| 1 | Oct 5–11 | Schema + migrations · organizer flow (templates, lock date, share link) · contributor flow with token links · dashboard with counts and nudge (Resend) |
| 2 | Oct 12–18 | Card renderer (SVG→PNG, text-fit, 3 themes, bleed/safe zone) · full-deck preview (web) · print-at-home PDF (9-up with cut marks) · unit tests for text-fit edge cases (long answers, emoji) |
| 3 | Oct 19–25 | Stripe Checkout + webhooks · Game Crafter integration (API or concierge ZIP export) · order admin page · order emails · 5 Etsy listings live · 3 beta decks with real friends' groups |
| 4 | **Oct 26 launch** | Launch · fix list · holiday cutoff banner ("order by Nov 15 for Christmas, est.") · PostHog funnels (started → 20 cards → locked → paid) |
| 5–6 | Nov 2–15 | Contributor reminders (auto-nudge 72h and 24h before lock) · AI prompt suggestions · referral: "Make your own deck" link on every printed box card |
| 7–12 | Nov 16–Dec 27 | After the print cutoff: sell the **PDF + "printed deck arrives in January" gift certificate** · plan the Valentine's templates (couples 52 reasons) · pin 20/week for Valentine's |

---

## 6. Go-to-market (first 90 days after launch, Oct 26 → Jan 24)

**Channel by channel:**

| Channel | Rules / notes | Plan |
|---|---|---|
| **Etsy** | Print-on-demand allowed **only with production-partner disclosure** ([Etsy POD rules](https://www.listadum.com/blog/understanding-etsys-rules-for-print-on-demand-sellers)); fees ≈ 6.5% + 3% + $0.25 + $0.20/listing; Offsite Ads 12–15% on attributed sales | 5 listings at launch (52 reasons · who knows the bride best · retirement trivia · open-when · newlywed advice), 10 by December; buyers get a personalization link |
| **Pinterest** | Organic; pins take 30–90 days to rank | 20 pins/week; boards per occasion; link to SEO pages |
| **TikTok / IG Reels** | Organic | 3/week: honoree reading-reaction videos (ask the first 20 customers for clips in exchange for a free extra copy) |
| **Facebook groups** (bridal shower/bachelorette planning, milestone party ideas, retirement parties) | Most restrict promotion to specific days | Share in promo threads; answer "gift idea" posts |
| **Reddit:** r/Weddingsunder10k (229K), r/weddingplanning, r/bachelorette, r/GiftIdeas | Self-promotion usually banned; verify each sub | Helpful answers only; link when explicitly allowed |
| **Built-in invites** | Each deck exposes 5–30 contributors | A "Make one for someone you love" card in every printed box + contributor confirmation email CTA |
| **Gift-guide bloggers** | Holiday guides close late Oct–early Nov | Pitch 20 "unique gift" bloggers in week 4 with a free sample deck |

**20 SEO / programmatic pages** (question lists + builder CTA):
1. "who knows the bride best questions"
2. "how well do you know the couple questions"
3. "bachelorette trivia questions about the bride"
4. "52 reasons why I love you ideas" (+ for mom / dad / grandma / wife / husband: 5 pages)
5. "open when letters ideas" (+ college / deployment / long distance: 3 pages)
6. "retirement trivia questions about coworker"
7. "50th birthday trivia questions about mom"
8. "60th birthday gift ideas from family"
9. "advice for the newlyweds cards ideas"
10. "going away gift from group ideas"
11. "family trivia questions about grandparents"
12. "graduation gift from family ideas"
13. "valentines gift 52 reasons deck"

(Items 4 and 5 expand into separate pages, 20 pages in all.)

**Launch sequence:**
- Oct 26: soft launch to week-0 organizers (they start real decks).
- Oct 28: Etsy listings boosted with 3 reviews from friends' real orders.
- Nov 1: gift-guide pitches.
- Nov 1–15: "order by Nov 15" countdown content.
- Nov 16–Dec 20: PDF + gift certificate.
- Jan 2: the Valentine's campaign starts. Order-by date ≈ late January (confirm the vendor cutoff).

**Seeding the first users and the "outcome" data:**
- 5 free decks for real occasions in your network (reviews + videos).
- Track which prompts get completed and which get skipped to improve templates weekly.

---

## 7. Metrics and kill criteria

**Weekly targets (weeks after the Oct 26 launch):**

| | Week 2 (Nov 8) | Week 4 (Nov 22) | Week 8 (Dec 20) | Week 12 (Jan 17) |
|---|---|---|---|---|
| Visitors (cumulative, site + Etsy) | 1,500 | 4,000 | 8,000 | 12,000 |
| Decks started | 120 | 350 | 700 | 1,000 |
| Decks reaching 20+ cards | 50% of started | 50% | 55% | 55% |
| Paid orders (cumulative) | 20 | 60 | 130 | 200 |
| Revenue (cumulative) | $700 | $2,100 | $4,500 | $7,000 |

**Unit economics:**
- Average order value ≈ $35 (print/PDF/extra-copy mix).
- Gross profit ≈ $17 on a direct print order.
- Customer acquisition cost ≈ $0 (organic) + Etsy fees.
- Viral hook: at least 1 in 20 contributors starts their own deck within 90 days.

**Kill/pivot criteria:**
- **Day 30 (Nov 25):** < 25 paid **or** < 35% of started decks reaching 20 cards → pivot to **single-author "52 reasons" decks** (no group), sold mainly on Etsy.
- **Day 60 (Dec 25):** < 80 paid → cut to the 2 best templates; focus everything on Valentine's.
- **Day 90 (Jan 24):** < $1,500/mo run-rate going into Valentine's → **final checkpoint Feb 20.** If Valentine's also misses (< 150 orders in Jan 25–Feb 14), stop and keep the Etsy listings passive.

---

## 8. Legal and compliance checklist

- [ ] **Content policy:** a report button; organizer approves every card before print; block hateful or explicit content from printing; organizer accepts responsibility for content.
- [ ] **IP:** no trademarked game names ("Cards Against Humanity", "Trivial Pursuit", etc.). Users must own any photos they upload (checkbox). No song lyrics or brand logos on cards.
- [ ] **Etsy:** disclose The Game Crafter as a production partner; the item description must match the product (print-on-demand, made to order).
- [ ] **Shipping promises:** show *estimated* delivery only; the holiday cutoff is labeled "estimated, not guaranteed".
- [ ] **Custom-goods refund policy:** reprint for defects; no refund after lock (shown before payment).
- [ ] **Sales tax:** Stripe Tax for direct sales; Etsy collects as the marketplace facilitator.
- [ ] **Privacy:** contributor emails used only for this deck; CAN-SPAM-compliant nudges; delete contributor emails 30 days after print.
- [ ] **Children:** contributors must be 13+; kids' cards are entered by a parent (avoids COPPA).

---

## 9. Top 5 risks and mitigations

| Risk | Mitigation |
|---|---|
| Contributors don't show up → deck never locks or gets bought | Auto-nudges, a 20-card minimum, AI prompt suggestions, organizer "fill-in" mode, smaller 30-card decks |
| Print quality, delays or holiday queue → refunds and bad reviews | Sample orders in week 0, conservative cutoffs, backup vendor, proactive status emails |
| Game Crafter API can't automate checkout | Concierge ordering for the first 50 orders; revisit automation after proof |
| Seasonal revenue cliff after the holidays | Valentine's, showers and graduations; year-round birthday and retirement templates |
| MakeMyCards / Inside Joke copy the gift formats | Speed, Etsy reviews, Pinterest SEO depth, template completion data, packaging quality |

---

## 10. Budget to first revenue (target < $500)

| Item | Cost |
|---|---|
| Domain | $12 |
| 2–3 sample decks + shipping (Game Crafter) | ~$45 |
| Etsy listing fees (10 listings) | $2 |
| Vercel Pro / Supabase share (2 months) | ~$25 |
| 5 free seed decks for network occasions | ~$100 |
| **Total** | **≈ $185** |

**First 10 actions on Monday (Sep 28):**
1. Pick a working name; check trademarks and domain; buy the domain.
2. Open a Game Crafter account and developer API key; order 2 sample poker decks with test designs.
3. Ask Claude Code to scaffold a landing page with a template gallery + "Start your deck" fake door + Stripe early-bird Payment Link ($29).
4. Design 5 template mockups (52 reasons, bride trivia, retirement trivia, open-when, newlywed advice).
5. Create an Etsy seller account; draft 5 listings (don't publish yet).
6. Create a Pinterest business account; pin 15 mockups.
7. Message 10 friends with upcoming occasions and offer a free deck (seed users).
8. Join 3 bridal/party-planning Facebook groups; read and save their promo rules.
9. Film 2 short concept videos (TikTok/IG).
10. Do the 2-hour Game Crafter API spike: create a game + deck + 3 cards via API; document how ordering works.
