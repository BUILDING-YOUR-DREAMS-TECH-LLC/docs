---
title: "Configuración - Categorías (Email)"
---

## Objetivo

Definir categorias para clasificacion automatica de emails.

## Acceso

Ruta: /app/{tenant}/settings/categories

## Roles

- owner, admin

## Crear categoria

1. Pulsa Add Category.
2. Completa el formulario.
3. Pulsa Save Category.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Name | Si | texto | Technical Support | Nombre de categoria |
| Description | No | texto | Issues and bugs | Contexto para IA |
| Color | No | hex | #94a3b8 | Color del badge |
| Keywords | No | texto | urgent, error, bug | Separado por comas |

## Editar categoria

- Pulsa el icono Edit en la fila.
- Ajusta campos y guarda.

## Activar / desactivar

- Usa el switch en la columna Status.

## Eliminar categoria

- Pulsa Delete y confirma.

## Buenas practicas

- Usa nombres cortos y claros.
- Define Keywords para mejorar clasificacion.


## Captura

![Configuración de Categorías](../../images/helios/es/screenshots/settings-02-categories.png)

## Relacionados

- [04-inbox-email.md](./04-inbox-email.md)