# Inbox (Email)

## Objetivo

Gestionar emails entrantes y salientes con IA y aprobacion humana (human-in-the-loop).

## Acceso

Sidebar -> Inbox
Rutas:

- /app/{tenant}/inbox (vista principal)
- /app/{tenant}/inbox/all (todas las cuentas)
- /app/{tenant}/inbox/{credentialId} (una cuenta)
- /app/{tenant}/inbox/message/{id} (detalle del email)

## Roles

- owner, admin, agent

## Requisitos previos

- Al menos un agent con canal Email habilitado.
- Una cuenta de Email conectada (Gmail/Outlook OAuth o SMTP/IMAP).
- Integrations con OpenAI o Google si el plan no incluye modelos.

## Conectar una cuenta de email

En Inbox, pulsa Connect Email Account (o Email Accounts).

Opciones:

1) Gmail/Workspace (OAuth)
2) Outlook / Microsoft 365 (OAuth)
3) Custom SMTP/IMAP

### Gmail (OAuth)

Pasos:

1. En el panel de Email Accounts, elige Gmail.
2. Selecciona un agent en Assign agent.
3. Pulsa Connect Gmail (OAuth).
4. Completa el flujo de Google y vuelve al portal.

### Outlook (OAuth)

Pasos:

1. En el panel de Email Accounts, elige Outlook.
2. Selecciona un agent en Assign agent.
3. Pulsa Connect Outlook (OAuth).
4. Completa el flujo de Microsoft y vuelve al portal.

### SMTP/IMAP (Custom)

Pasos:

1. Pulsa Add via SMTP/IMAP.
2. Completa Account Information y SMTP Settings.
3. (Opcional) Completa IMAP Settings para emails entrantes.
4. Pulsa Add Account.

Campos: Account Information

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Email Address | Si | email valido | support@acme.com | Cuenta conectada |
| Display Name | No | texto | Acme Support | Nombre visible |
| Signature | No | texto largo | Regards, Acme | Firma de la cuenta |
| Auto-Reply Language | Si | codigo idioma o auto | auto | Auto = espejo del remitente |
| Assign agent | Si | seleccion | Support Agent | Requerido para IA |
| Generate AI Responses | No | checkbox | ON/OFF | Crea borradores IA |

Campos: SMTP Settings (Outbound - Required)

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| SMTP Host | Si | hostname | smtp.gmail.com | - |
| Port | Si | numero | 587 | - |
| SMTP Username | Si | texto | user@acme.com | - |
| SMTP Password | Si | texto | ******** | - |
| Use TLS/SSL | No | checkbox | ON | Recomendado |

Campos: IMAP Settings (Inbound - Optional)

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| IMAP Host | No | hostname | imap.gmail.com | Requerido para recibir |
| Port | No | numero | 993 | - |
| IMAP Username | No | texto | user@acme.com | - |
| IMAP Password | No | texto | ******** | - |
| Use TLS/SSL | No | checkbox | ON | Recomendado |

## Gestionar cuentas conectadas

En la lista de cuentas puedes:

- Verify: prueba conectividad.
- Test email: envia correo de prueba.
- Toggle Active/Inactive.
- Assign Agent.
- Delete.
- Edit (abre Email Configuration).

## Email Configuration (por cuenta)

Ruta rapida: Inbox -> card de cuenta -> Edit

### Account Configuration

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| From Name | No | texto | Helios Support | Nombre remitente |
| Assigned Agent | Si | seleccion | Support Agent | Necesario para IA |
| Account Signature | No | texto largo | Regards, {agent_name} | Se aplica al enviar |

Variables de firma disponibles:

- {sender_name}
- {agent_name}
- {tenant_name}
- {account_email}
- {sender_role}

### AI Response Settings

- Generate AI Responses: crea borradores.
- Send Automatically: envia sin aprobacion.
- Agent Signature: firma del agent.
- Auto-Reply Language: idioma de respuestas auto.
- Require Manual Review For: High / Urgent.
- Auto-Reply Guard: reglas de bloqueo por tokens, dominios y headers.

Campos clave (Auto-Reply Guard):

| Campo | Uso | Ejemplo |
| --- | --- | --- |
| Additional blocked sender tokens | Bloquea remitentes con tokens | noreply, billing |
| Additional blocked domains | Bloquea dominios | noreply.company.com |
| Allowed reply domains | Solo responder a dominios | yourcompany.com |
| Block headers | Bloquea por headers | List-Unsubscribe |

### Email Categorization

- Lista de categorias activas.
- Enable dynamic categories.
- Enable Other category.
- Sync categories to Gmail labels / Outlook categories.
- Archive on label sync (solo Gmail).

### Daily Summary Email

Configura un resumen diario de actividad.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Enable Daily Summary | No | checkbox | ON | Activa resumen |
| Send Time | Si (si habilitado) | HH:MM | 08:00 | Hora local |
| Timezone | Si (si habilitado) | timezone | America/Bogota | - |

## Bandeja de entrada (lista de emails)

Funciones principales:

- Search: busca por remitente, asunto, agent, categoria.
- Account filter: filtra por cuenta.
- Direction: inbound / outbound.
- Status: pending, ready_for_review, approved, sent, reviewed, failed, quota_exceeded.
- Agent filter: all, unassigned, o un agent.
- Category filter: all, uncategorized, not_analyzed, o una categoria.
- Sort: Date o Category.
- Sync: (solo en vista de una cuenta) fuerza sincronizacion.

## Detalle del email

Ruta: /app/{tenant}/inbox/message/{id}

Secciones principales:

1) Subject
2) Summary (Generate/Refresh summary)
3) AI-Generated Response (editable)
4) Original Message
5) Metadata (Received, Assigned agent, Send using, Signature)
6) Analysis (Intent, Sentiment, Category, Tags)

Acciones:

- Regenerate Response
- No Reply Needed
- Approve & Send
- Refresh summary / analysis
- Reassign agent
- Elegir cuenta de envio (Send using)
- Elegir firma (My / Agent / Account / None)

Notas importantes:

- Si Auto-reply blocked, el sistema desactiva IA y pide confirmacion para enviar.
- Para enviar, el campo de respuesta no debe estar vacio.

## Buenas practicas

- Asigna un agent a cada cuenta antes de activar IA.
- Usa categorias claras para clasificacion.
- Manten reglas de Auto-Reply Guard para evitar respuestas a no-reply.
- Usa firmas con variables para consistencia.

## Errores comunes

- Reconnect required en Gmail: reconecta el OAuth desde la tarjeta.
- Verify falla: revisa SMTP/IMAP y credenciales.
- AI response no aparece: revisa agent y proveedor LLM.

## Ilustraciones sugeridas

- Captura de Email Accounts con opciones Gmail/Outlook/SMTP.
- Captura del detalle del email con Summary y AI response.

