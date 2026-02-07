---
title: "Acceso y autenticación"
---

## Objetivo

Explicar como entrar al portal, crear cuenta, aceptar invitaciones y recuperar contrasena.

## Rutas clave

- /login
- /pricing (seleccion de plan)
- /signup?plan=...
- /auth/complete?plan=...
- /forgot-password
- /reset-password
- /auth/invite/{token}

## Iniciar sesion

Pasos:

1. Ve a /login.
2. Elige una opcion:
   - Continue with Google
   - Email + Password
3. Si usas Email + Password, completa los campos y pulsa Sign in.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Email | Si | email valido | name@company.com | Se usa para autenticacion |
| Password | Si | minimo 8 caracteres | ******** | - |

## Crear cuenta (signup)

Flujo recomendado:

1. Ve a /pricing y elige un plan.
2. La pagina te lleva a /signup?plan=PLAN.
3. Completa el formulario y pulsa Create account.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Full Name | Si | texto libre | John Doe | Nombre del propietario inicial |
| Email | Si | email valido | name@company.com | Email principal |
| Company Name | Si | texto libre | Acme Inc. | Nombre del tenant |
| Subdomain | Si | minusculas, numeros y guiones | acme | Se usa para la URL del workspace |
| Password | Si | minimo 8 caracteres | ******** | - |

Notas:

- Si eliges Google OAuth, el flujo puede redirigir a /auth/complete para terminar datos del tenant.
- El subdomain debe ser unico.

## Completar cuenta (OAuth)

Si entras con Google y no existe tenant, se muestra /auth/complete.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Company Name | Si | texto libre | Acme Inc. | Nombre del tenant |
| Subdomain | Si | minusculas, numeros y guiones | acme | URL del workspace |

## Verificacion de email

Algunas acciones requieren email verificado (por ejemplo: crear agents o subir documents). Si ves un mensaje de verificacion:

1. Abre el correo de verificacion.
2. Haz click en el enlace.
3. Vuelve al portal y repite la accion.

## Invitaciones de equipo

Si recibes un enlace de invitacion:

1. Abre /auth/invite/{token}.
2. Completa el formulario para crear tu usuario.
3. Al finalizar, se abre el Dashboard del tenant.

Campos:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| Nombre Completo | Si | texto libre | Juan Perez | Debe tener al menos 2 caracteres |
| Password | Si | minimo 8 caracteres | ******** | - |
| Confirm Password | Si | igual al password | ******** | - |

## Recuperar contrasena

1. Ve a /forgot-password.
2. Escribe tu Email y pulsa Send reset link.
3. Abre el correo y entra al enlace.
4. En /reset-password define la nueva contrasena.

Campos de reset:

| Campo | Obligatorio | Formato | Ejemplo | Nota |
| --- | --- | --- | --- | --- |
| New Password | Si | minimo 8 caracteres | ******** | - |
| Confirm Password | Si | igual al password | ******** | - |

## Cerrar sesion

Usa el menu de usuario en el sidebar (o la opcion Sign out) para cerrar sesion.

## Ilustraciones sugeridas

### Login con Google y Email
![Login con Google y Email](../../images/helios/es/auth/login-form.png)
### Registro con subdominio
![Registro con subdominio](../../images/helios/es/auth/signup-form.png)
