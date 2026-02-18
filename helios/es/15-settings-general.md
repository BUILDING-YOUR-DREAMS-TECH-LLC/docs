---
title: "Configuración (General)"
---

## Objetivo

Configurar datos generales del tenant y revisar limites de plan.

## Acceso

Sidebar -> Settings
Ruta: /app/{tenant}/settings

## Roles

- owner, admin

## General Settings

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Organization Name | Si | texto | Acme Inc. | Nombre visible |
| Timezone | Si | timezone | America/Bogota | Afecta fechas |
| Language | Si | idioma | es | Idioma por defecto |

Acciones:

- Save Changes

## Plan & Usage (resumen)

La pagina muestra:

- Plan actual y limites.
- Uso de usuarios, agents, documents, email accounts, webhooks y mensajes.
- Acceso a Billing.

## Buenas practicas

- Ajusta Timezone antes de configurar reportes.
- Revisa limites si algun modulo falla por cuota.

## Relacionados

- [19-billing-usage.md](./19-billing-usage.md)
- [18-settings-api-keys.md](./18-settings-api-keys.md)