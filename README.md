# Product Automations

A growing collection of automations I build around problems I encounter in products, operations, and everyday workflows.

The goal is not to automate everything. I use automation where repetitive work can be removed, information can move more clearly, or people can make better decisions with less manual effort.

Each project starts with a problem or workflow first. The implementation comes after.

## Why This Repository Exists

I come from an engineering background and now work closer to product — understanding users, shaping workflows, and thinking about how technology can make those workflows better.

This repository is where I explore that intersection.

Some automations are small utilities built around a single repetitive task. Others may grow into connected systems with multiple workflows, decision points, and human handoffs.

For each published automation, I try to document:

- the problem that made it worth building
- the workflow and decisions behind it
- what should be automated and what should remain human
- the actual implementation

The workflow files are included so the work can be inspected, not just described.

## Automations

### Sprint Summary Generator

Turns scattered sprint updates into a concise view of progress, wins, blockers, risks, and next steps.

**Problem:** Sprint information often lives across tickets and updates, while stakeholders need a clear view of what changed and what needs attention.

**Workflow:** Sprint inputs → structured analysis → stakeholder-ready summary → Slack or email

[Explore the automation →](./sprint-summary-generator)

---

More automations will be added as I build, test, and document them.

## How I Approach Automation

**Problem → Workflow → Decision Points → Automation → Human Handoff**

I am less interested in connecting tools for the sake of it and more interested in understanding where automation genuinely improves a workflow.

That means asking:

- What repetitive work should disappear?
- What context does the system need?
- Where is AI useful, and where is deterministic logic better?
- What decisions still need a person?
- What happens when the workflow fails?

## Repository Structure

```text
product-automations/
├── README.md
│
└── sprint-summary-generator/
    ├── CASE-STUDY.md
    ├── assets/
    │   └── workflow-overview.png
    └── workflow/
        └── sprint-summary-generator.json