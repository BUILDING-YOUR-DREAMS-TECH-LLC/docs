---
title: "Onboarding - Plan"
---

## Objetivo

Seleccionar plan durante el onboarding del tenant.

## Acceso

Ruta: /app/{tenant}/onboarding/plan

## Roles

- owner, admin

## Flujo

1. Se muestra PlanSelector con planes disponibles.
2. Elige el plan deseado.
3. Si requiere pago, completa el flujo de Stripe.

## Datos mostrados

- Plan name, descripcion y precio.
- Limites y features.
- Plan actual (si aplica).

## Buenas practicas

- Revisa limites antes de elegir el plan.
- Considera usar trial si esta habilitado.

## Ilustraciones sugeridas

### Selector de Planes
![Selector de Planes](../../images/helios/es/onboarding/onboarding-plan-selector.png)

