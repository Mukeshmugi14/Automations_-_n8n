# CallMind – Customer Support Calling Agent

AI calling agent to send voice reminders / notifications to customers.

> Note: Actual voice calling requires a telephony provider (e.g. Twilio, Exotel, etc.).

## Features

- Call customers with reminder script
- Customizable script and variables (name, time, purpose)
- Logs call status

## Setup

1. Choose telephony provider (e.g. Twilio).
2. Configure n8n HTTP Request node to call provider's Voice API.
3. Import `workflow.json`.
4. Trigger via:
   - Cron (daily reminders)
   - Webhook (on event)
   - From another workflow

## Input Example

```json
{
  "phone": "+911234567890",
  "name": "John",
  "reminder": "Your payment is due tomorrow."
}
