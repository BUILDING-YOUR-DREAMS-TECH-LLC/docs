---
title: "Claves API (BYOK)"
---

## Objetivo

Guardar tus propias API keys para OpenAI y Google AI.

## Acceso

Settings -> API Keys
Ruta: /app/{tenant}/settings/api-keys

## Roles

- owner, admin

## Guardar OpenAI API Key

1. En OpenAI API Key, pega tu key.
2. Pulsa Save & Verify.
3. Verifica el estado (Verified/Unverified).

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| OpenAI API Key | Si | sk-... | sk-xxxx | Se guarda cifrada |

## Guardar Google AI API Key

1. En Google AI API Key, pega tu key.
2. Pulsa Save & Verify.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Google AI API Key | Si | AIza... | AIza... | Se guarda cifrada |

## Eliminar key

- Usa el icono de trash en la key.

## Buenas practicas

- Usa keys de produccion separadas de pruebas.
- Configura limites de gasto en el proveedor.

## Relacionados

- 08-integrations.md
- 03-agents.md

## Ilustraciones sugeridas

### Estado de API Keys
![Estado de API Keys](../../images/helios/es/settings-api-keys/settings-api-keys-status.png)

