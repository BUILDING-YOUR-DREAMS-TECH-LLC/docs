---
title: "Equipo"
---

## Objetivo

Administrar usuarios, roles e invitaciones del tenant.

## Acceso

Sidebar -> Team
Ruta: /app/{tenant}/team

## Roles

- owner, admin (gestion completa)
- agent, viewer (solo lectura)

## Invitar un miembro

1. Pulsa Invite Team Member.
2. Completa Email y Role.
3. Pulsa Send Invitation.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Email Address | Si | email valido | user@acme.com | - |
| Role | Si | admin/agent/viewer | agent | Control de permisos |

## Cambiar rol de un usuario

1. En la tabla, abre Actions (menu).
2. Selecciona el nuevo rol.
3. Confirma.

## Activar / desactivar usuario

1. En la tabla, abre Actions.
2. Pulsa Deactivate User o Activate User.
3. Confirma.

Notas:

- No puedes modificar tu propio usuario.
- El rol owner es fijo.

## Invitaciones pendientes

- Se listan en Pending Invitations.
- Muestra email, rol, invitado por, expiracion.

## Buenas practicas

- Usa viewer para acceso de solo lectura.
- Desactiva usuarios que no requieran acceso.

## Ilustraciones sugeridas

### Miembros del Equipo
![Miembros del Equipo](../../images/helios/es/team/team-members-list.png)

