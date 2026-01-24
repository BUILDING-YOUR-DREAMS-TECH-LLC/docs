---
title: "Overview - Portal del Cliente"
---


## Objetivo

Este documento resume como navegar el Portal del Cliente y como se conectan los modulos entre si.

## Mapa rapido del portal

- Dashboard: resumen general del tenant y accesos rapidos.
- Agents: crear y configurar agentes de IA.
- Inbox: gestion de Email con revision humana.
- WhatsApp: numeros, conversaciones y panel de mensajes.
- Voice Agents: agentes de voz y numeros telefonicos (Twilio).
- Web Chat: conversaciones del widget web.
- Integrations: claves externas (OpenAI, Google, Twilio, Gmail, etc.).
- Tools: funciones y webhooks para que los agentes ejecuten acciones.
- Documents: base de conocimiento para RAG.
- SQL Tables: tablas de datos internas para consultas SQL.
- Contacts: contactos y leads.
- Analytics: metricas generales.
- Team: usuarios y roles.
- Settings: ajustes generales, categorias, Gmail, API keys y billing.
- Notifications: alertas del sistema y canales.
- Onboarding/Plan: seleccion de plan.

## Flujo general recomendado

1. Configurar Integrations (OpenAI/Google/Twilio).
2. Crear Agents y activar canales.
3. Conectar Inbox (Gmail/Outlook/SMTP).
4. Conectar WhatsApp y Voice Agents (Twilio).
5. Subir Documents y/o crear SQL Tables.
6. Crear Tools si se requieren acciones externas.
7. Probar Agents y revisar Analytics.

## Convenciones

- La UI usa etiquetas en ingles. En estos manuales se mantienen tal cual.
- Los pasos se describen como rutas dentro del portal.
- Cuando un modulo requiere integraciones externas se indica en requisitos.

## Ilustraciones sugeridas

- Captura del Sidebar con todos los modulos.
- Diagrama simple del flujo: Integrations -> Agents -> Channels.

