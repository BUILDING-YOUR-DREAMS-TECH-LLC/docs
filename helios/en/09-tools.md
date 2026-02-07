---
title: "Tools & Functions"
---

## Objective

Create functions that agents can execute (webhooks or integration actions).

## Access

Sidebar -> Tools
Path: /app/{tenant}/tools

## Roles

- owner, admin, agent

## Prerequisites

- Connected Integrations if you want Integration Actions.

## Create a Tool

Press Create Tool.

### Type 1: API Request (Webhook)

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Tool Name | Yes | text | Book Appointment | Display name |
| Description | No | text | Book an appointment in CRM | Help the agent |
| URL API | Yes | URL | https://api.example.com/appointments | Supports {variable} |
| HTTPMethod | Yes | GET/POST/PUT/DELETE | POST | - |
| Authentication | No | none/bearer/basic | bearer | Optional |
| Bearer Token | Yes yes bearer | text | ******** | - |
| Basic Auth | Yes yes basic | user/pass | user/pass | - |
| Headers | No | key/value | Authorization | Use {variable} |
| Query Params | No | key/value | status=active | Use {variable} |
| Body (JSON) | No | JSON | {"id":"{contactId}"} | Valid JSON |
| Parameters Schema | No | JSON schema | {"type":"object"...} | Describe args |

Notes:

- If Body is empty, the tool payload is sent as JSON.
- Use {variable} to insert tool arguments.

### Type 2: Integration Action

Steps:

1. Select the integration (Google Calendar, Gmail, etc.).
2. Choose mode:
   - Quick Add Multiple: multiple selection.
   - Add Single (Custom): customize name/description.

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Integration | Yes | selection | Google Calendar | Must be connected |
| Action | Yes | selection | Create event | According to catalog |
| Tool Name | Yes (custom) | text | Create Meeting | Editable |
| Description | No | text | Create event | Editable |

## See Tools

In the list you can:

- See description.
- Open Parameters and Details.
- Delete tool.

## Good practices

- Use actionable names (Create Ticket, Update Order).
- Define Parameters Schema to avoid errors in execution.
- Document examples in Description if possible.

## Related

- 08-integrations.md
- 03-agents.md (tool selection)

## Suggested illustrations

### Create Tool (API Request)
![Create Tool](../../images/helios/en/tools/tool-create-modal.png)