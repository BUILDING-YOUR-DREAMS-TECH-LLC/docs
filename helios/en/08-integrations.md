---
title: "Integrations"
---

## Objective

Connect external services (LLM, mail, Twilio, calendars, webhooks) to enable portal features.

## Access

Sidebar -> Integrations
Path: /app/{tenant}/integrations

## Roles

- owner, admin, agent

## Integrations available

### Twilio (Voice & WhatsApp)

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Twilio Account SID | Yes | AC... | ACxxxxxxxxx | From Twilio Console |
| Twilio Auth Token | Yes | 32 chars | ******** | From Twilio Console |

Actions:

- Save Twilio Credentials
- Disconnect Twilio

###OpenAI

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| OpenAI API Key | Yes | sk-... | sk-xxxx | Required for AI |

Actions:

- Save OpenAI Key
- Remove OpenAI Key

### Google AI (Gemini)

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Google AI API Key | Yes | AIza... | AIza... | Required for RAG |

Actions:

- Save Google AI Key
- Remove Google AI Key

### Gmail (Email)

Actions:

- Connect (opens Settings/Gmail)
- Manage (if already connected)
-Go to Inbox

Notes:

- Requires assigning agent before connecting.

### Google Calendar

Action:

- Connect (OAuth)

###Microsoft 365

Action:

- Connect (OAuth)

### Custom Webhooks

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Name | Yes | text | N8N workflow | Internal name |
| Webhook URL | Yes | URL | https://... | External endpoint |

Actions:

- Add Webhook
-Remove

### ElevenLabs (TTS)

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| ElevenLabs API Key | Yes | text | elevenlabs_... | For premium voices |

### Bing Web Search

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Bing Web Search API Key | Yes | text | ... | Enable Web Search |

## Good practices

- Save Twilio once and reuse it in WhatsApp and Voice.
- Connect OpenAI or Google before creating agents.
- Use Webhooks for external actions (N8N, Make).


## Screenshot

![Integrations Overview](../../images/helios/en/screenshots/integrations-01-overview.png)

## Related

- [22-twilio-setup.md](./22-twilio-setup.md)
- [09-tools.md](./09-tools.md)

