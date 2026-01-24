---
title: "Lista de capturas (checklist)"
---


Este documento centraliza todas las capturas sugeridas para los manuales y para registro de la aplicacion (landing y paginas publicas).

## Como usar este documento

- Usa un tenant demo y datos de ejemplo (no reales).
- Oculta datos sensibles (emails reales, tokens, telefonos).
- Mantiene una resolucion consistente (recomendado: 1440x900 o 1920x1080).
- Completa formularios con datos de ejemplo para que la UI se entienda.
- Guarda cada captura en una carpeta comun y actualiza el campo "Estado".

## Carpeta sugerida

- docs/user-manuals/es/assets/screenshots

## Convencion de nombres

- {modulo}-{nn}-{slug}.png
- Ejemplos: agents-01-list.png, whatsapp-02-connect-modal.png

## Landing y paginas publicas

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| LAND-01 | Home hero (logo + CTA) | / | Abrir homepage | landing-01-home-hero.png | pendiente |
| LAND-02 | Home seccion de producto (features) | / | Scroll a seccion de producto | landing-02-features.png | pendiente |
| LAND-03 | Pricing cards | /pricing | Abrir pricing | landing-03-pricing.png | pendiente |
| LAND-04 | About hero/mission | /about | Abrir about | landing-04-about.png | pendiente |
| LAND-05 | Docs landing | /docs | Abrir docs | landing-05-docs.png | pendiente |
| LAND-06 | Blog list | /blog | Abrir blog | landing-06-blog.png | pendiente |
| LAND-07 | Careers | /careers | Abrir careers | landing-07-careers.png | pendiente |
| LAND-08 | Contact form | /contact | Abrir contact | landing-08-contact.png | pendiente |
| LAND-09 | Terms header | /terms | Abrir terms | landing-09-terms.png | pendiente |
| LAND-10 | Privacy header | /privacy | Abrir privacy | landing-10-privacy.png | pendiente |
| LAND-11 | Cookies header | /cookies | Abrir cookies | landing-11-cookies.png | pendiente |

## Autenticacion

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| AUTH-01 | Login con Google y Email | /login | Abrir login | auth-01-login.png | pendiente |
| AUTH-02 | Signup formulario completo | /signup?plan=... | Abrir signup con plan | auth-02-signup.png | pendiente |
| AUTH-03 | OAuth complete (company + subdomain) | /auth/complete | Ingresar con Google sin tenant | auth-03-auth-complete.png | pendiente |
| AUTH-04 | Forgot password | /forgot-password | Link Forgot Password | auth-04-forgot-password.png | pendiente |
| AUTH-05 | Reset password | /reset-password | Abrir link de reset | auth-05-reset-password.png | pendiente |
| AUTH-06 | Invite (team) | /auth/invite/{token} | Abrir invitacion | auth-06-invite.png | pendiente |
| AUTH-07 | Unauthorized | /unauthorized | Abrir ruta sin permisos | auth-07-unauthorized.png | pendiente |

## Dashboard

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| DASH-01 | Dashboard principal con cards | /app/{tenant}/dashboard | Sidebar -> Dashboard | dashboard-01-main.png | pendiente |

## Agents

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| AGT-01 | Lista de agents + boton Create | /app/{tenant}/agents | Sidebar -> Agents | agents-01-list.png | pendiente |
| AGT-02 | Create Agent Step 1 (Basic Info) | /app/{tenant}/agents | Create Agent -> Step 1 | agents-02-create-step1.png | pendiente |
| AGT-03 | Create Agent Step 2 (Channels) | /app/{tenant}/agents | Create Agent -> Step 2 | agents-03-create-step2.png | pendiente |
| AGT-04 | Create Agent Step 3 (Capabilities) | /app/{tenant}/agents | Create Agent -> Step 3 | agents-04-create-step3.png | pendiente |
| AGT-05 | Create Agent Step 4 (AI Config) | /app/{tenant}/agents | Create Agent -> Step 4 | agents-05-create-step4.png | pendiente |
| AGT-06 | Edit Agent - Basic Info tab | /app/{tenant}/agents/{id}/edit | Abrir Edit | agents-06-edit-basic.png | pendiente |
| AGT-07 | Edit Agent - Channels tab | /app/{tenant}/agents/{id}/edit | Tab Channels | agents-07-edit-channels.png | pendiente |
| AGT-08 | Edit Agent - Tools tab (RAG/SQL/Tools) | /app/{tenant}/agents/{id}/edit | Tab Tools | agents-08-edit-tools.png | pendiente |
| AGT-09 | Edit Agent - AI Config tab | /app/{tenant}/agents/{id}/edit | Tab AI Config | agents-09-edit-ai.png | pendiente |
| AGT-10 | Agent Test view | /app/{tenant}/agents/{id}/test | Open Test | agents-10-test.png | pendiente |

