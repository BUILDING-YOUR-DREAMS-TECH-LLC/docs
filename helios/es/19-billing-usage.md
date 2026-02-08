---
title: "Facturación y uso"
---

## Objetivo

Gestionar el plan de suscripcion y monitorear limites de uso.

## Acceso

- Billing: /app/{tenant}/settings/billing
- Usage: /app/{tenant}/usage

## Roles

- owner, admin

## Billing

La pagina muestra:

- Plan actual (nombre, descripcion, precio).
- Estado de suscripcion.
- Features incluidos.
- Usage meters (agents, users, documents, mensajes, etc.).
- Plan Selector para upgrade/downgrade.
- Customer Portal (Stripe).

Acciones:

- Manage plan: abre el selector de planes.
- Customer Portal: gestiona pago, facturas y cancelacion.

## Usage

- Muestra consumo del mes y fecha de reset.
- Incluye limites de: Agents, Users, AI Messages, Documents.

## Buenas practicas

- Revisa limites antes de habilitar mas canales.
- Si estas cerca del limite, considera upgrade.

## Relacionados

- 15-settings-general.md
- 21-onboarding-plan.md