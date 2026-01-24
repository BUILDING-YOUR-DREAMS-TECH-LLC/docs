---
title: "API Keys (BYOK)"
---

## Objective

Save your own API keys for OpenAI and Google AI.

## Access

Settings -> API Keys
Path: /app/{tenant}/settings/api-keys

## Roles

- owner, admin

## Save OpenAI API Key

1. In OpenAI API Key, paste your key.
2. Press Save & Verify.
3. Check the status (Verified/Unverified).

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| OpenAI API Key | Yes | sk-... | sk-xxxx | It is saved encrypted |

## Save Google AI API Key

1. In Google AI API Key, paste your key.
2. Press Save & Verify.

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Google AI API Key | Yes | AIza... | AIza... | It is saved encrypted |

## Delete key

- Use the trash icon on the key.

## Good practices

- Use production keys separate from tests.
- Set spending limits on the supplier.

## Related

- 08-integrations.md
- 03-agents.md

## Suggested illustrations

- Capture of API Keys with Verified status.