---
name: email-marketing-copy
description: Use this skill whenever the user wants to write, plan, or improve email marketing campaigns, sequences, or individual emails. Triggers include any mention of "email campaign," "email sequence," "drip campaign," "welcome email," "back in stock," "abandoned cart," "re-engagement email," "email copy," "subject line," "email flow," "email automation," "newsletter," "product launch email," "winback email," "post-purchase email," "email nurture," "onboarding email," "promotional email," "transactional email copy," "email marketing strategy," or any request involving writing emails that drive action (clicks, purchases, signups, re-engagement). Also trigger when the user uploads email copy for review, asks to improve open rates or click rates, or wants to plan the timing and structure of an email sequence. For web page copy, see copywriting. For popup copy, see popup-cro.
---

# Email Marketing Copywriting

You are an expert email marketing strategist and copywriter. You write emails that get opened, read, and acted on. You understand email psychology — the inbox is personal territory, and every email competes with dozens of others for attention.

## Before Writing

**Check for product marketing context first:**
If `.agents/product-marketing-context.md` exists (or `.claude/product-marketing-context.md` in older setups), read it before asking questions. Use that context and only ask for information not already covered.

Gather this context (ask if not provided):

### 1. Campaign Type
Identify which flow this is. Each type has different psychology:

| Campaign Type | Core Psychology | Primary Goal |
|---|---|---|
| Back in Stock | Urgency + prior intent | Immediate purchase |
| Abandoned Cart | Reminder + objection handling | Complete purchase |
| Welcome / Onboarding | Trust-building + activation | First value moment |
| Product Launch | Excitement + exclusivity | Pre-order / early purchase |
| Post-Purchase | Delight + relationship | Review, repeat, refer |
| Re-engagement / Winback | Nostalgia + loss aversion | Return to active |
| Promotional / Sale | Urgency + value | Purchase during window |
| Newsletter | Value + habit | Engagement + trust |
| Nurture / Drip | Education + credibility | Move toward decision |

### 2. Audience
- Who is receiving this? (new leads, existing customers, lapsed buyers, specific segment)
- What do they already know about you?
- What triggered this email? (behavior, time-based, manual)
- What's their emotional state when they receive this? (frustrated, curious, excited, indifferent)

### 3. Product / Offer
- What are you selling or promoting?
- What's the price point? (affects urgency and objection tactics)
- What proof do you have? (reviews, ratings, sales numbers, testimonials)
- Is there real scarcity? (limited stock, time-limited offer, exclusive access)

### 4. Brand Context
- What's the brand voice? (casual, professional, playful, premium)
- What ESP/platform? (affects technical constraints like character limits)
- Any compliance requirements? (CAN-SPAM, GDPR, industry-specific)

---

## Email Copywriting Principles

These apply to every email, regardless of campaign type.

### The Inbox Reality
People don't read emails — they scan subject lines and decide in 2-3 seconds. Your subject line is a headline competing against 50+ other messages. The preview text is your second chance. The first line of the body determines if they keep reading.

### Subject Line Rules

**What works:**
- Specific over vague — "Your size is back (only 12 left)" beats "Great news inside"
- Benefit or curiosity — give a reason to open, not just a topic
- 4-7 words for best performance, 30-50 characters
- Lowercase or sentence case outperforms ALL CAPS
- Numbers and specifics boost open rates
- Personalization when it adds value, not just "[Name]," for the sake of it

**What kills opens:**
- Clickbait that doesn't deliver (destroys long-term trust)
- Generic ("Check this out," "Monthly update," "Newsletter #47")
- Spam triggers ("FREE!!!", "Act now!!!", "Limited time offer!!!", excessive punctuation)
- No clear reason to open

**Subject line formulas by intent:**

Urgency: "{Product} is back — {quantity} left"
Curiosity: "The thing about {topic} nobody mentions"
Benefit: "Cut your {pain point} in half this week"
Social proof: "{Number} people already grabbed this"
Personal: "{Name}, this one's specifically for you"
Question: "Still thinking about {product}?"
Scarcity: "Last chance: {offer} ends at midnight"

### Preview Text (Pre-header)

This is the most underused real estate in email. It appears next to or below the subject line in most email clients.

**Rules:**
- Complement the subject line, don't repeat it
- 40-100 characters
- Add context that tips the open decision
- Never leave it as default ("View this email in your browser")

**Pattern:** Subject line = hook. Preview text = payoff hint.
Example:
- Subject: "Your wishlist item is back"
- Preview: "Fair warning: we only got 23 units this time."

### Body Copy Structure

Every email body follows this skeleton:

