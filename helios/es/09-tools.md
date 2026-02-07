---
title: "Herramientas y funciones"
---

## Objetivo

Crear funciones que los agents puedan ejecutar (webhooks o acciones de integraciones).

## Acceso

Sidebar -> Tools
Ruta: `/app/{tenant}/tools`

## Roles

- owner, admin, agent

## Requisitos previos

- Integrations conectadas si quieres Integration Actions.

## Crear un Tool

Pulsa Create Tool.

### Tipo 1: API Request (Webhook)

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Tool Name | Si | texto | Book Appointment | Nombre visible |
| Description | No | texto | Reserva cita en CRM | Ayuda al agent |
| API URL | Si | URL | `https://api.example.com/appointments` | Soporta `{variable}` |
| HTTP Method | Si | GET/POST/PUT/DELETE | POST | - |
| Authentication | No | none/bearer/basic | bearer | Opcional |
| Bearer Token | Si (si bearer) | texto | ******** | - |
| Basic Auth | Si (si basic) | user/pass | user / pass | - |
| Headers | No | key/value | Authorization | Usa `{variable}` |
| Query Params | No | key/value | status=active | Usa `{variable}` |
| Body (JSON) | No | JSON | `{"id":"{contactId}"}` | Valido JSON |
| Parameters Schema | No | JSON schema | `{"type":"object"...}` | Describe args |

Notas:

- Si Body esta vacio, se envia el payload del tool como JSON.
- Usa `{variable}` para insertar argumentos del tool.

### Tipo 2: Integration Action

Pasos:

1. Selecciona la integracion (Google Calendar, Gmail, etc.).
2. Elige modo:
   - Quick Add Multiple: seleccion multiple.
   - Add Single (Custom): personaliza nombre/descripcion.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Integration | Si | seleccion | Google Calendar | Debe estar conectada |
| Action | Si | seleccion | Create event | Segun catalogo |
| Tool Name | Si (custom) | texto | Create Meeting | Editable |
| Description | No | texto | Crea evento | Editable |

## Ver Tools

En la lista puedes:

- Ver descripcion.
- Abrir Parameters y Details.
- Delete tool.

## Buenas practicas

- Usa nombres accionables (Create Ticket, Update Order).
- Define Parameters Schema para evitar errores en ejecucion.
- Documenta ejemplos en Description si es posible.

## Relacionados

- 08-integrations.md
- 03-agents.md (seleccion de tools)

## Ilustraciones sugeridas

### Crear Herramienta (API Request)
![Crear Herramienta](../../images/helios/es/tools/tool-create-modal.png)

