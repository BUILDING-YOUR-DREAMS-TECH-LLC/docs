---
title: "Web Chat"
---

## Objective

Manage web chat conversations embedded in websites.

## Access

Sidebar -> Web Chat
Path: /app/{tenant}/conversations

## Roles

- owner, admin, agent

## Prerequisites

- An agent with Web Chat channel enabled.
- Widget installed on your site (see web chat widget).

## Conversation list

In the main view you can:

- Filter by status: active, closed, archived.
- Open a conversation with View.

Data displayed:

- Name of the visitor (or Anonymous Visitor)
- Email or visitor_id
- Agent assigned
- Date and time

## Conversation detail

Path: /app/{tenant}/conversations/{id}

Actions:

- Send message (input + Send)
-Transfer to Human
- Close (if status active)
- Archive (if status closed)

Notes:

- The panel updates every few seconds.
- Messages show if they used RAG or SQL.

## Good practices

- Use Transfer to Human when the user requests it.
- Close the conversation when the topic is resolved.


## Screenshot

![Web Chat Conversations](../../images/helios/en/screenshots/webchat-01-list.png)

## Related

- [23-web-chat-widget.md](./23-web-chat-widget.md) (widget installation)