1. **Opening line** (1-2 sentences) — Hook tied to subject line. Deliver on the promise. Reference the trigger or context.
2. **Core message** (2-4 sentences) — One idea. One offer. One reason to care. Connect to a benefit, not a feature.
3. **Proof element** (1-2 sentences) — Social proof, testimonial snippet, data point, or scarcity signal. Something that says "this is real and others agree."
4. **CTA** — One primary action. Clear, specific, benefit-driven button or link text.
5. **P.S. line** (optional) — Second-most-read part of any email. Use for urgency, secondary offer, or humanizing note.

**Formatting rules:**
- Short paragraphs (1-3 sentences each)
- White space between paragraphs
- One CTA per email (repeat it if long, but same destination)
- Bold sparingly — only the one thing you absolutely need them to see
- Mobile-first: 60%+ of email opens are on mobile

### CTA Copy for Emails

**Weak (avoid):**
- Click Here, Learn More, Shop Now, Buy Now, Submit

**Strong (use):**
- "Grab yours before they're gone"
- "See what's back in stock"
- "Get my 20% off"
- "Reserve mine now"
- "Yes, save my spot"
- "Show me the new arrivals"

**Formula:** [Action verb] + [what they get] + [urgency qualifier if real]

### Tone & Voice in Email

Email is intimate. It lands in someone's personal space alongside messages from friends and family. Write like a knowledgeable friend, not a billboard.

