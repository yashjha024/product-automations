# Product Automations 🤖

Automations I build to remove repetitive work, improve workflows, and explore how AI can support real decisions.

---

## 📁 Repository Structure

This repository is structured systematically to house JSON-based automation workflows (such as n8n, Make, or custom automation engines), along with their documentation and visual assets directly in the root directory.

```text
product-automations/
├── README.md
└── <automation-name>/
    ├── README.md
    ├── workflow/
    │   └── <automation-name>.json
    └── assets/
        └── image.png
```

## 🚀 Available Automations

| Automation | Description | Workflow | Documentation |
| :--- | :--- | :--- | :--- |
| **[Sprint Summary Generator](./sprint-summary-generator)** | Automatically aggregates sprint tasks, generates AI-powered executive summaries, and distributes reports. | [JSON](./sprint-summary-generator/workflow/sprint-summary-generator.json) | [README](./sprint-summary-generator/README.md) |

---

## 🛠️ How to Add a New Automation

1. Create a new project directory directly in the root folder `<automation-name>/`.
2. Add your workflow JSON definition inside `workflow/<automation-name>.json`.
3. Add a visual architecture diagram or screenshot in `assets/image.png`.
4. Include a dedicated `README.md` detailing the prerequisites, triggers, nodes, and setup instructions.
