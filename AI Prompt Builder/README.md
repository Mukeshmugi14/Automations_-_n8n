# PromptSmith – AI Prompt Builder

n8n workflow that asks user a few structured questions and returns a polished AI prompt for their use case.

## Features

- Collects goal, style, audience, format
- Builds a strong prompt string
- Can be triggered via webhook, Telegram, or form
- Returns prompt back to frontend or API caller

## Setup

1. Import `workflow.json` into n8n.
2. Use Webhook or manual trigger (depends on integration).
3. Integrate with frontend (form / Telegram / internal tool).

## Expected Input (Webhook)

```json
{
  "goal": "Write a LinkedIn post about product launch",
  "audience": "Startup founders",
  "tone": "Friendly and confident",
  "format": "Short post"
}
