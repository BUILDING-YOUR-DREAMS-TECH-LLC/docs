---
title: "Chat web"
---

## Objetivo

Gestionar conversaciones del chat web embebido en sitios web.

## Acceso

Sidebar -> Web Chat
Ruta: /app/{tenant}/conversations

## Roles

- owner, admin, agent

## Requisitos previos

- Un agent con canal Web Chat habilitado.
- Widget instalado en tu sitio (ver web chat widget).

## Lista de conversaciones

En la vista principal puedes:

- Filtrar por status: active, closed, archived.
- Abrir una conversacion con View.

Datos mostrados:

- Nombre del visitante (o Anonymous Visitor)
- Email o visitor_id
- Agent asignado
- Fecha y hora

## Detalle de conversacion

Ruta: /app/{tenant}/conversations/{id}

Acciones:

- Enviar mensaje (input + Send)
- Transfer to Human
- Close (si status active)
- Archive (si status closed)

Notas:

- El panel se actualiza cada pocos segundos.
- Los mensajes muestran si usaron RAG o SQL.

## Buenas practicas

- Usa Transfer to Human cuando el usuario lo solicite.
- Cierra la conversacion cuando el tema esta resuelto.

## Relacionados

- 23-web-chat-widget.md (instalacion del widget)

## Ilustraciones sugeridas

### Lista de Conversaciones
![Lista de Conversaciones](../../images/helios/es/web-chat/web-chat-list.png)

### Detalle de Conversación
![Detalle de Conversación](../../images/helios/es/web-chat/web-chat-detail.png)

