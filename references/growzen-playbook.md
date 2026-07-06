# GrowZen Playbook (MCP-connected mode)

Read this only when the GrowZen MCP server is connected (you can see tools named `growzen_*`). It maps common requests to the exact tool sequence. If the tools are not available, do not follow this file. Instead deliver the work as copy and tell the user how to connect GrowZen.

## Golden rules in GrowZen mode

- **Drafts never send.** `growzen_campaign_create_draft` creates a draft the user reviews and launches in GrowZen. Never tell the user an email was sent. Say it is drafted and give them the review step.
- **Confirm before acting.** For anything that writes (import leads, draft a campaign), state the plan and get a yes first. Read tools are safe to use freely.
- **Ground copy in real fields.** Always check what the audience actually has before writing merge variables.

## Available tools (reference)

Read: `growzen_campaigns_list`, `growzen_campaigns_analytics`, `growzen_campaign_get`, `growzen_leads_availability`, `growzen_leads_list`, `growzen_lead_list_fields`, `growzen_templates_list`, `growzen_inbox_summary`, `growzen_inbox_search`, `growzen_accounts_list`, `growzen_usage_get`.

Write (additive, never sends): `growzen_leads_import`, `growzen_lead_create`, `growzen_lead_list_create`, `growzen_leads_copy_segment`, `growzen_template_create`, `growzen_campaign_create_draft`, `growzen_draft_reply`.

## Playbook: "I have leads from Apollo/Apify/a spreadsheet, build me a campaign"

1. **Import.** Call `growzen_leads_import` with the leads (up to 500 per call; repeat for more). Put any extra columns in `metadata` so they become personalization fields. Pass a `source` label (e.g. "apollo"). This adds them to a list AND the unified cloud lead pool.
2. **Check field coverage.** Call `growzen_lead_list_fields` on the new list. Note which fields exist and their coverage percentage. Only write merge variables for fields present, and plan fallbacks for anything under ~80%.
3. **Pick the content approach.** Ask the user: reuse their best-performing templates, or have you write fresh copy? For proven copy, call `growzen_templates_list` with `sort=performance`. For fresh copy, write it grounded in their business and the fields from step 2.
4. **Draft the campaign.** Call `growzen_campaign_create_draft` with the target list, the sequence steps (each with a `day` offset plus either a `templateId` or inline `subject`+`body`), and a `placeholderFallbacks` map for every variable you used except firstName.
5. **Hand off.** Tell the user it is drafted (not sent) and give them the review link to launch it in GrowZen.

## Playbook: "Follow up with everyone who opened but didn't reply"

1. Call `growzen_leads_copy_segment` with `segment: "opened"` and a `targetListName` (e.g. "Opened, no reply") to build the audience. It creates the list and returns `targetLeadListId`.
2. If it returns `copied: 0`, stop and tell the user nothing matched. Do not draft on an empty list.
3. Otherwise write a fresh follow-up angle (see sequences.md) and draft it against that list with `growzen_campaign_create_draft`.

## Playbook: "How are my campaigns doing / what should I fix?"

1. `growzen_campaigns_analytics` for the aggregate picture and best/worst performers.
2. `growzen_campaign_get` for a specific campaign's sequence and stats.
3. `growzen_templates_list` with `sort=performance` to see which copy actually works.
4. Diagnose with deliverability.md and the copy rules. Recommend concrete changes, then offer to draft the improved version.

## Playbook: "Help me handle my replies"

1. `growzen_inbox_summary` for unread counts, sentiment breakdown, and hot leads.
2. `growzen_inbox_search` to find specific threads.
3. `growzen_draft_reply` to compose a suggested reply (draft only; the user sends it). Match their tone; be concise and move the conversation toward the next step.

## When the audience or content is missing

- No leads yet: the user scrapes/imports first. You can import for them (step 1 above) or point them to the leads page.
- No SMTP account connected: a draft can still be created, but they need a sender before launching. Mention it.
- Empty or tiny list: say so; do not draft a campaign onto nothing.
