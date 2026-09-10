# D2C Insider AI Bootcamp

The student repo. Clone it, open it in the Claude Code desktop app, and work through the sessions in order.

By the end you have ten AI teammates operating on your brand, your data and your competitors, plus a 90 day plan for what they do next.

**Start here:** [`student-handbook.md`](student-handbook.md), then [`session-0-setup.md`](session-0-setup.md).

---

## What is different about this version

Earlier cohorts ran this in a terminal. This one runs in the **Claude Code desktop app**, the Mac and Windows application. No command line, no npm, no PATH problems. You install an app, point it at a folder, and type in a chat box.

Everything else is the same shape: skills, subagents, connectors, scheduled runs. You just see them instead of typing them.

## Layout

```
d2c-insider-ai-bootcamp/
├── student-handbook.md              the master map, read this first
├── session-0-setup.md ... session-12-telegram.md
├── CLAUDE.template.md               the file Session 1 fills in
├── resources.md                     what to add after the bootcamp
├── templates/
│   └── brand-brain/                 copy this to brand-brain/ and fill it
├── .claude/
│   ├── skills/                      13 teammates, auto-loaded
│   └── agents/                      4 subagents
├── references/                      deep dives, one folder per session
└── examples/
    └── the-paan-legacy/             one brand, fully worked, all 10 teammates
```

Two folders get created as you work and are **never committed**: `brand-brain/`, your inputs, and `my-work/`, your teammates' output. Your business data stays on your machine.

## The roster

| # | Teammate | Primitive | Session | Owns |
|---|---|---|---|---|
| 01 | Brand Brain | `/interview-me` or `/brand-brain` skill, writes `CLAUDE.md` | 1 | Brand DNA, voice rules, compliance |
| 02 | Market Analyst | `/market-analyst` skill | 2 | Competitor intel, pricing, cadence |
| 03 | Voice of Customer | `/voice-of-customer` skill | 2 and 3 | Themes, sentiment, persona cards |
| 04 | Content Lead | `content-lead` subagent | 4 | 30 day calendar, pieces, listings |
| 05 | Performance Marketer | `performance-marketer` subagent + `/creative-brief` | 6 | Ad angles, variants, briefs |
| 06 | Storefront Specialist | `/pdp-writer` skill | 7 | PDPs, landing pages, CRO |
| 07 | Marketplace Editor | `/marketplace-editor` skill | 7 | Amazon A+, Flipkart listings |
| 08 | Ops Manager | `/ops-manager` skill | 8 | SOPs, vendor kit, returns |
| 09 | Retention Manager | `/retention-manager` skill | 8 | WhatsApp and email flows, segments |
| 10 | Growth Analyst | `/growth-analyst` skill | 9 | Weekly brief, unit economics, dashboard |
| — | The Captain | `captain` subagent | 10 | Cross teammate synthesis, 90 day roadmap |

Add-ons: `/influencer-scout` (Session 11), the Telegram bot (Session 12), `/fal-image-gen` and the `image-ad-strategist` agent for real image generation.

## Two rules baked into every session

**Index files, not raw outputs.** Every teammate writes a short index. The Captain reads only indexes, never raw work. That is what lets one agent sit across ten teammates without running out of room.

**Default and Power scope.** Every skill asks you to pick at the start. Default fits a Pro plan and the session slot. Power is for Max or take home. Same lesson either way.

## The worked example

`examples/the-paan-legacy/` is one gourmet paan brand taken through all ten teammates: filled `CLAUDE.md`, the `brand-brain/` inputs behind it, and 40-plus real outputs in `my-work/`. When a session's instructions are clear but you cannot picture the output, open the matching folder there.

## Requirements

- A Claude **Pro or Max** plan. Claude Code does not run on the free tier.
- The **Claude Code desktop app** for Mac or Windows.
- **Git** installed, or the ability to download a ZIP from GitHub.
- Your own brand data. The more of `templates/brand-brain/` you fill before Session 1, the better every later session gets.
