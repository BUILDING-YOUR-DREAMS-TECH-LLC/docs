---
title: "Screenshots Checklist"
---

This document centralizes all the screenshots suggested for the manuals and for registration of the application (landing and public pages).

## How to use this document

- Use a demo tenant and example data (not real).
- Hides sensitive data (real emails, tokens, phones).
- Maintains a consistent resolution (recommended: 1440x900 or 1920x1080).
- Complete forms with example data so that the UI is understood.
- Save each capture in a common folder and update the "Status" field.

## Suggested folder

- docs/user-manuals/en/assets/screenshots

## Naming convention

- {modulo}-{nn}-{slug}.png
- Examples: agents-01-list.png, whatsapp-02-connect-modal.png

## Landing and public pages

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| LAND-01 | Home hero (logo + CTA) | / | Open homepage | landing-01-home-hero.png | pending |
| LAND-02 | Home product section (features) | / | Scroll to product section | landing-02-features.png | pending |
| LAND-03 | Pricing cards | /pricing | Open pricing | landing-03-pricing.png | pending |
| LAND-04 | About hero/mission | /about | Open about | landing-04-about.png | pending |
| LAND-05 | Docs landing | /docs | Open docs | landing-05-docs.png | pending |
| LAND-06 | Blog list | /blog | Open blog | landing-06-blog.png | pending |
| LAND-07 | Careers | /careers | Open careers | landing-07-careers.png | pending |
| LAND-08 | Contact form | /contact | Open contact | landing-08-contact.png | pending |
| LAND-09 | Terms header | /terms | Open terms | landing-09-terms.png | pending |
| LAND-10 | Privacy header | /privacy | Open privacy | landing-10-privacy.png | pending |
| LAND-11 | Cookie header | /cookies | Open cookies | landing-11-cookies.png | pending |

## Authentication

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| AUTH-01 | Login with Google and Email | /login | Open login | auth-01-login.png | pending |
| AUTH-02 | Complete form signup | /signup?plan=... | Open signup with plan | auth-02-signup.png | pending |
| AUTH-03 | OAuth complete (company + subdomain) | /auth/complete | Login with Google without tenant | auth-03-auth-complete.png | pending |
| AUTH-04 | Forgot password | /forgot-password | Link Forgot Password | auth-04-forgot-password.png | pending |
| AUTH-05 | Reset password | /reset-password | Open reset link | auth-05-reset-password.png | pending |
| AUTH-06 | Invite (team) | /auth/invite/{token} | Open invitation | auth-06-invite.png | pending |
| AUTH-07 | Unauthorized | /unauthorized | Open route without permissions | auth-07-unauthorized.png | pending |

## Dashboard

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| DASH-01 | Main dashboard with cards | /app/{tenant}/dashboard | Sidebar -> Dashboard | dashboard-01-main.png | pending |

##Agents| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| AGT-01 | List of agents + Create button | /app/{tenant}/agents | Sidebar -> Agents | agents-01-list.png | pending |
| AGT-02 | Create Agent Step 1 (Basic Info) | /app/{tenant}/agents | Create Agent -> Step 1 | agents-02-create-step1.png | pending |
| AGT-03 | Create Agent Step 2 (Channels) | /app/{tenant}/agents | Create Agent -> Step 2 | agents-03-create-step2.png | pending |
| AGT-04 | Create Agent Step 3 (Capabilities) | /app/{tenant}/agents | Create Agent -> Step 3 | agents-04-create-step3.png | pending |
| AGT-05 | Create Agent Step 4 (AI Config) | /app/{tenant}/agents | Create Agent -> Step 4 | agents-05-create-step4.png | pending |
| AGT-06 | Edit Agent - Basic Info tab | /app/{tenant}/agents/{id}/edit | Open Edit | agents-06-edit-basic.png | pending |
| AGT-07 | Edit Agent - Channels tab | /app/{tenant}/agents/{id}/edit | Tab Channels | agents-07-edit-channels.png | pending |
| AGT-08 | Edit Agent - Tools tab (RAG/SQL/Tools) | /app/{tenant}/agents/{id}/edit | TabTools | agents-08-edit-tools.png | pending |
| AGT-09 | Edit Agent - AI Config tab | /app/{tenant}/agents/{id}/edit | Tab AI Config | agents-09-edit-ai.png | pending |
| AGT-10 | Agent Test view | /app/{tenant}/agents/{id}/test | Open Test | agents-10-test.png | pending |

