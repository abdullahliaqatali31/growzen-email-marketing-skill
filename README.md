# GrowZen Email Marketing Specialist (Claude Agent Skill)

An Agent Skill that turns Claude into an expert cold-email and outreach strategist. It works with **any** sending stack, and becomes an autonomous email marketer when you also connect the **GrowZen MCP server** (import leads, draft campaigns, and triage replies right in your GrowZen account).

- Copywriting frameworks, subject-line testing, and sequence design
- Deliverability and compliance (warmup, SPF/DKIM/DMARC, CAN-SPAM, GDPR, CASL)
- Anti-"AI-sounding" copy rules so your emails read human
- GrowZen-connected playbooks for lead import, grounded drafting, and inbox triage

Full guide and setup: **https://growzen.app/skill**

## What's inside

```
growzen-email-marketing-skill/
├── SKILL.md                        # main skill: methodology + dual-mode logic
└── references/
    ├── frameworks.md               # cold email copy frameworks + ICP
    ├── subject-lines.md            # subject patterns + testing
    ├── sequences.md                # multi-step cadence design
    ├── deliverability.md           # inboxing + legal compliance
    └── growzen-playbook.md         # GrowZen MCP tool workflows
```

## Install

### Claude Code
```bash
/plugin marketplace add abdullahliaqatali31/growzen-email-marketing-skill
/plugin install growzen-email-marketing@growzen
```
Or drop this folder into `~/.claude/skills/growzen-email-marketing/` (personal) or `.claude/skills/` (project).

### Claude.ai (web / desktop)
Download this folder as a `.zip` and upload it under **Settings -> Features -> Skills**.

### Claude Agent SDK
Include the skill directory in your agent's skills configuration.

## Best paired with the GrowZen MCP

Connect Claude to your GrowZen account so the skill can act, not just advise:
- Server URL: `https://api.growzen.app/mcp`
- Create an API key at **app.growzen.app -> Dashboard -> API & MCP**

Learn more: https://growzen.app/mcp · https://growzen.app/integrations

## License

Free to use. The skill is provided by GrowZen (https://growzen.app). Contributions and issues welcome.