## Inbox (Email)

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| INB-01 | Email Accounts (Gmail/Outlook/SMTP) | /app/{tenant}/inbox | Inbox -> Email Accounts | inbox-01-accounts.png | pendiente |
| INB-02 | Connect Gmail (assign agent) | /app/{tenant}/inbox | Connect Gmail modal | inbox-02-gmail-connect.png | pendiente |
| INB-03 | Connect SMTP/IMAP form | /app/{tenant}/inbox | Add via SMTP/IMAP | inbox-03-smtp-imap.png | pendiente |
| INB-04 | Inbox list con filtros | /app/{tenant}/inbox/all | Inbox -> All | inbox-04-list.png | pendiente |
| INB-05 | Inbox list de una cuenta | /app/{tenant}/inbox/{credentialId} | Click cuenta | inbox-05-account-list.png | pendiente |
| INB-06 | Email detail con Summary y AI Response | /app/{tenant}/inbox/message/{id} | Abrir mensaje | inbox-06-message-detail.png | pendiente |
| INB-07 | Email Configuration - Account Config | /app/{tenant}/inbox | Edit account | inbox-07-account-config.png | pendiente |
| INB-08 | Email Configuration - AI Response Settings | /app/{tenant}/inbox | Edit account | inbox-08-ai-settings.png | pendiente |
| INB-09 | Email Configuration - Categorization | /app/{tenant}/inbox | Edit account | inbox-09-categorization.png | pendiente |
| INB-10 | Email Configuration - Daily Summary | /app/{tenant}/inbox | Edit account | inbox-10-daily-summary.png | pendiente |

## WhatsApp

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| WA-01 | Lista de numeros conectados | /app/{tenant}/whatsapp | Sidebar -> WhatsApp | whatsapp-01-numbers.png | pendiente |
| WA-02 | Connect New Number (Twilio) | /app/{tenant}/whatsapp | Connect New Number modal | whatsapp-02-connect-twilio.png | pendiente |
| WA-03 | Connect New Number (Meta Cloud API) | /app/{tenant}/whatsapp | Toggle Meta Cloud API | whatsapp-03-connect-meta.png | pendiente |
| WA-04 | Conversaciones recientes (tabla) | /app/{tenant}/whatsapp | Ver tabla | whatsapp-04-conversations.png | pendiente |
| WA-05 | WhatsApp chat detail + AI Insights | /app/{tenant}/whatsapp/{id} | View Chat | whatsapp-05-chat-detail.png | pendiente |
| WA-06 | WhatsApp Notifications | /app/{tenant}/whatsapp/notifications | Sidebar -> WhatsApp Notifications | whatsapp-06-notifications.png | pendiente |
| WA-07 | WhatsApp Settings (si aplica) | /app/{tenant}/whatsapp/settings | Sidebar -> WhatsApp Settings | whatsapp-07-settings.png | pendiente |

## Web Chat

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| WC-01 | Lista de conversaciones con filtros | /app/{tenant}/conversations | Sidebar -> Web Chat | webchat-01-list.png | pendiente |
| WC-02 | Conversacion detalle con input | /app/{tenant}/conversations/{id} | View | webchat-02-detail.png | pendiente |

