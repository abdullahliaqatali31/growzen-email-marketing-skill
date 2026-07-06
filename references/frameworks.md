# Cold Email Copy Frameworks

Reference for writing individual cold emails that get replies. Read this when writing or critiquing a single email.

## The anatomy of an email that gets a reply

1. **Subject**: see `subject-lines.md`. Short, specific, no clickbait.
2. **First line (the hook)**: must be about THEM, not you. Reference something real: their role, company, a trigger event, a problem their segment has. Never open with "I hope this finds you well" or "I wanted to reach out."
3. **The relevance**: one or two sentences connecting their situation to the problem you solve. Show you understand their world.
4. **The value**: what changes for them. Concrete outcome, not features. "Book 2-3 more demos a week" beats "AI-powered outreach automation."
5. **One CTA**: a single, low-friction ask. "Worth a quick 15 minutes next week?" or "Want me to send a 2-minute video?" Never stack two asks.
6. **Signature**: real name, real company, real physical address (CAN-SPAM), and a working unsubscribe.

Total length: **80-120 words** for the first email. Shorter usually wins.

## Proven frameworks

Pick the one that fits the situation. Do not force all of them into one email.

### PAS (Problem, Agitate, Solve)
- **Problem:** name the pain the segment feels.
- **Agitate:** one line on what it costs them to leave it.
- **Solve:** how you fix it, in one line, plus the CTA.
Best for painful, expensive problems the reader already knows they have.

### BAB (Before, After, Bridge)
- **Before:** their current state.
- **After:** the better state.
- **Bridge:** how you get them there.
Best when the outcome is aspirational and easy to picture.

### AIDA (Attention, Interest, Desire, Action)
Classic. Attention (hook) -> Interest (relevance) -> Desire (outcome) -> Action (CTA). A safe default.

### The "observation" opener
Lead with a specific, true observation about them ("Saw your team just opened a second office in Austin"). Then connect it to the problem. High reply rates because it proves you did homework. Only works with real data.

## ICP: define it before writing

Never write to an unknown reader. You need:
- **Who**: role/title, company size, industry.
- **Their trigger**: what makes now the right time (hiring, funding, a new tool, a season, a pain).
- **The one outcome**: the single result they buy.
- **Their objection**: what makes them hesitate, so you can pre-empt it.

If the user has not given you these, ask two quick questions before writing: (1) who is this for, and (2) what is the one outcome you sell them.

## Value proposition rules

- Sell the outcome, not the mechanism. "Fewer bounced emails" not "4-layer verification."
- Be specific and quantified where honest. "Cut your bounce rate under 2%" beats "improve deliverability."
- One value per email. If you have three, that is three emails in a sequence, not one paragraph.

## Personalization tiers

1. **Basic:** first name, company. Table stakes. Do not stop here.
2. **Segment:** copy written for their role/industry so it feels 1:1 even when scaled.
3. **1:1 signal:** a real observation (trigger event, recent post, a detail from their site). Highest reply rate, lowest scale. Reserve for high-value targets.

Only use merge variables the list actually has, and always set fallback text so a missing field never produces "Hi ," or "at ." When connected to GrowZen, check coverage with `growzen_lead_list_fields` first.

## What kills replies (avoid)

- Talking about yourself in the first line.
- More than one CTA.
- Feature lists and jargon.
- Fake personalization ("I love what you're doing at {{company}}").
- Walls of text and multi-paragraph pitches.
- Writing that reads as AI-generated (see the anti-AI rules below).

## Do not write like AI

The fastest way to get ignored (and flagged) is copy that reads as machine-written. Avoid:
- The em dash. Use a period, comma, or colon instead.
- Words like: elevate, seamless, unlock, leverage, robust, in today's fast-paced world, I wanted to reach out, I hope this email finds you well, delve, tapestry, testament.
- Perfectly balanced "not only X but also Y" constructions on every line.
- Overly formal transitions.

Write short. Write like a specific human who knows the reader. Contractions are fine. One good sentence beats three padded ones.
