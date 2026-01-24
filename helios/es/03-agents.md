---
title: "Agents (AI Agents)"
---

# Agents (AI Agents)

## Objetivo

Crear y configurar asistentes de IA que operan en Email, WhatsApp, Web Chat y Voz. Cada agent define canales, capacidades y configuracion de IA.

## Acceso

Sidebar -> Agents
Ruta: /app/{tenant}/agents

## Roles

- owner, admin, agent

## Requisitos previos

- Integrations: al menos un proveedor LLM (OpenAI o Google) si tu plan no incluye modelos.
- Documents: necesarios para habilitar RAG.
- SQL Tables: necesarias para habilitar SQL.
- Tools: opcional, solo si quieres acciones externas.
- Voice: si activas voz, luego debes crear un Voice Agent con numero en el modulo Voice Agents.
- Email verificado: requerido para crear agents.

## Crear un agent (Create Agent)

Paso a paso:

1. En Agents, pulsa Create Agent.
2. Completa los 4 pasos del modal.

### Paso 1: Basic Information

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Agent Name | Si | texto libre | Customer Support Agent | Nombre visible en el portal |
| Description | No | texto libre | Responde dudas de soporte | Define tono y rol |

### Paso 2: Configure Channels

Selecciona uno o varios canales. Nota: si activas Voice, el formulario desactiva Email/WhatsApp/Web Chat en este paso.

- Email: respuestas en Inbox.
- WhatsApp: conversaciones en modulo WhatsApp.
- Web Chat: widget web.
- Voice: telefonia (requiere Voice Agents + Twilio).

### Paso 3: Agent Capabilities

Opciones:

- RAG (Google File Search)
  - Requiere Google AI API Key y documentos subidos.
  - Debes seleccionar al menos 1 document.
- SQL Database Access
  - Requiere tablas en SQL Tables.
  - Debes seleccionar al menos 1 tabla.
- Web Search
  - Permite consultas externas si tienes Bing Web Search configurado.
- Tools & Actions
  - Selecciona tools creados en Tools.

Campos y datos (RAG):

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Knowledge Base Documents | Si (si RAG activo) | seleccion multiple | FAQ.pdf | Selecciona documentos relevantes |

Campos y datos (SQL):

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Allowed Tables | Si (si SQL activo) | seleccion multiple | orders, inventory | Limita el acceso del agent |

Campos y datos (Tools):

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Tools | No | seleccion multiple | Create Ticket | Solo tools creados en Tools |

### Paso 4: AI Configuration

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Provider | Si | dropdown | OpenAI | Depende de tu plan y keys |
| Model | Si | dropdown | gpt-4o | Algunos modelos requieren BYOK |
| Temperature | Si | 0.0 - 1.0 | 0.7 | Algunos modelos fijan 1.0 |
| Max Tokens | Si | numero | 800 | Limitado por el modelo |
| Top P | Si | 0.0 - 1.0 | 1.0 | Control de sampling |
| System Prompt | No | texto largo | You are a helpful assistant | Limite de caracteres |

Acciones:

- Next para avanzar.
- Create Agent para guardar.

## Editar un agent

Ruta: /app/{tenant}/agents/{id}/edit

El formulario usa pestanas:

### Basic Info

- Agent Name
- Description

### Channels

- Email / WhatsApp / Web Chat / Voice
- Si activas Voice, puedes definir Initial Greeting (max 500 chars)

### Tools (Capabilities)

- RAG: seleccionar documentos
- SQL: seleccionar tablas
- Web Search
- Tools & Actions

### AI Config

- Model, Temperature, Max Tokens, Top P
- Timezone (opcional)
- System Prompt
- Insert tools context (inserta referencias de tools al prompt)
- Human Escalation: Detect escalation requests

Acciones:

- Save Changes para guardar.
- Cancel para volver a Agents.

## Probar un agent

Ruta: /app/{tenant}/agents/{id}/test

Funciones principales:

- Enviar mensajes de prueba.
- Ver trazas (RAG, SQL, tools).
- Probar voz si el agent tiene voice habilitado.

## Activar o desactivar un agent

En la lista de Agents, usa el toggle de estado en cada card.

## Eliminar un agent

En la card del agent, usa Delete. Confirma la accion.

## Buenas practicas

- Usa un nombre claro por caso de uso (Soporte, Ventas, Cobros).
- Habilita solo canales que vas a operar.
- Para RAG, sube documentos limpios y con nombres claros.
- Para SQL, limita las tablas a las necesarias.
- Mantener el System Prompt debajo del limite, especialmente en voice.

## Errores comunes

- No aparecen modelos: falta API key en Integrations o plan no incluye el modelo.
- RAG desactivado: falta Google key o documentos.
- SQL desactivado: no hay tablas.

## Ilustraciones sugeridas

- Captura del modal Create Agent paso 2 (Channels).
- Captura del tab AI Config con Model y System Prompt.