## Voice Agents

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| VA-01 | Lista de Voice Agents | /app/{tenant}/voice-agents | Sidebar -> Voice Agents | voice-01-list.png | pendiente |
| VA-02 | Create Voice Agent Step 1 | /app/{tenant}/voice-agents | Create Voice Agent -> Step 1 | voice-02-create-step1.png | pendiente |
| VA-03 | Create Voice Agent Step 2 (Voice Config) | /app/{tenant}/voice-agents | Create Voice Agent -> Step 2 | voice-03-create-step2.png | pendiente |
| VA-04 | Create Voice Agent Step 3 (Phone Number) | /app/{tenant}/voice-agents | Create Voice Agent -> Step 3 | voice-04-create-step3.png | pendiente |
| VA-05 | Edit Voice Agent | /app/{tenant}/voice-agents/{id}/edit | Edit | voice-05-edit.png | pendiente |
| VA-06 | Calls list | /app/{tenant}/voice-agents/calls | Sidebar -> Calls | voice-06-calls.png | pendiente |
| VA-07 | Call detail | /app/{tenant}/voice-agents/calls/{callId} | Open call | voice-07-call-detail.png | pendiente |

## Documents (RAG)

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| DOC-01 | Lista de documentos con estados | /app/{tenant}/documents | Sidebar -> Documents | documents-01-list.png | pendiente |
| DOC-02 | Upload Document modal | /app/{tenant}/documents | Upload Document | documents-02-upload-modal.png | pendiente |
| DOC-03 | Document Type dropdown abierto | /app/{tenant}/documents | Upload Document | documents-03-type-dropdown.png | pendiente |
| DOC-04 | Documento en estado Processing/Failed | /app/{tenant}/documents | En la lista | documents-04-status.png | pendiente |

## SQL Tables

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| SQL-01 | Lista de tablas + Create Table | /app/{tenant}/sql-tables | Sidebar -> SQL Tables | sql-01-list.png | pendiente |
| SQL-02 | Create Table modal (Schema) | /app/{tenant}/sql-tables | Create Table | sql-02-create-modal.png | pendiente |
| SQL-03 | Tabla detalle con datos | /app/{tenant}/sql-tables/{id} | Abrir tabla | sql-03-detail.png | pendiente |
| SQL-04 | Add Row form | /app/{tenant}/sql-tables/{id} | Add Row | sql-04-add-row.png | pendiente |
| SQL-05 | Natural Language Query + resultado | /app/{tenant}/sql-tables/{id} | Natural Language Query | sql-05-nlq.png | pendiente |

## Integrations

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| INT-01 | Vista general de Integrations | /app/{tenant}/integrations | Sidebar -> Integrations | integrations-01-overview.png | pendiente |
| INT-02 | Tarjeta Twilio con SID/Token | /app/{tenant}/integrations | Twilio card | integrations-02-twilio.png | pendiente |
| INT-03 | Tarjeta OpenAI con key cargada | /app/{tenant}/integrations | OpenAI card | integrations-03-openai.png | pendiente |
| INT-04 | Tarjeta Google AI con key cargada | /app/{tenant}/integrations | Google AI card | integrations-04-google-ai.png | pendiente |
| INT-05 | Gmail connect / manage | /app/{tenant}/integrations | Gmail card | integrations-05-gmail.png | pendiente |
| INT-06 | Google Calendar connect | /app/{tenant}/integrations | Google Calendar card | integrations-06-calendar.png | pendiente |
| INT-07 | Microsoft 365 connect | /app/{tenant}/integrations | Microsoft 365 card | integrations-07-microsoft.png | pendiente |
| INT-08 | Webhooks list | /app/{tenant}/integrations | Custom Webhooks | integrations-08-webhooks.png | pendiente |
| INT-09 | Bing Web Search card | /app/{tenant}/integrations | Bing card | integrations-09-bing.png | pendiente |
| INT-10 | ElevenLabs card | /app/{tenant}/integrations | ElevenLabs card | integrations-10-elevenlabs.png | pendiente |

## Tools

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| TLS-01 | Lista de Tools | /app/{tenant}/tools | Sidebar -> Tools | tools-01-list.png | pendiente |
| TLS-02 | Create Tool - API Request (URL + Method) | /app/{tenant}/tools | Create Tool | tools-02-api-request.png | pendiente |
| TLS-03 | Create Tool - API Request (Headers/Body) | /app/{tenant}/tools | Create Tool | tools-03-api-body.png | pendiente |
| TLS-04 | Create Tool - Integration Action | /app/{tenant}/tools | Create Tool -> Integration Action | tools-04-integration-action.png | pendiente |
| TLS-05 | Tool details / Parameters | /app/{tenant}/tools | Open Tool | tools-05-details.png | pendiente |

