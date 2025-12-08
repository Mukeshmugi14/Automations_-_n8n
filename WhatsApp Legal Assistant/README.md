# LexiChat – WhatsApp Legal Assistant

AI assistant over WhatsApp that helps users understand legal concepts and documents in simple language.

## Disclaimer

This is **not** a replacement for a licensed lawyer. Always include legal disclaimers in your UI/responses.

## Features

- WhatsApp chat interface
- Simplifies legal text and concepts
- Suggests questions to ask a real lawyer
- Logs conversations (optional)

## Setup Overview

1. Get WhatsApp API / provider with webhooks.
2. Configure incoming message webhook to call n8n Webhook node.
3. Import `workflow.json` into n8n.
4. Set `OPENAI_API_KEY` and WhatsApp API credentials.

## Flow

- User sends text (e.g., clause, question) on WhatsApp.
- Provider hits n8n webhook.
- n8n sends text to LLM with legal assistant prompt.
- n8n sends answer back via WhatsApp API.

## Customization

- Edit system prompt in `Prepare Prompt` node.
- Add logging (Sheets/DB).
- Add language support.
