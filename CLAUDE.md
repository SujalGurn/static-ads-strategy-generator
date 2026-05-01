# Email Skills — Project Context

## What This Project Is

A Figma + Claude workflow for building high-converting email campaigns. The user designs in Figma using the **Email Love HTML Email Builder** plugin, which exports production-ready responsive HTML. Claude handles strategy, copy, MJML code, and campaign sequencing.

**Current active campaign:** Back-in-Stock — Full Restock, All Styles (Summit Socks)

---

## Model

Using **Claude Opus 4.6** (`claude-opus-4-6`) for maximum output quality.
Set in: `/Users/sujalgurung/.claude/settings.json`

---

## Tool Stack

### Figma + Email Love Plugin
- Plugin: [Email Love HTML Email Builder](https://www.figma.com/community/plugin/1387891288648822744/email-love-html-email-builder)
- Working Figma file: `figma.com/design/wNmDJC0ZdTyr0Ar0DPIJpt/emails` (file key: `wNmDJC0ZdTyr0Ar0DPIJpt`)
- Email Love exports: HTML (Klaviyo-ready) + image blocks hosted on `asset.emaillove.com` CDN
- Export format: Klaviyo `kl-section`/`kl-column` table structure (not raw MJML)

### Figma MCP
- Configured in `~/.claude/settings.json` — sources token from `.env` via bash wrapper
- Token stored in: `/Users/sujalgurung/email skills/.env` → `FIGMA_PERSONAL_ACCESS_TOKEN`
- **✅ TOKEN VALID** (confirmed 2026-04-18)
- Claude can read Figma frames, layers, text, styles directly via API

### ESP
- **Klaviyo** — HTML paste-in via code editor
- Liquid tags: `{{ first_name|default:"there" }}`, `{% unsubscribe_link %}`, `{{ manage_preferences_url }}`

### Email Code Format
- Email Love HTML (from Figma plugin) → paste directly into Klaviyo ✓
- MJML (from Claude) → compile at mjml.io/try-it-live → paste into Klaviyo ✓
- Both formats are valid — Email Love HTML is preferred when designs come from Figma

---

## Creative Rule — CRITICAL

**Every email must have a unique creative concept.** Never repeat the same layout, section structure, or visual approach from a previously created email unless explicitly asked.

Each new email should differ in at least 2 of:
- Layout structure (hero image top vs split vs text-first vs grid)
- Colour treatment (background colour, CTA colour, accent use)
- Typography approach (headline size, weight, letter-spacing)
- Copy angle (urgency vs social proof vs story vs objection-first)
- Section order (reviews placement, trust strip position, P.S. usage)

When creating: reference the inspiration files first → extract what's visually distinctive → translate that creative energy into Summit Socks brand, not copy the layout verbatim.

---

## Skill Files (in this directory)

| File | Purpose |
|---|---|
| `SKILL.md` | Skill trigger config |
| `campaign-frameworks.md` | Full sequences: BIS, cart, welcome, winback, etc. |
| `email-copy-patterns.md` | Subject line formulas, CTA patterns, power words |
| `email-marketing-copy.skill` | Binary skill bundle |
| `brand-context-summitsocks-2026-04-15.md` | Full Summit Socks brand context |

---

## Brand: Summit Socks

**Site:** summitsocks.com.au · summitsocks.co
**Market:** Australia (primary), New Zealand (secondary)
**Category:** Premium alpaca socks, DTC
**Tagline:** *"Comfort that climbs with you."*
**Voice:** Grounded, honest, quietly confident. Like a tradie who did the research and found what works.
**ESP:** Klaviyo
**Price anchor:** Buy 2 Get 1 Free (most popular) — Boot Socks drop $74.99 → $50/pair AUD · Buy 4 Get 4 Free also available · Mix & match styles/colours/sizes to qualify · AOV ~$132 AUD

### Product Catalog

| SKU | Price | Alpaca% | Reviews | Notes |
|---|---|---|---|---|
| Alpaca Boot Socks ⭐ HERO | $74.99 | 70% | 255+ reviews, 89% ★ | Mid-calf, full-cushion. B2G1 = $50/pair. |
| Alpaca Ankle Socks | $49.99 | 63% | 270+ reviews, 86% ★ | Highest review count. Daily wear. |
| Alpaca Crew Socks | $59.99 | 65% | 170+ reviews, ~85% ★ | ⚠ Calf tightness reviews — avoid "compression" language |
| Alpaca No-Show Socks | $44.99 | 61% | 82+ reviews, ~85% ★ | Newest. Sneakers/casual. |

### Key Differentiators
- 70% Premium Peruvian Baby Alpaca (Boot Socks)
- Lanolin-free → hypoallergenic, no itch
- Naturally antimicrobial → no odour treatment needed
- Semi-hollow fibre → thermoregulates (warm in cold, breathable in heat)
- "3x more breathable than wool" · "softer than cashmere"

### Trust Signals
- 100-Day Comfort Guarantee (full refund)
- Afterpay on all SKUs
- Australia Post: Metro Express 1–2 days / Standard 2–4 days · Regional Express 1–3 days / Standard 3–8 days
- Free standard shipping over $89 AUD · Express $14.99 · Standard $8.99
- 775+ total reviews, ~87% five-star

### Audiences
*(Based on 80+ customer conversations and 3,733 orders — ~60–65% male, primary age 45–70)*

| Segment | Share | Profile | Pain Point | Best Product |
|---|---|---|---|---|
| Tradies & boot wearers | ~30% | Male 30–60, metro + regional AU | Comfort in work boots, fatigue, smell | Boot Socks Black/Grey L/XL |
| Health & circulation | ~20% | 60+, mixed gender | Non-restrictive fit, sensitive skin, diabetic-friendly | Crew/Boot Socks — non-binding |
| Everyday comfort | ~20% | Broad 30–70+, metro | Quality everyday socks, winter warmth | Ankle Socks (most popular) |
| Gift buyers | ~15% | Often female, buying for male | Practical premium gift, sizing confusion | Bundles — guide carefully |
| Outdoor & adventure | ~15% | Male 30–55, AU + NZ | Performance hiking/fishing/4WD | Boot + Crew, Grey/Black, Large |

**Top products by volume:** Ankle Socks 37%, Boot Socks 28%, Crew Socks 21%, No-Show 14%
**Top colours:** Black 61%, Grey 35%, Cloud White 4%
**Top sizes:** Medium 54%, Large 41%, XL 5%

### Creative Constraints
- ⛔ Avoid: compression/snug fit as benefit (calf complaints)
- ⛔ Avoid: sustainability/ethical sourcing claims (no certification)
- ⛔ Avoid: medical/health condition claims
- ⛔ Avoid: "most reviewed" comparisons (775+ vs Hollow's 21K)
- ✅ Lead: Boot Socks + B2G1 bundle deal
- ✅ Lead: Alpaca vs merino fibre advantage
- ✅ Lead: Australian proximity (vs US competitors)
- ✅ Lead: Price advantage vs Hollow Socks (~$78 AUD) on B2G1 = $50 AUD

---

## Campaign Files

### Back-in-Stock — Full Restock (All Styles)
`/email skills/campaigns/back-in-stock/`
Full strategy: `campaign-strategy.md`

**11 MJML email files — two segments:**

#### Waitlist Segment (High-Intent)
| File | Email | Send | Creative | Image |
|---|---|---|---|---|
| `w1-a-waitlist-clean.mjml` | W1-A | Immediate | Clean/minimal, white bg | m1-13.jpg |
| `w1-b-waitlist-socialproof.mjml` | W1-B | Immediate | Review-led, grey bg | 20-Summit Socks-3.jpg |
| `w1-c-waitlist-warmurgency.mjml` | W1-C | Immediate | Warm/scarcity, cream bg | m1-5.jpg |
| `w2-a-nudge-urgency.mjml` | W2-A | +24hr | Stock depletion, split layout | m1-6.jpg |
| `w2-b-nudge-bundle.mjml` | W2-B | +24hr | Bundle pricing grid, value | 9-Alpaca Socks-10.jpg |

#### General List Segment (Dormant 2-3 months)
| File | Email | Send | Creative | Image |
|---|---|---|---|---|
| `g1-a-general-honest.mjml` | G1-A | Immediate | Founder letter, cream bg | m1-13.jpg |
| `g1-b-general-seasonal.mjml` | G1-B | Immediate | Seasonal angle, white bg | 20-Summit Socks-3.jpg |
| `g1-c-general-reviews.mjml` | G1-C | Immediate | 3 review quotes, grey bg | 9-Alpaca Socks-10.jpg |
| `g2-a-general-fullrange.mjml` | G2-A | +48hr | 2×2 product grid | 4 images |
| `g2-b-general-ankledive.mjml` | G2-B | +48hr | Ankle deep dive, reasons-why | m1-1.jpg |
| `g3-lastchance.mjml` | G3 | +96hr | Last chance + objections | m1-3.jpg |

**Note:** `email-1-alert.mjml`, `email-2-nudge.mjml`, `email-3-lastchance.mjml` are older 3-email versions — superseded by the 11-email system above.

**To use in Klaviyo:**
1. Open any `.mjml` file → copy code
2. Go to [mjml.io/try-it-live](https://mjml.io/try-it-live) → paste → copy HTML output
3. In Klaviyo: New Template → HTML editor → paste HTML
4. Replace `[ADD_PRODUCT_IMAGE_URL]` with Shopify CDN image URL
5. In G2-A: replace all 4 image placeholders (`[ADD_BOOT_IMAGE_URL]` etc.)
6. In G3: replace `[WAITLIST_FORM_URL]` with waitlist form link
7. Preview + test before activating

---

## Inspiration System

### Folder
`/Users/sujalgurung/email skills/emails inspiration/`

### File Naming Convention
```
YYYY-MM-DD-[brand]-[campaign-type]-email.html
YYYY-MM-DD-[brand]-[campaign-type]-email.png   ← screenshot (optional)

Examples:
2026-04-15-patagonia-back-in-stock-email.html
2026-04-15-patagonia-back-in-stock-email.png
2025-09-04-true-botanicals-back-in-stock-email.html
```

### How to Save Inspiration (user workflow)
1. Find email on milled.com or Email Love gallery
2. **Download HTML** → save to `/emails inspiration/` with naming above
3. **Screenshot** → save as `.png` in same folder OR paste into Figma inspiration page
4. Both is best: HTML = code structure for Claude, screenshot = visual for Figma

### What Claude Does With Inspiration Files
When asked to create an email:
1. Reads all HTML files in `/emails inspiration/` relevant to the campaign type
2. Extracts: layout patterns, colour approaches, section ordering, copy angles, CTA styles
3. Uses those as creative input — NOT direct copies — remixed through Summit Socks brand lens
4. Produces a UNIQUE design concept each time

### Current Inspiration Files
| File | Brand | Type | Key Patterns Noted |
|---|---|---|---|
| `2025-09-04-email-inspiration-from-true-botanicals-103-email.html` | True Botanicals | Back in Stock | Cream bg (#fbfaf6), image-block based, Email Love CDN, Klaviyo kl-section format |

---

## Full Workflow: Inspiration → Figma → Klaviyo

```
GATHER INSPIRATION
User finds email on milled.com / Email Love gallery
  → Download HTML → save to /emails inspiration/YYYY-MM-DD-brand-type.html
  → Screenshot → paste into Figma inspiration page
                 OR save as /emails inspiration/YYYY-MM-DD-brand-type.png

CREATE EMAIL (Claude)
Claude reads inspiration HTML files
  → Extracts layout/colour/copy patterns
  → Generates UNIQUE creative concept for Summit Socks
  → Writes MJML code with full copy OR reviews Figma design

BUILD IN FIGMA (user, optional)
User builds design in Figma using Email Love components
  → [With MCP active] Claude reads frames → gives copy/layout feedback
  → Email Love plugin exports → production Klaviyo HTML (kl-section format)
                 OR
User compiles Claude's MJML at mjml.io → pastes HTML into Klaviyo

KLAVIYO
Set subject line + preview text
Set flow filters (suppress purchasers)
Preview on desktop + mobile
Activate
```

---

## What's Working / What's Not

### Working
- 3-email BIS sequence (immediate → +12-24hr → +48-72hr)
- Email 1: Image-led, minimal copy — let product sell itself
- Email 2: Real review language in quotes (not marketing speak)
- Email 3: Honest "not here to pressure you" opener — reduces unsubscribes
- P.S. lines for urgency — highest-read spot in any email
- Bundle pricing front-and-centre ($50/pair vs $74.99 single)
- Dual CTA in Email 3: buy OR notify me next time
- MJML format — clean, compilable, responsive by default

### Not Working / Avoid
- Multiple products per BIS email — dilutes urgency
- Discount in Email 1 — trains customers to wait before buying
- "Compression" or "snug fit" copy — confirmed customer complaint
- Generic CTAs: "Buy Now", "Shop", "Click Here"
- Fake urgency — Summit's real scarcity (sold out 4x) is the asset

---

## Session Log

**Apr 15, 2026 — Session 1**
- Project initialized
- Model changed: Sonnet → Opus 4.6
- Brand context loaded: Summit Socks full context
- Figured out tool stack: Email Love (Figma → HTML), Klaviyo ESP, MJML for code

**Apr 15, 2026 — Session 2**
- Figma MCP configured: settings.json sources token from .env via bash wrapper
- Token in .env currently INVALID — user needs to regenerate at Figma settings
- Figma file key confirmed: `wNmDJC0ZdTyr0Ar0DPIJpt`
- 3 MJML email files created for Boot Socks BIS campaign
- Subject lines + preview text documented in campaign README
- Inspiration system established: HTML + PNG naming convention in /emails inspiration/
- Creative rule locked in: every email must have unique layout/colour/copy approach
- Email Love export format confirmed: Klaviyo kl-section HTML (not raw MJML)

**Apr 15, 2026 — Session 3**
- Model switched to claude-opus-4-6
- Campaign strategy file created: `campaigns/back-in-stock/campaign-strategy.md`
- All 11 MJML email files built (W1-A, W1-B, W1-C, W2-A, W2-B, G1-A, G1-B, G1-C, G2-A, G2-B, G3)
- Each email has unique layout, colour approach, copy angle — no two are the same
- CLAUDE.md updated to reflect full 11-email system

**Pending**
- Figma MCP token confirmed valid — MCP ready to use
- User to add product images to MJML files (replace `[ADD_PRODUCT_IMAGE_URL]`)
- G2-A needs 4 image URLs: `[ADD_BOOT_IMAGE_URL]`, `[ADD_ANKLE_IMAGE_URL]`, `[ADD_CREW_IMAGE_URL]`, `[ADD_NOSHOW_IMAGE_URL]`
- G3 needs `[WAITLIST_FORM_URL]` (Klaviyo or Shopify waitlist form)
- User to compile MJML → HTML (mjml.io) → load into Klaviyo
- Set up two-branch Klaviyo flow (Waitlist vs General — see campaign-strategy.md)
