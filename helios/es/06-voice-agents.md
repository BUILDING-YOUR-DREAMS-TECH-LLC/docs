---
title: "Agentes de voz"
---

## Objetivo

Configurar agentes de voz con numeros telefonicos (Twilio) y analizar llamadas.

## Acceso

Sidebar -> Voice Agents
Ruta: /app/{tenant}/voice-agents

## Roles

- owner, admin, agent

## Requisitos previos

- Integrations: Twilio conectado.
- Agents: un agent base con canal Voice habilitado y modelo compatible realtime.
- Integrations: OpenAI para analytics (transcription/summary/sentiment).
- Integrations: ElevenLabs si quieres voz TTS externa.

## Crear un Voice Agent

En Voice Agents, pulsa Create Voice Agent.

El modal tiene 3 pasos:

### Paso 1: Select Base Agent

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Base Agent | Si | seleccion | Support Agent | Debe tener Voice habilitado |

### Paso 2: Voice Configuration

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Voice Provider | Si | OpenAI o ElevenLabs | OpenAI | ElevenLabs requiere key |
| Primary Language | Si | codigo idioma | es | Afecta pronunciacion |
| Initial Greeting | No | texto | Hola, en que puedo ayudarte | Se reproduce al iniciar |
| Voice (OpenAI) | Si | seleccion | alloy | Algunas voces no tienen preview |
| Voice ID (ElevenLabs) | Si | texto | UOIqAnmS... | Desde ElevenLabs |

Call Analytics (si OpenAI conectado):

- Transcription (enable)
- AI Summary (enable)
- Sentiment Analysis (enable)
- Call Recording (enable, requiere Twilio)

Call Termination:

- Enable End Call (ON/OFF)
- End Call Prompt (texto largo)
- Inactivity Timeout (segundos, 5-60)

### Paso 3: Phone Number (Twilio)

Opciones:

- Guardar Twilio SID/Auth Token si no esta conectado.
- Select an existing Twilio number (dropdown).
- Phone Number manual (formato +E.164).

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Twilio Account SID | Si (si no conectado) | AC... | ACxxxx | Integrations |
| Twilio Auth Token | Si (si no conectado) | 32 chars | ******** | Integrations |
| Phone Number | Si | +E.164 | +15551234567 | Numero Twilio |

## Gestionar Voice Agents

En cada card:

- Toggle Active/Inactive.
- Edit.
- Delete.

## Llamadas (Calls)

Rutas:

- /app/{tenant}/voice-agents/calls (lista)
- /app/{tenant}/voice-agents/calls/{callId} (detalle)

Datos mostrados:

- Direction (inbound/outbound)
- From / To
- Agent
- Duration
- Status
- Sentiment
- Fecha y hora

## Buenas practicas

- Usa un agent base con prompt claro y breve.
- Define un Initial Greeting corto.
- Activa Inactivity Timeout como respaldo.
- Si usas ElevenLabs, valida que el Voice ID sea correcto.

## Errores comunes

- No aparece el agent base: el agent no tiene Voice habilitado o modelo no es realtime.
- No aparecen numeros: Twilio no conectado.
- Analytics no funcionan: OpenAI no conectado.

## Relacionados

- 22-twilio-setup.md
- 08-integrations.md
- 03-agents.md

## Ilustraciones sugeridas

- Captura del modal Step 2 (Voice Configuration).
- Captura de la lista de llamadas.
