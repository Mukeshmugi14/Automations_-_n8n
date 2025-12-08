# NeoChat – Telegram AI Companion

AI assistant that lives inside Telegram. Users chat with the bot and get intelligent responses.

## Features

- Telegram Bot integration
- General Q&A / brainstorming / explanations
- Custom persona (e.g. coder, tutor, marketer)
- Logs user queries (optional)

## Prerequisites

- Telegram Bot Token from @BotFather
- n8n instance
- LLM API key

## Setup

1. Create a bot via @BotFather and get `TELEGRAM_BOT_TOKEN`.
2. Import `workflow.json` into n8n.
3. Set environment variables:
   - `TELEGRAM_BOT_TOKEN`
   - `OPENAI_API_KEY`
4. In Telegram node, set:
   - Updates via Webhook or polling
5. Deploy n8n URL as Telegram bot webhook if using webhook mode.

## Usage

- User sends message to Telegram bot
- Workflow:
  - Receives message
  - Generates answer via LLM
  - Sends reply back to user

## Customization

- Change system prompt in Function node to adjust personality
- Add conversation history memory (store to DB/Redis)
