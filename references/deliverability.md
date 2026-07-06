# Deliverability and Compliance

Reference for landing in the inbox and sending legally. Read this when the user asks about spam, bounces, warmup, or the rules of cold email.

## The deliverability stack (in order)

1. **Domain and DNS.** Use a separate sending domain (not your primary), with SPF, DKIM, and DMARC all set. Missing auth is the fastest route to spam. If the user runs their own mailboxes, confirm all three are configured.
2. **Warmup.** New mailboxes must be warmed before real sending: start low and ramp daily volume over ~2-4 weeks. Sending 500 cold emails from a fresh inbox on day one will burn it. Keep warmup running in the background even after ramp.
3. **Volume discipline.** Respect per-inbox daily limits. Ramp gradually. To scale, add more warmed inboxes and rotate, do not blast one inbox harder.
4. **List quality.** Verify addresses before sending. A high bounce rate (roughly >2-3%) tells providers you are a spammer. Never send to an unverified purchased list without cleaning it first.
5. **Content.** Avoid spam-trigger words, heavy links, big images, and attachments in cold email. Plain, personal, short text lands best. See the anti-AI and copy rules in frameworks.md.
6. **Engagement.** Replies and opens teach the inbox you are wanted; bounces, spam complaints, and unsubscribes teach the opposite. Good targeting and good copy are deliverability tools, not just conversion tools.

## Health thresholds to watch

- **Bounce rate:** keep under ~2-3%. Above that, pause and clean the list.
- **Spam complaint rate:** keep very low (well under 0.1%). Complaints are the most damaging signal.
- **Reply/open trends:** a sudden drop often means a reputation or placement problem, not just bad copy.

If a user reports emails going to spam, check in this order: authentication (SPF/DKIM/DMARC), warmup status, list verification/bounce rate, volume ramp, then content. It is usually one of the first four, not the copy.

## Legal compliance (you are responsible for knowing your recipients)

This is not optional and it protects the sender.

- **United States (CAN-SPAM):** cold B2B email is permitted if you use truthful headers and subject lines, identify the message honestly, include a valid physical postal address, and honor opt-outs within 10 business days. Provide a clear, working unsubscribe.
- **EU / UK (GDPR / PECR):** you generally need consent, or a documented legitimate-interest assessment, to email individuals. B2B has some latitude but the bar is higher than the US. Keep records.
- **Canada (CASL):** requires consent or an existing business relationship. One of the strictest regimes.
- **Everywhere:** honor unsubscribes immediately and permanently, keep a suppression list, and never email anyone who opted out. Do not use harvested or purchased lists without a lawful basis.

You may decline to help with clearly unlawful or deceptive sending (fake identities, misleading subjects, ignoring opt-outs, sending to people who unsubscribed).

## Spam-word awareness

Flag and rewrite when copy leans on: free, guarantee, act now, limited time, risk-free, cash, winner, congratulations, click here, $$$, urgent, and excessive punctuation or ALL CAPS. One or two are survivable; a pile of them plus a fresh domain is a spam-folder recipe.

## Quick pre-send checklist

- [ ] SPF, DKIM, DMARC set on the sending domain
- [ ] Mailbox warmed and within daily limit
- [ ] List verified, bounce risk low
- [ ] One clear CTA, 80-120 words, no spam words
- [ ] Working unsubscribe + physical address (CAN-SPAM)
- [ ] Stop-on-reply / suppression configured
- [ ] Copy does not read as AI-generated