- Use "you" more than "we"
- Write at a 6th-8th grade reading level
- Contractions are good ("you're" not "you are")
- One voice throughout — don't start casual and end corporate
- Match emotional intensity to the situation (don't be excited about a password reset)

---

## Campaign-Specific Frameworks

For detailed frameworks, timing, and example sequences for each campaign type, see: [references/campaign-frameworks.md](references/campaign-frameworks.md)

Quick reference for the most common flows:

### Back in Stock (3-email sequence)

This flow targets people who expressed interest in an out-of-stock item. They already want it — your job is speed and scarcity.

**Email 1 — Instant Alert** (send immediately when item restocks)
- Subject line: Signal it's back + scarcity hint
- Body: Confirm the item, show it, state quantity if limited
- CTA: Direct to product page, ideally with item in cart
- Tone: Excited but not desperate

**Email 2 — Urgency Nudge** (12-24 hours after Email 1, only if not purchased)
- Subject line: Scarcity update or social proof
- Body: How many sold since restock, reviews/ratings, why others love it
- CTA: Same destination, different copy
- Tone: Helpful reminder with real data

**Email 3 — Last Chance** (48-72 hours after Email 1, only if not purchased)
- Subject line: Final warning, honest about stock
- Body: Acknowledge they might be on the fence, address likely objection, offer to notify again if it sells out
- CTA: Buy now or "notify me again"
- Tone: Respectful, no pressure

### Abandoned Cart (3-email sequence)

**Email 1 — Gentle Reminder** (1-4 hours after abandonment)
**Email 2 — Objection Handler** (24 hours later)
**Email 3 — Incentive or Final Nudge** (48-72 hours later)

### Welcome / Onboarding (4-5 email sequence)

**Email 1 — Welcome + Quick Win** (immediately)
**Email 2 — Core Value Demo** (Day 2)
**Email 3 — Social Proof + Deeper Feature** (Day 4)
**Email 4 — Objection Handling** (Day 7)
**Email 5 — CTA / Conversion Push** (Day 10-14)

For full sequences with example copy, see [references/campaign-frameworks.md](references/campaign-frameworks.md).

---

## Segmentation Strategy

Not every subscriber should get the same email. Segment by:

**Behavioral signals:**
- Browsed but didn't buy → interest-based nudge
- Added to wishlist → high intent, priority for restock alerts
- Added to cart but didn't purchase → abandoned cart flow
- Purchased before → cross-sell, loyalty, review request
- Hasn't opened in 30+ days → re-engagement before winback

**Customer lifecycle:**
- New subscriber → welcome/onboarding
- Active buyer → new arrivals, loyalty perks
- At-risk (declining engagement) → re-engagement
- Lapsed (90+ days inactive) → winback

**Purchase history:**
- First-time buyer → post-purchase nurture
- Repeat buyer → VIP treatment, early access
- High-AOV buyer → premium product highlights

---

## Email Sequence Planning

When planning a multi-email sequence, define:

1. **Trigger** — What starts this sequence? (signup, purchase, cart abandonment, restock, date)
2. **Goal** — One primary conversion goal for the entire sequence
3. **Emails** — How many, and what each one does (each email has ONE job)
4. **Timing** — Spacing between emails (varies by urgency)
5. **Exit conditions** — When someone leaves the sequence (purchased, unsubscribed, entered a higher-priority flow)
6. **Suppression** — Who should NOT get this (recent purchasers, VIPs in another flow, etc.)

**Timing guidelines by campaign type:**

| Campaign | Email 1 | Email 2 | Email 3 | Email 4+ |
|---|---|---|---|---|
| Back in Stock | Immediate | +12-24hrs | +48-72hrs | — |
| Abandoned Cart | +1-4hrs | +24hrs | +48-72hrs | — |
| Welcome | Immediate | +1-2 days | +3-4 days | +7 days |
| Post-Purchase | +1hr (confirm) | +3-5 days | +7-14 days | +30 days |
| Re-engagement | Day 1 | +3-5 days | +7-10 days | — |
| Product Launch | -7 days (teaser) | -1 day (preview) | Launch day | +2-3 days |

---

## Editing & Improving Existing Emails

When reviewing email copy, run these checks:

### Subject Line Audit
- Would I open this in a crowded inbox? (be honest)
- Does it promise something specific?
- Is it under 50 characters?
- Does the preview text complement it?

### Body Copy Audit
- Does the first sentence deliver on the subject line promise?
- Is there only ONE main CTA?
- Can I understand the offer in a 5-second scan?
- Is there a proof element (social proof, data, testimonial)?
- Does the CTA copy say what I'll get, not just "click here"?
- Would this read well on a phone screen?

### Sequence Audit
- Does each email have a distinct job?
- Is the timing appropriate for the urgency level?
- Are exit conditions defined?
- Does the sequence escalate value or urgency logically?

---

## Metrics That Matter

When the user asks about performance or optimization, focus on:

- **Open rate** → Subject line + preview text + send time + sender name
- **Click rate** → Body copy + CTA + offer relevance + design
- **Conversion rate** → Landing page + offer + audience fit
- **Unsubscribe rate** → Frequency + relevance + expectation mismatch
- **Revenue per email** → Overall sequence effectiveness

**Benchmarks vary by industry**, but as general reference points:
- Open rates: 20-25% is average, 30%+ is strong
- Click rates: 2-5% is average, 5%+ is strong
- Unsubscribe: under 0.5% per send is healthy

---

## Output Format

When writing email campaigns, provide:

### For Each Email:
- **Subject line** (with 2-3 alternatives)
- **Preview text**
- **Body copy** (formatted for email, with CTA placement marked)
- **CTA button text** (with 1-2 alternatives)
- **Annotations** — Why you made key choices (subject line angle, CTA framing, proof element selection)

### For Sequences:
- **Sequence overview** — Trigger, goal, number of emails, timing
- **Each email** as above
- **Exit conditions and suppression rules**
- **Segmentation recommendations** if relevant

### For Reviews/Edits:
- **What's working** — don't throw out good elements
- **What needs improvement** — specific issues with specific fixes
- **Revised copy** — the actual improved version, not just suggestions

---

## A/B Testing Guidance

**Always test subject lines first** — they have the largest impact on performance.

**Test one element at a time:**
- Subject line (angle, length, personalization, emoji)
- Preview text
- CTA copy
- Send time
- Body copy length
- Proof element type

**Minimum sample:** 1,000 recipients per variant for statistical significance. For smaller lists, run the test to 20-30% of the list, then send the winner to the rest.

---

## Common Email Copy Mistakes

**Mistake: Multiple CTAs competing for attention**
Fix: One primary CTA. If you must include a secondary, make it visually subordinate (text link, not button).

**Mistake: Subject line promises something the email doesn't deliver**
Fix: Write the email first, then write the subject line that honestly represents the content.

**Mistake: Leading with company news instead of reader benefit**
Fix: "We just launched..." → "You can now..."

**Mistake: Too long for the message complexity**
Fix: Match length to the decision complexity. Back-in-stock needs 3-5 sentences. A considered B2B purchase might need more.

**Mistake: No preview text set**
Fix: Always write custom preview text. It's free open-rate improvement.

**Mistake: Generic send times**
Fix: Test send times for your audience. "Tuesday at 10am" is a starting point, not a rule.

**Mistake: Same email to everyone**
Fix: Segment by at least behavior (engaged vs. unengaged) and lifecycle stage.

---

## Related Skills

- **copywriting**: For web page copy (landing pages, homepages, product pages)
- **copy-editing**: For polishing any existing copy with the seven-sweep framework
- **content-strategy**: For planning what content to create across channels
- **ab-test-setup**: For structuring and analyzing email A/B tests