## Contacts

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| CNT-01 | Lista de contactos + search | /app/{tenant}/contacts | Sidebar -> Contacts | contacts-01-list.png | pendiente |
| CNT-02 | Add Contact modal | /app/{tenant}/contacts | Add Contact | contacts-02-add-modal.png | pendiente |
| CNT-03 | Edit Contact modal | /app/{tenant}/contacts | Menu -> Edit | contacts-03-edit-modal.png | pendiente |

## Analytics

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| ANL-01 | Dashboard de Analytics | /app/{tenant}/analytics | Sidebar -> Analytics | analytics-01-main.png | pendiente |

## Team

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| TEAM-01 | Lista de Team Members | /app/{tenant}/team | Sidebar -> Team | team-01-list.png | pendiente |
| TEAM-02 | Invite Team Member modal | /app/{tenant}/team | Invite Team Member | team-02-invite.png | pendiente |
| TEAM-03 | Pending Invitations list | /app/{tenant}/team | Scroll abajo | team-03-pending.png | pendiente |

## Settings (General y submodulos)

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| SET-01 | Settings general (tenant info) | /app/{tenant}/settings | Sidebar -> Settings | settings-01-general.png | pendiente |
| SET-02 | Settings categories | /app/{tenant}/settings/categories | Settings -> Categories | settings-02-categories.png | pendiente |
| SET-03 | Settings Gmail | /app/{tenant}/settings/gmail | Settings -> Gmail | settings-03-gmail.png | pendiente |
| SET-04 | Settings API Keys | /app/{tenant}/settings/api-keys | Settings -> API Keys | settings-04-api-keys.png | pendiente |
| SET-05 | Settings Email | /app/{tenant}/settings/email | Settings -> Email | settings-05-email.png | pendiente |
| SET-06 | Settings Billing | /app/{tenant}/settings/billing | Settings -> Billing | settings-06-billing.png | pendiente |

## Billing y Usage

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| BILL-01 | Usage / consumo | /app/{tenant}/usage | Sidebar -> Usage | billing-01-usage.png | pendiente |

## Notifications

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| NOTI-01 | Notifications general | /app/{tenant}/notifications | Sidebar -> Notifications | notifications-01-list.png | pendiente |
| NOTI-02 | WhatsApp Notifications | /app/{tenant}/whatsapp/notifications | Sidebar -> WhatsApp Notifications | notifications-02-whatsapp.png | pendiente |

## Onboarding

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| ONB-01 | Onboarding plan | /app/{tenant}/onboarding/plan | Sidebar -> Onboarding | onboarding-01-plan.png | pendiente |

## Web Chat Widget (embed)

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| WID-01 | Snippet del widget en HTML | N/A | Captura en editor de codigo | widget-01-snippet.png | pendiente |

## Twilio Console (externo)

| ID | Captura | Ruta | Como llegar | Archivo sugerido | Estado |
| --- | --- | --- | --- | --- | --- |
| TW-01 | Account SID y Auth Token | https://console.twilio.com | Twilio Console -> Account | twilio-01-credentials.png | pendiente |
| TW-02 | WhatsApp Senders list | https://console.twilio.com | Messaging -> Senders -> WhatsApp | twilio-02-wa-senders.png | pendiente |
| TW-03 | WhatsApp webhook config | https://console.twilio.com | Messaging -> Services o Senders | twilio-03-wa-webhook.png | pendiente |
| TW-04 | Phone Numbers list | https://console.twilio.com | Phone Numbers -> Manage | twilio-04-numbers.png | pendiente |
| TW-05 | Voice webhook config | https://console.twilio.com | Phone Numbers -> Number -> Voice | twilio-05-voice-webhook.png | pendiente |

## Notas para adjuntar capturas

- Guarda la imagen en la carpeta sugerida.
- Actualiza el campo "Estado" a "ok" cuando este lista.
- Si quieres ver la imagen en este documento, agrega un link Markdown debajo de la fila:
  ![AGT-01](assets/screenshots/agents-01-list.png)
