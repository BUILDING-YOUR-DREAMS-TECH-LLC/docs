---
title: "Documentos"
---

## Objetivo

Gestionar documentos para RAG (knowledge base) usados por los agents.

## Acceso

Sidebar -> Documents
Ruta: /app/{tenant}/documents

## Roles

- owner, admin, agent

## Requisitos previos

- Integrations: Google AI API Key (requerido para Google File Search).
- Email verificado: requerido para subir documentos.

## Subir un documento (Upload Document)

Paso a paso:

1. Pulsa Upload Document.
2. Arrastra o selecciona un archivo.
3. Completa los campos.
4. Pulsa Upload Document.

Tipos soportados:

- PDF, TXT, MD, DOCX
- Max 10 MB

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Document File | Si | archivo | FAQ.pdf | Max 10 MB |
| Display Name | No | texto | FAQ Helios ES | Nombre visible |
| Description | No | texto | Use this doc for privacy | Indica cuando usar |
| Document Type | Si | seleccion | general | Ajusta chunking |

Document Type y uso:

- general: balanceado
- legal: chunks pequenos
- technical: chunks mas grandes
- faq: chunks muy pequenos

## Estados del documento

- Ready
- Processing
- Failed (ver error)

## Eliminar documento

En la lista, pulsa el icono de delete y confirma.

## Buenas practicas

- Usa nombres claros y consistentes.
- Define Description para guiar al agent.
- Divide documentos largos por tema.

## Relacionados

- 03-agents.md (RAG)