## Inbox (Email)

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| INB-01 | Email Accounts (Gmail/Outlook/SMTP) | /app/{tenant}/inbox | Inbox -> Email Accounts | inbox-01-accounts.png | pending |
| INB-02 | Connect Gmail (assign agent) | /app/{tenant}/inbox | Connect Gmail modal | inbox-02-gmail-connect.png | pending |
| INB-03 | Connect SMTP/IMAP form | /app/{tenant}/inbox | Add via SMTP/IMAP | inbox-03-smtp-imap.png | pending |
| INB-04 | Inbox list with filters | /app/{tenant}/inbox/all | Inbox -> All | inbox-04-list.png | pending |
| INB-05 | Inbox list of an account | /app/{tenant}/inbox/{credentialId} | Click account | inbox-05-account-list.png | pending |
| INB-06 | Email detail with Summary and AI Response | /app/{tenant}/inbox/message/{id} | Open message | inbox-06-message-detail.png | pending |
| INB-07 | Email Configuration - Account Config | /app/{tenant}/inbox | Edit account | inbox-07-account-config.png | pending |
| INB-08 | Email Configuration - AI Response Settings | /app/{tenant}/inbox | Edit account | inbox-08-ai-settings.png | pending |
| INB-09 | Email Configuration - Categorization | /app/{tenant}/inbox | Edit account | inbox-09-categorization.png | pending |
| INB-10 | Email Configuration - Daily Summary | /app/{tenant}/inbox | Edit account | inbox-10-daily-summary.png | pending |

## WhatsApp| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| WA-01 | List of connected numbers | /app/{tenant}/whatsapp | Sidebar -> WhatsApp | whatsapp-01-numbers.png | pending |
| WA-02 | Connect New Number (Twilio) | /app/{tenant}/whatsapp | Connect New Number modal | whatsapp-02-connect-twilio.png | pending |
| WA-03 | Connect New Number (Meta Cloud API) | /app/{tenant}/whatsapp | Toggle Meta Cloud API | whatsapp-03-connect-meta.png | pending |
| WA-04 | Recent conversations (table) | /app/{tenant}/whatsapp | See table | whatsapp-04-conversations.png | pending |
| WA-05 | WhatsApp chat detail + AI Insights | /app/{tenant}/whatsapp/{id} | View Chat | whatsapp-05-chat-detail.png | pending |
| WA-06 | WhatsApp Notifications | /app/{tenant}/whatsapp/notifications | Sidebar -> WhatsApp Notifications | whatsapp-06-notifications.png | pending |
| WA-07 | WhatsApp Settings (if applicable) | /app/{tenant}/whatsapp/settings | Sidebar -> WhatsApp Settings | whatsapp-07-settings.png | pending |

##WebChat

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| WC-01 | Conversation list with filters | /app/{tenant}/conversations | Sidebar -> Web Chat | webchat-01-list.png | pending |
| WC-02 | Detailed conversation with input | /app/{tenant}/conversations/{id} | View | webchat-02-detail.png | pending |

