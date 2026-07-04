# 🏃‍♂️ Sprint Summary Generator

An automated n8n workflow designed to streamline sprint reporting by processing sprint progress data through an AI agent (powered by OpenAI GPT-5 Mini), structuring the output, and distributing executive updates across Slack and Email (Gmail).

---

## 📊 Workflow Architecture

![Workflow Overview](./assets/image.png)

### 🔗 Key Stages

1. **Manual / Trigger Ingestion**: Initiates the workflow with structured sprint input data, including `completed_tickets`, `blocked_tickets`, `key_updates`, `bugs`, and `next_steps`.
2. **AI Summarization Agent**: Uses a LangChain Agent node powered by **OpenAI GPT-5 Mini** to synthesize raw sprint data into 3–5 concise bullet-style executive statements, highlighting notable wins, blockers, and risks.
3. **Structured Output Parsing**: Enforces a strict JSON schema via the **Sprint Summary Parser** to reliably extract structured fields: `sprint_summary`, `wins`, `blockers`, `risks`, and `next_steps`.
4. **Multi-Channel Distribution**:
   - **Slack**: Formats and broadcasts a clean Markdown report to your designated team channel.
   - **Gmail / Email**: Formats and dispatches an HTML email summary to stakeholders and leadership.

---

## 📂 Folder Structure

```text
sprint-summary-generator/
├── README.md                                  # Documentation & Setup Guide
├── workflow/
│   └── sprint-summary-generator.json          # n8n Workflow JSON Definition
└── assets/
    └── image.png                              # Visual architecture diagram
```

---

## ⚙️ Setup & Installation

### 1. Prerequisites
- **Automation Platform**: n8n (v1.x+ with LangChain nodes enabled).
- **API Credentials**:
  - **OpenAI API**: Credential for OpenAI GPT-5 Mini (`openAiApi`).
  - **Slack**: Webhook or Slack OAuth credential for channel posting.
  - **Gmail**: OAuth2 credential for sending email reports (`gmailOAuth2`).

### 2. Import Workflow
1. Navigate to your n8n workspace.
2. Select **Import from File** or **Import from JSON**.
3. Upload `workflow/sprint-summary-generator.json`.

### 3. Configure Credentials & Input Data
Update the credential connections and input parameters within the imported workflow:
- **OpenAI GPT-5 Mini**: Connect your OpenAI API credentials.
- **Send to Slack**: Select your target Slack channel or configure the webhook ID.
- **Send to Email**: Update the `sendTo` parameter in the Gmail node with recipient email addresses.
- **Manual Trigger / Input**: Pass in JSON payload containing `completed_tickets`, `blocked_tickets`, `key_updates`, `bugs`, and `next_steps`.

---

## 📝 Example Output Schema

The AI Agent outputs structured JSON parsed into clean reports for Slack and Gmail:

```json
{
  "sprint_summary": "Sprint progress remained on schedule with major deliverables completed across core services.",
  "wins": [
    "Successfully migrated authentication service to OAuth2",
    "Reduced API response latency by 25%"
  ],
  "blockers": [
    "Waiting on third-party vendor API access for billing module"
  ],
  "risks": [
    "Potential delay in Q3 release if sandbox testing is impeded"
  ],
  "next_steps": [
    "Begin end-to-end integration testing for checkout flow",
    "Finalize security audit remediation"
  ]
}
```
