---
title: "Configuración de Twilio (WhatsApp + Voz)"
---

## Objetivo

Guiar la configuracion basica de Twilio para WhatsApp y Voice en Helios.

## Requisitos

- Cuenta Twilio activa
- Acceso a Twilio Console

## Datos que necesitas

- Account SID
- Auth Token
- Numero WhatsApp (sandbox o productivo)
- Numero telefonico (voice)

## Paso 1: Crear cuenta y obtener credenciales

1. Entra a https://www.twilio.com/try-twilio
2. Completa el registro y verifica telefono.
3. En el Dashboard copia:
   - Account SID (empieza con AC)
   - Auth Token (32 chars)

## Paso 2: Guardar Twilio en Helios

1. Ve a /app/{tenant}/integrations.
2. En Twilio (Voice & WhatsApp) pega Account SID y Auth Token.
3. Pulsa Save Twilio Credentials.

## Paso 3: WhatsApp (sandbox o produccion)

### Sandbox (pruebas)

1. En Twilio Console: Messaging -> Try it out -> Send a WhatsApp message.
2. Conecta tu numero personal siguiendo el codigo del sandbox.
3. Copia el WhatsApp Sandbox Number.

### Produccion

1. En Twilio Console: Messaging -> Senders -> WhatsApp Senders.
2. Solicita acceso y completa verificacion.
3. Una vez aprobado, usa tu numero productivo.

### Webhook de WhatsApp

Configura el webhook en Twilio:

- URL: https://TU_DOMINIO.com/api/whatsapp/webhook
- Method: POST

## Paso 4: Voice (telefonia)

1. Compra o usa un numero en Twilio -> Phone Numbers.
2. En la configuracion del numero:
   - Voice webhook URL: https://TU_DOMINIO.com/api/voice/webhook
   - Method: POST
   - (Opcional) Status callback: https://TU_DOMINIO.com/api/voice/status-callback

## Paso 5: Conectar numero en Helios

- WhatsApp: /app/{tenant}/whatsapp -> Connect New Number
- Voice: /app/{tenant}/voice-agents -> Create Voice Agent

## Buenas practicas

- Usa un numero separado para pruebas y produccion.
- Verifica que los webhooks respondan 200.
- Revisa logs si no llegan mensajes o llamadas.

## Errores comunes

- Webhook no llega: URL incorrecta o sin HTTPS.
- Invalid signature: revisa Auth Token guardado.
- Numero no aparece: revisa que este activo en Twilio.