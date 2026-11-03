

# Mason Equity Second Brain

The second brain is a Markdown vault that provides reusable context and ongoing memory for Mason Equity AI agents.

A Handoff skill generates session summaries and saves them in the vault. Future agents use these summaries to quickly resume prior tasks, with the decisions, progress, and next steps already captured.

Context is organized by workstream. Dataview uses note metadata to group related notes in workstream hubs, while links connect relevant context.

The vault stores:

- Financial reporting documentation.
- Syndication documentation and investor materials.
- Social media content, drafts, and generation workflows.
- Skill files and reusable agent instructions.
- Programming project documentation and session handoffs.

## Directory structure

```text
MEP Vault/
├── 2. Home.md                  Workstream navigation
├── Active/                     Current work, organized by workstream
│   ├── Content/                Social media content and workflows
│   ├── Financial Reporting/    Models and reporting documentation
│   ├── Asset Management/       Property operations
│   ├── Fundraise/              Syndication and investor materials
│   ├── HoldCo/                 Holding Company operations and accounting
│   ├── Programming/            Programming projects and agent tooling
│   └── Personal/               Personal notes and projects
├── Reference/                  Reusable context
│   └── Session Summaries/      Handoffs for future agents
├── Skills/                     Generalized skill references for agent inspiration
├── Claude Config/              Shared procedures, standards, and examples
├── .claude/skills/             Claude skill files
├── .agents/skills/             Agent skill files
├── Inbox/                      Captures awaiting organization
└── Archive/                    Completed or superseded work
```

## Generalized skills

[Browse the generalized skills collection](Skills/README.md) for reusable workflows
organized by workstream:

- **Programming:** Hydrate, folder sorting, Handoff, Markdown validator,
  agent messaging, and dependency monitoring.
- **Content:** article adapter, post promoter, and design evaluation.
- **Financial Reporting:** CFO Agent and Monthly reporting.
- **Personal:** time blocking.

These are generalized references for pointing an agent at for inspiration,
not installation-ready skills. Private names, paths, records, and configuration
have been removed from the collection. Each reference explains the workflow
and what an agent needs to adapt it to another environment.


## Snapshot provenance

Non-authoritative snapshot dated 2026-11-03. Source: `Active/Programming/Second Brain - External Overview.md` in the MEP vault. The source vault is not a Git repository; this snapshot has no source commit revision.


## How this was built

The generalized skill references were prepared with OpenAI Codex assistance. Review and validate adaptations for your environment.
