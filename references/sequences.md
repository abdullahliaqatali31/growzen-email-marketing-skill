# Follow-up Sequences

Reference for designing multi-step outreach cadences. Read this when the user wants a sequence, not a single email.

## Why sequences win

Most replies come from follow-ups, not the first email. A single send leaves the majority of your pipeline on the table. But each step must add something new. Repeating "just bumping this up" trains people to ignore you.

## Default structure

A solid B2B cold sequence is **3 to 5 steps** over ~2-3 weeks. Do not go past a polite few touches without a reason.

| Step | Day | Job | Angle |
|---|---|---|---|
| 1 | 0 | Introduce the problem + one CTA | Hook + relevance (see frameworks.md) |
| 2 | 2-3 | New angle, same thread | Proof, a specific result, or a case |
| 3 | 5-6 | Different value or a question | Reframe the offer, or ask a one-line question |
| 4 (optional) | 9-10 | Social proof / resource | Share something useful, low ask |
| 5 | 12-14 | Breakup | "Should I close this out?" Short, no pressure |

Rules:
- **Space steps 2-4 days apart**, not daily. Daily follow-ups read as desperate and hurt deliverability.
- **Later steps reply in the same thread** (blank subject) so it reads as a continuation.
- **Each step earns its place.** New angle, new proof, or a genuine question. Never "just following up" with nothing added.
- **The breakup works.** A short "want me to close this out?" often gets the reply the pitch did not, because it is easy to answer and creates mild loss aversion.

## Follow-up angles (pick different ones per step)

- **Proof:** a specific result for a similar company. Numbers beat adjectives.
- **The one-line question:** "Are you the right person for [outcome], or should I talk to someone else?"
- **New value:** a different benefit than step 1, in case the first did not land.
- **Resource:** share a genuinely useful link/tip with no ask. Builds goodwill.
- **Breakup:** permission to stop. Short and warm.

## Timing and safety

- **Stop on reply.** The moment someone replies, all pending follow-ups for that person must stop. (GrowZen does this automatically; other tools need it configured.)
- **Stop on unsubscribe and bounce** too.
- Keep total daily volume per inbox within safe warmup-aware limits (see deliverability.md). A sequence multiplies volume, so plan the ramp.

## Personalization across a sequence

- Personalize the first email hardest (it decides whether they read the rest).
- Keep merge fields to ones the list has, with fallbacks, on every step (a broken variable on step 3 is just as damaging as on step 1).
- In GrowZen mode, check `growzen_lead_list_fields` once and design all steps around the fields that exist.

## Sequence anti-patterns

- 7+ aggressive follow-ups. You are not persistent, you are spam.
- Identical "bump" emails with no new content.
- Sending all steps from one cold inbox at high volume (rotate and warm up).
- Follow-ups that ignore a reply because stop-on-reply was not set.
