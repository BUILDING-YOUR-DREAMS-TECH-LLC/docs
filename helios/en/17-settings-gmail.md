---
title: "Gmail Integrations"
---

## Objective

Connect Gmail accounts via OAuth to send and receive emails.

## Access

Settings -> Gmail
Path: /app/{tenant}/settings/gmail

## Roles

- owner, admin

## Connect Gmail

1. Select an agent in Assign agent.
2. Press Connect Gmail.
3. Complete Google OAuth.

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Assign agent | Yes | selection | Support Agent | Required for AI |

## Manage accounts

On each account:

-Go to Inbox
- Disconnect (Trash icon)
- View status (Active/Expired)

## Notes

- OAuth is more secure than app passwords.
- If the token expires, reconnect the account.


## Screenshot

![Gmail Settings](../../images/helios/en/screenshots/settings-03-gmail.png)

## Related

- [Inbox (Email)](/helios/en/04-inbox-email)
- [Integrations](/helios/en/08-integrations)

