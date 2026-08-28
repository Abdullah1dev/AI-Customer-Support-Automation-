# AI Customer Support Automation

An n8n-based AI automation workflow that processes customer support requests submitted through a Google Form and stored in Google Sheets.

## Workflow

Google Form
    ↓
Google Sheets
    ↓
Google Sheets Trigger
    ↓
AI Agent
    ↓
IF Condition
    ↓
High / Normal Priority
    ↓
Google Sheets

## Features

- Detects new customer support submissions
- Uses n8n Google Sheets Trigger
- Processes requests using an AI Agent
- Uses an OpenRouter chat model
- Classifies customer issues
- Determines urgency
- Generates a summary
- Recommends an appropriate support action
- Uses conditional branching based on urgency
- Stores AI analysis in Google Sheets

## AI Processing

The AI Agent analyzes:

- Customer name
- Issue type
- Customer message
- Preferred contact method

The AI generates:

- Issue type
- Urgency
- Summary
- Recommended action

## Tech Stack

- n8n
- Google Forms
- Google Sheets
- AI Agent
- OpenRouter
- LLM
- Conditional workflow logic

## Setup

1. Import `ai-customer-support-automation.json` into n8n.
2. Connect your own Google Sheets credentials.
3. Configure your own OpenRouter credentials.
4. Select the required Google Sheet and worksheet.
5. Execute the workflow with a test submission.

## Security

API keys, OAuth credentials, and other secrets are not included in this repository.

## Example

Example customer request:

> I was charged twice for my subscription and need help getting a refund.

Example AI analysis:

- Issue Type: Billing/Payment Issue
- Urgency: Medium
- Summary: Customer reports a duplicate subscription charge.
- Recommended Action: Verify the duplicate charge and process a refund if confirmed.