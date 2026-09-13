# MrMortgageMan API — System Architecture

> AI-powered infrastructure for mortgage lending, lead generation, and real estate content automation.

***

## What This Org Does

This GitHub organization houses the backend systems, AI skill libraries, and web applications that power the **MrMortgageMan** brand ecosystem. Everything here connects to a broader automation stack built around HubSpot, Zapier, Notion, and Claude AI.

***

## Repositories

| Repo | Visibility | Purpose | Status |
|---|---|---|---|
| [mrmortgageman-skills](https://github.com/mrmortgageman-api/mrmortgageman-skills) | Private | Claude AI skill files for content, email, and RevOps | 🟢 Live |
| [scenario-engine-calculators](https://github.com/mrmortgageman-api/scenario-engine-calculators) | Private | Authoritative deterministic calculator services for the Scenario Engine (purchase payment, refinance break-even, and related mortgage math). Contracts and known-answer specs are versioned in `skill-library/scenario-engine-prompts`; deployed separately from the TCA presentation app. | 🟡 Building |
| [mortgage-scenario-engine](https://github.com/mrmortgageman-api/mortgage-scenario-engine) | Private | WOW Calculator API — early 3-scenario lead-magnet calculator. Not redeployed since 2026-03-13. Confirmed **not** the calculator the Scenario Engine kernel/router reference — do not treat as authoritative. Superseded by `scenario-engine-calculators`. | 🔴 Deprecated |
| [nextjs-boilerplate](https://github.com/mrmortgageman-api/nextjs-boilerplate) | Private | Active Next.js application (48 Vercel deployments) — hosts the TCA export/presentation tool | 🟢 Live |
| [skill-library](https://github.com/mrmortgageman-api/skill-library) | Public | Defensive Midfield operator skills for AI agents; also the canonical source for the Scenario Engine kernel and knowledge docs (`scenario-engine-prompts/`) | 🟢 Live |

***

## System Architecture

```
MrMortgageMan AI Ecosystem
│
├── Content & Marketing Layer
│   └── mrmortgageman-skills (Claude skill files)
│       ├── Phase 1: cold-email, copywriting, email-sequence
│       └── Phase 2: SEO, video scripts, social (planned)
│
├── Product Layer
│   ├── nextjs-boilerplate (web application — TCA presentation/export)
│   ├── scenario-engine-calculators (authoritative calculator API — building)
│   └── mortgage-scenario-engine (deprecated — superseded by scenario-engine-calculators)
│
├── Governance Layer
│   └── skill-library/scenario-engine-prompts (Scenario Engine kernel, knowledge docs,
│       calculator contracts — canonical source; Claude Project and Griff GPT are
│       manually-synced deployment mirrors of this repo)
│
├── Automation Layer (external)
│   ├── HubSpot CRM
│   ├── Zapier workflows
│   └── Notion Control Tower
│
└── AI Agent Layer (external)
    ├── Claude Code (uses skill files from this org)
    ├── SignalStrike (lead intelligence)
    └── Buyer Supply Engine
```

***

## Tech Stack

- **Frontend:** Next.js, Vercel
- **API:** Node.js (`scenario-engine-calculators` — authoritative; `mortgage-scenario-engine` deprecated, do not build against it)
- **AI:** Claude Code, Claude API
- **CRM:** HubSpot
- **Automation:** Zapier
- **Docs:** Notion

***

## Contact

**Scott Thompson** — Loan Officer & System Architect
🌐 [mrmortgageman.com](https://mrmortgageman.com)

***

*This organization is part of the MrMortgageMan brand. Not all repos are public.*