## Voice Agents

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| VA-01 | Voice Agent List | /app/{tenant}/voice-agents | Sidebar -> Voice Agents | voice-01-list.png | pending |
| VA-02 | Create Voice Agent Step 1 | /app/{tenant}/voice-agents | Create Voice Agent -> Step 1 | voice-02-create-step1.png | pending |
| VA-03 | Create Voice Agent Step 2 (Voice Config) | /app/{tenant}/voice-agents | Create Voice Agent -> Step 2 | voice-03-create-step2.png | pending |
| VA-04 | Create Voice Agent Step 3 (Phone Number) | /app/{tenant}/voice-agents | Create Voice Agent -> Step 3 | voice-04-create-step3.png | pending |
| VA-05 | Edit Voice Agent | /app/{tenant}/voice-agents/{id}/edit | Edit | voice-05-edit.png | pending |
| VA-06 | Call list | /app/{tenant}/voice-agents/calls | Sidebar -> Calls | voice-06-calls.png | pending |
| VA-07 | Call details | /app/{tenant}/voice-agents/calls/{callId} | Open call | voice-07-call-detail.png | pending |

## Documents (RAG)

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| DOC-01 | List of documents with statuses | /app/{tenant}/documents | Sidebar -> Documents | documents-01-list.png | pending |
| DOC-02 | Upload Document modal | /app/{tenant}/documents | Upload Document | documents-02-upload-modal.png | pending |
| DOC-03 | Document Type dropdown open | /app/{tenant}/documents | Upload Document | documents-03-type-dropdown.png | pending |
| DOC-04 | Document in Processing/Failed status | /app/{tenant}/documents | On the list | documents-04-status.png | pending |

## SQL Tables| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| SQL-01 | List of tables + Create Table | /app/{tenant}/sql-tables | Sidebar -> SQL Tables | sql-01-list.png | pending |
| SQL-02 | Create Table modal (Schema) | /app/{tenant}/sql-tables | Create Table | sql-02-create-modal.png | pending |
| SQL-03 | Detail table with data | /app/{tenant}/sql-tables/{id} | Open table | sql-03-detail.png | pending |
| SQL-04 | Add Row form | /app/{tenant}/sql-tables/{id} | AddRow | sql-04-add-row.png | pending |
| SQL-05 | Natural Language Query + result | /app/{tenant}/sql-tables/{id} | Natural Language Query | sql-05-nlq.png | pending |

##Integrations

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| INT-01 | Integrations overview | /app/{tenant}/integrations | Sidebar -> Integrations | integrations-01-overview.png | pending |
| INT-02 | Twilio Card with SID/Token | /app/{tenant}/integrations | Twilio card | integrations-02-twilio.png | pending |
| INT-03 | OpenAI card with key loaded | /app/{tenant}/integrations | OpenAI card | integrations-03-openai.png | pending |
| INT-04 | Google AI card with key loaded | /app/{tenant}/integrations | Google AI card | integrations-04-google-ai.png | pending |
| INT-05 | Gmail connect / manage | /app/{tenant}/integrations | Gmail card | integrations-05-gmail.png | pending |
| INT-06 | Google Calendar connect | /app/{tenant}/integrations | Google Calendar card | integrations-06-calendar.png | pending |
| INT-07 | Microsoft 365 connect | /app/{tenant}/integrations | Microsoft 365 card | integrations-07-microsoft.png | pending |
| INT-08 | Webhooks list | /app/{tenant}/integrations | Custom Webhooks | integrations-08-webhooks.png | pending |
| INT-09 | Bing Web Search card | /app/{tenant}/integrations | Bing card | integrations-09-bing.png | pending |
| INT-10 | ElevenLabs card | /app/{tenant}/integrations | ElevenLabs card | integrations-10-elevenlabs.png | pending |

##Tools

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| TLS-01 | Tools List | /app/{tenant}/tools | Sidebar -> Tools | tools-01-list.png | pending |
| TLS-02 | Create Tool - API Request (URL + Method) | /app/{tenant}/tools | CreateTool | tools-02-api-request.png | pending |
| TLS-03 | Create Tool - API Request (Headers/Body) | /app/{tenant}/tools | CreateTool | tools-03-api-body.png | pending |
| TLS-04 | Create Tool - Integration Action | /app/{tenant}/tools | Create Tool -> Integration Action | tools-04-integration-action.png | pending |
| TLS-05 | Tool details / Parameters | /app/{tenant}/tools | OpenTool | tools-05-details.png | pending |

