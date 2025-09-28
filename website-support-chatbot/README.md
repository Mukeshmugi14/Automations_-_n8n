Website Support Chatbot
Overview
Website chat messages are received via a webhook, a prompt is constructed, an LLM endpoint is called, and the reply is returned to the requester.

Architecture
Trigger: Webhook endpoint for website chat events.

Logic: Prompt construction and LLM call.

Response: JSON reply streamed back to requester.

Prerequisites
n8n instance with access to public webhook URLs.

LLM provider credentials and endpoint.

HTTPS capability for production webhooks.

Environment variables
LLM_API_URL=<provider_endpoint>

LLM_API_KEY=<secret>

CHAT_AUTH_TOKEN=<optional_site_token>

Files
workflow.json

Import
Use n8n Editor UI to import workflow.json.

Verify nodes load without credential errors.

Configuration
Set Webhook path to website-chat or preferred route.

Add headers or auth in HTTP Request node for LLM.

Map input fields: message, text, site.

Testing
Use test webhook URL during development.

Send sample payload with message and site fields.

Confirm JSON reply contains reply property.

Deployment
Activate workflow to generate production webhook URL.

Update website integration to post to production URL.

Monitor executions and error logs.

Security
Validate origin via shared secret header.

Rate‑limit website calls at CDN or gateway layer.

Avoid logging sensitive user data.

Troubleshooting
401/403 from LLM: verify API key and headers.

Empty replies: log raw LLM response for parsing issues.

Timeouts: reduce prompt size or increase timeout.

Backup and versioning
Export workflow after changes and commit JSON to Git.

Tag releases corresponding to production deployments.
