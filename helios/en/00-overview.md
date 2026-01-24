---
title: "Overview - Customer Portal"
---

## Objective

This document summarizes how to navigate the Customer Portal and how the modules connect to each other.

## Quick map of the portal

- Dashboard: general summary of the tenant and quick access.
- Agents: create and configure AI agents.
- Inbox: Email management with human review.
- WhatsApp: numbers, conversations and message panel.
- Voice Agents: voice agents and telephone numbers (Twilio).
- Web Chat: web widget conversations.
- Integrations: foreign keys (OpenAI, Google, Twilio, Gmail, etc.).
- Tools: functions and webhooks for agents to execute actions.
- Documents: knowledge base for RAG.
- SQL Tables: internal data tables for SQL queries.
- Contacts: contacts and leads.
- Analytics: general metrics.
- Team: users and roles.
- Settings: general settings, categories, Gmail, API keys and billing.
- Notifications: system alerts and channels.
- Onboarding/Plan: plan selection.

## Recommended general flow

1. Configure Integrations (OpenAI/Google/Twilio).
2. Create Agents and activate channels.
3. Connect Inbox (Gmail/Outlook/SMTP).
4. Connect WhatsApp and Voice Agents (Twilio).
5. Upload Documents and/or create SQL Tables.
6. Create Tools if external actions are required.
7. Test Agents and review Analytics.

## Conventions

- The UI uses labels in English. In these manuals they are maintained as is.
- Steps are described as routes within the portal.
- When a module requires external integrations, it is indicated in requirements.

## Suggested illustrations

- Capture of the Sidebar with all the modules.
- Simple flow diagram: Integrations -> Agents -> Channels.