##Contacts

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| CNT-01 | Contact list + search | /app/{tenant}/contacts | Sidebar -> Contacts | contacts-01-list.png | pending |
| CNT-02 | Add Contact modal | /app/{tenant}/contacts | Add Contact | contacts-02-add-modal.png | pending |
| CNT-03 | Edit Contact modal | /app/{tenant}/contacts | Menu -> Edit | contacts-03-edit-modal.png | pending |

##Analytics| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| ANL-01 | Analytics Dashboard | /app/{tenant}/analytics | Sidebar -> Analytics | analytics-01-main.png | pending |

##Team

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| TEAM-01 | Team Member List | /app/{tenant}/team | Sidebar -> Team | team-01-list.png | pending |
| TEAM-02 | Invite Team Member modal | /app/{tenant}/team | Invite Team Member | team-02-invite.png | pending |
| TEAM-03 | Pending Invitations list | /app/{tenant}/team | Scroll down | team-03-pending.png | pending |

## Settings (General and submodules)

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| SET-01 | General settings (tenant info) | /app/{tenant}/settings | Sidebar -> Settings | settings-01-general.png | pending |
| SET-02 | Settings categories | /app/{tenant}/settings/categories | Settings -> Categories | settings-02-categories.png | pending |
| SET-03 | Gmail Settings | /app/{tenant}/settings/gmail | Settings -> Gmail | settings-03-gmail.png | pending |
| SET-04 | Settings API Keys | /app/{tenant}/settings/api-keys | Settings -> API Keys | settings-04-api-keys.png | pending |
| SET-05 | Settings Email | /app/{tenant}/settings/email | Settings -> Email | settings-05-email.png | pending |
| SET-06 | Settings Billing | /app/{tenant}/settings/billing | Settings -> Billing | settings-06-billing.png | pending |

## Billing and Usage

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| BILL-01 | Usage / consumption | /app/{tenant}/usage | Sidebar -> Usage | billing-01-usage.png | pending |

##Notifications

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| NOTI-01 | General notifications | /app/{tenant}/notifications | Sidebar -> Notifications | notifications-01-list.png | pending |
| NOTI-02 | WhatsApp Notifications | /app/{tenant}/whatsapp/notifications | Sidebar -> WhatsApp Notifications | notifications-02-whatsapp.png | pending |

## Onboarding

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| ONB-01 | Onboarding plan | /app/{tenant}/onboarding/plan | Sidebar -> Onboarding | onboarding-01-plan.png | pending |

## Web Chat Widget (embed)

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| WID-01 | Widget snippet in HTML | N/A | Capture in code editor | widget-01-snippet.png | pending |

## Twilio Console (external)

| ID | Capture | Route | How to get there | Suggested file | Status |
| --- | --- | --- | --- | --- | --- |
| TW-01 | Account SID and Auth Token | https://console.twilio.com | Twilio Console -> Account | twilio-01-credentials.png | pending |
| TW-02 | WhatsApp Senders list | https://console.twilio.com | Messaging -> Senders -> WhatsApp | twilio-02-wa-senders.png | pending |
| TW-03 | WhatsApp webhook config | https://console.twilio.com | Messaging -> Services or Senders | twilio-03-wa-webhook.png | pending |
| TW-04 | Phone Numbers list | https://console.twilio.com | Phone Numbers -> Manage | twilio-04-numbers.png | pending |
| TW-05 | Voice webhook config | https://console.twilio.com | Phone Numbers -> Number -> Voice | twilio-05-voice-webhook.png | pending |## Notes to attach screenshots

- Save the image in the suggested folder.
- Update the "Status" field to "ok" when ready.
- If you want to see the image in this document, add a Markdown link below the row:
  ![AGT-01](assets/screenshots/agents-01-list.png)