# PRD Copilot

An AI-assisted workflow that turns raw product context into a structured PRD draft while keeping missing information visible instead of filling gaps with assumptions.

![PRD Copilot Workflow](./assets/workflow-overview.png)

## The Problem

Product ideas rarely begin as clean documents.

Context is usually scattered across feature ideas, meeting notes, user problems, business goals, and constraints. Turning that information into a usable first draft takes time, and important gaps can easily be hidden when the document is written too quickly.

The bigger risk is not an incomplete PRD. It is a confident-looking PRD built on assumptions that were never validated.

## What I Built

I built a workflow that takes available product context and converts it into a structured PRD draft.

The workflow accepts:

- feature idea
- meeting notes
- user problem
- business goal
- constraints

It then structures the available context into:

- problem statement
- goal
- target users
- user stories
- in-scope items
- out-of-scope items
- assumptions
- risks
- success metrics
- open questions

If important information is missing, the workflow is instructed to mark it as unknown rather than inventing an answer.

## How It Works

```text
Raw Product Context
        ↓
Feature Idea · Meeting Notes · User Problem
Business Goal · Constraints
        ↓
PRD Generation
        ↓
Structured Output Validation
        ↓
PRD Draft