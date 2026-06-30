# Auto AI Internship Applier

## Overview

Auto AI Internship Applier is an automation workflow developed using n8n that simplifies the process of applying for internship opportunities. The workflow integrates Google Sheets, Google Gemini AI, and Gmail to automatically generate personalized internship application emails and send them to hiring managers.

The primary objective of this project is to eliminate repetitive manual tasks involved in preparing and sending application emails while demonstrating practical implementation of workflow automation and AI integration.

---

## Motivation

Applying to multiple companies requires writing similar emails repeatedly, which is both time-consuming and inefficient. As a Computer Science student interested in automation and artificial intelligence, I built this project to explore how AI can be combined with workflow automation tools to solve real-world problems.

This project allowed me to gain practical experience in integrating cloud services, designing automated workflows, and using large language models to generate professional communication.

---

## Key Features

* Automatically monitors a Google Sheet for new internship application records.
* Retrieves applicant details such as name, skills, experience, and target role.
* Uses Google Gemini AI to generate a personalized internship application email.
* Formats the generated response into a structured output.
* Sends the email automatically through Gmail.
* Reduces manual effort by automating the complete email generation and delivery process.
* Uses secure authentication through Google OAuth credentials (excluded from this repository).

---

## Technology Stack

| Technology       | Purpose                                  |
| ---------------- | ---------------------------------------- |
| n8n              | Workflow automation platform             |
| Google Sheets    | Stores applicant information             |
| Google Gemini AI | Generates personalized email content     |
| Gmail API        | Sends application emails                 |
| JSON             | Workflow configuration and data exchange |

---

## Workflow

The workflow follows the sequence below:

1. A new applicant record is added to a Google Sheet.
2. The Google Sheets Trigger detects the new entry.
3. Applicant information is passed to the Google Gemini AI model.
4. Gemini generates a professional internship application email based on the provided details.
5. A Structured Output Parser formats the AI response into a consistent JSON structure.
6. Gmail sends the generated email to the specified hiring manager automatically.

---

## Workflow Architecture

```
Google Sheets
       │
       ▼
Google Sheets Trigger
       │
       ▼
Google Gemini AI
       │
       ▼
Structured Output Parser
       │
       ▼
Gmail
       │
       ▼
Application Email Sent
```

---

## Project Structure

```
Auto-AI-Internship-Applier/
│
├── workflow.json
├── README.md
├── LICENSE
├── .gitignore
└── docs/
    └── workflow.png
```

---

## Getting Started

### Prerequisites

Before importing the workflow, ensure the following services are available:

* n8n (Cloud or Self-hosted)
* Google Account
* Google Sheets
* Gmail
* Google Gemini API access

### Installation

1. Clone this repository.

```bash
git clone https://github.com/your-username/Auto-AI-Internship-Applier.git
```

2. Open your n8n workspace.

3. Import the `workflow.json` file.

4. Configure the required credentials:

   * Google Sheets OAuth
   * Gmail OAuth
   * Google Gemini API

5. Replace the sample Google Spreadsheet ID with your own spreadsheet.

6. Activate the workflow.

7. Add applicant details to the configured Google Sheet to begin sending automated internship application emails.

---

## Repository Contents

| File                | Description                         |
| ------------------- | ----------------------------------- |
| `workflow.json`     | Main n8n workflow                   |
| `README.md`         | Project documentation               |
| `LICENSE`           | MIT License                         |
| `.gitignore`        | Files excluded from version control |
| `docs/workflow.png` | Workflow screenshot                 |

---

## Future Enhancements

The following improvements are planned for future versions:

* Automatic resume attachment support
* LinkedIn Jobs integration
* Application status tracking dashboard
* Duplicate application detection
* Multi-language email generation
* Email scheduling functionality
* Logging and notification support

---

## Learning Outcomes

This project provided hands-on experience with:

* Workflow automation using n8n
* AI-powered content generation
* Google Workspace API integration
* OAuth authentication
* Prompt engineering
* JSON-based workflow design
* Automation of repetitive business processes

---

## Security Notice

For security reasons, this repository does not include:

* Google OAuth credentials
* API keys
* Personal email addresses
* Webhook identifiers
* Sensitive configuration values

After importing the workflow, users must configure their own credentials before execution.

---

## Contributing

Contributions are welcome.

If you would like to improve this project, you can:

* Report issues
* Suggest enhancements
* Submit pull requests
* Improve documentation

Please create an issue before making major changes so that the proposed improvements can be discussed.

##
