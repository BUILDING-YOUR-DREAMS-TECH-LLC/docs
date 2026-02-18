---
title: "Integraciones de Gmail"
---

## Objetivo

Conectar cuentas Gmail via OAuth para envio y recepcion de emails.

## Acceso

Settings -> Gmail
Ruta: /app/{tenant}/settings/gmail

## Roles

- owner, admin

## Conectar Gmail

1. Selecciona un agent en Assign agent.
2. Pulsa Connect Gmail.
3. Completa el OAuth de Google.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Assign agent | Si | seleccion | Support Agent | Requerido para IA |

## Gestionar cuentas

En cada cuenta:

- Go to Inbox
- Disconnect (Trash icon)
- Ver estado (Active/Expired)

## Notas

- OAuth es mas seguro que app passwords.
- Si el token expira, reconecta la cuenta.


## Captura

![Configuración de Gmail](../../images/helios/es/screenshots/settings-03-gmail.png)

## Relacionados

- [04-inbox-email.md](./04-inbox-email.md)
- [08-integrations.md](./08-integrations.md)