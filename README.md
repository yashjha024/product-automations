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

## Automations

### Sprint Summary Generator

Turns scattered sprint updates into a concise view of progress, wins, blockers, risks, and next steps.

**Problem:** Sprint information often lives across tickets and updates, while stakeholders need a clear view of what changed and what needs attention.

**Workflow:** Sprint inputs → structured analysis → stakeholder-ready summary → Slack or email

[Explore the automation →](./sprint-summary-generator)

---

### PRD Copilot

Turns raw product context into a structured PRD draft while keeping missing information visible instead of filling gaps with assumptions.

**Problem:** Product ideas are often scattered across meeting notes, user problems, business goals, and constraints, making it difficult to turn incomplete context into a clear first draft.

**Workflow:** Product context → AI synthesis → structured output validation → PRD draft

[Explore the automation →](./prd-copilot)

---

### Interview Prep Assistant

Uses a candidate's resume and target role to create personalized interview preparation around their actual experience.

**Problem:** Generic interview questions ignore the combination of what a candidate has claimed on their resume and the role they are actually preparing for.

**Workflow:** Resume + target role → text extraction → contextual analysis → structured preparation plan

[Explore the automation →](./interview-prep-assistant)

---

### Day Planner

Combines calendar commitments, backlog tasks, and current priorities to create a realistic plan around the time actually available.

**Problem:** Calendars show commitments and task lists show work, but neither answers what can realistically be completed when both compete for the same day.

**Workflow:** Calendar events + tasks + priorities → workload analysis → structured daily plan

[Explore the automation →](./day-planner)

---

### AI Email Assistant

Turns incoming emails into structured actions by identifying what needs attention, preparing replies, detecting calendar events, and summarizing inbox activity.

**Problem:** The real work of email begins after reading it—deciding what matters, what needs a response, what belongs on the calendar, and what should not be forgotten.

**Workflow:** Incoming email → analysis → structured actions → draft reply / calendar event → daily summary

[Explore the automation →](./ai-email-assistant)

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
├── sprint-summary-generator/
│   ├── README.md
│   ├── assets/
│   │   └── image.png
│   └── workflow/
│       └── sprint-summary-generator.json
│
├── prd-copilot/
│   ├── README.md
│   ├── assets/
│   │   └── image.png
│   └── workflow/
│       └── prd-copilot.json
│
├── interview-prep-assistant/
│   ├── README.md
│   ├── assets/
│   │   └── image.png
│   └── workflow/
│       └── interview-prep-assistant.json
│
├── day-planner/
│   ├── README.md
│   ├── assets/
│   │   └── image.png
│   └── workflow/
│       └── day-planner.json
│
└── ai-email-assistant/
    ├── README.md
    ├── assets/
    │   └── image.png
    └── workflow/
        └── ai-email-assistant.json