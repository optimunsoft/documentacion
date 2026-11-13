---
title: Usuarios
description: Gestión de usuarios en Control de acceso de Zoe Nube, disponible solo para administradores. Cubre la ubicación del menú, el modelo de acceso por rol y por empresa, la tabla de usuarios con sus asignaciones de empresa y rol, la creación de un usuario con contraseña temporal compleja y de un solo uso, el código de cuenta de 8 dígitos, el primer inicio de sesión con cambio obligatorio de contraseña, la edición de usuarios, el restablecimiento de contraseña y la eliminación de usuarios con su huella de auditoría.
module: control-de-acceso
category: administracion
slug: usuarios
order: 1
tags: [control de acceso, usuarios, roles y permisos, administrador, codigo de cuenta, contraseña temporal, auditoria, permisos por empresa, creacion masiva, edicion sincronizada, subusuario, crear usuario, editar usuario, restablecer contraseña, eliminar usuario, primer inicio de sesion, cambio de contraseña, nombre de usuario, empresas asignadas, trazabilidad]
draft: false
rag_exclude: false
last_updated: 2026-11-11
---

# Usuarios

Control de acceso es la parte de Zoe Nube donde el administrador decide quién entra a sus empresas y con qué permisos. La opción **Usuarios** lista a las personas de su equipo (subusuarios), permite crearlas y administrarlas, y muestra a qué empresas pertenece cada una y con qué rol. Los roles y sus permisos se configuran en [Roles y permisos](roles-y-permisos.md). Este documento describe la pantalla, el modelo de acceso, la creación de usuarios, el código de cuenta, el primer inicio de sesión y las acciones de editar, restablecer contraseña y eliminar.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Restricción de acceso](#restricción-de-acceso)
3. [Arquitectura general del control de acceso](#arquitectura-general-del-control-de-acceso)
4. [Elementos de la pantalla de Usuarios](#elementos-de-la-pantalla-de-usuarios)
5. [Crear un usuario](#crear-un-usuario)
6. [Contraseña temporal, identidad personal y auditoría](#contraseña-temporal-identidad-personal-y-auditoría)
7. [Código de cuenta](#código-de-cuenta)
8. [Primer inicio de sesión del usuario](#primer-inicio-de-sesión-del-usuario)
9. [Editar un usuario](#editar-un-usuario)
10. [Restablecer la contraseña](#restablecer-la-contraseña)
11. [Eliminar un usuario](#eliminar-un-usuario)
12. [Errores frecuentes](#errores-frecuentes)
13. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
14. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Control de acceso > Usuarios`.
- **Ubicación del menú:** en el menú lateral principal (sidebar), junto a **Inicio** y **Mis Empresas**. Es independiente del módulo de Contabilidad: no se necesita entrar a una empresa para usarlo.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `INICIO / CONTROL DE ACCESO / USUARIOS`.
- **Título de la pantalla:** «Usuarios», con el subtítulo «Gestiona y administra tus usuarios y colaboradores».
- Al abrir **Control de acceso** en el menú se despliegan dos opciones: **Usuarios** y **Roles y permisos**.

---

## Restricción de acceso

- Control de acceso está **disponible únicamente para usuarios con perfil de administrador**.
- Un subusuario que inicia sesión solo ve **Inicio** y **Mis Empresas** en el menú lateral; **Control de acceso** no aparece.
- En el encabezado de Zoe, el administrador figura con el rol «Administrador» y el subusuario con el rol «Subusuario».

---

## Arquitectura general del control de acceso

| Principio | Descripción |
| :--- | :--- |
| Acceso mediante rol | Todo acceso de un subusuario a una empresa se hace obligatoriamente a través de un **Rol**, que agrupa un conjunto específico de **Permisos**. |
| Permisos por empresa | Los roles y permisos se configuran y se evalúan de forma independiente por cada empresa. Una misma persona puede tener un rol distinto en cada empresa. |
| Protección del sistema | Las acciones críticas de los módulos están protegidas por permisos nativos definidos por la plataforma. Si un subusuario no tiene el permiso requerido, el sistema le impide ejecutar la acción de manera definitiva. |
| Reflejo inmediato | Los cambios que el administrador hace sobre roles y permisos se aplican de forma automática e instantánea a los usuarios asociados a ese rol. |

---

## Elementos de la pantalla de Usuarios

| Elemento | Función |
| :--- | :--- |
| Campo de búsqueda («Buscar por usuario, nombre o apellido») y botón **Filtrar** | Filtra la lista de usuarios. |
| **Listado de usuarios** y contador de registros | Título de la tabla y número de usuarios. |
| **Código de cuenta** | Muestra el código de 8 dígitos de la cuenta del administrador. Ver [Código de cuenta](#código-de-cuenta). |
| **Crear usuario** | Abre la ventana «Nuevo usuario». Atajo de teclado: **Alt + N**. |
| **Columnas** | Selector para elegir qué columnas muestra la tabla. |
| Paginación y «7 por página» | Navegación entre páginas de la tabla. |

Columnas de la tabla:

| Columna | Qué muestra |
| :--- | :--- |
| ID | Número de la fila. |
| Usuario | Nombre de usuario con el que la persona inicia sesión. |
| Nombre | Nombres y apellidos. |
| Asignaciones | Cada empresa a la que el usuario tiene acceso y su rol en ella, con el formato `EMPRESA - ROL`, por ejemplo `MI TIERRITA S.A.S - CONTADOR`. |
| Acciones | Tres íconos: **editar** (lápiz), **restablecer contraseña** (dos flechas circulares) y **eliminar** (papelera). |

Cuando no hay usuarios, la tabla muestra «Sin registros».

---

## Crear un usuario

1. Hacer clic en **Crear usuario**. Se abre la ventana **Nuevo usuario** («Registra un nuevo usuario en el sistema»).
2. Completar los datos de la persona (tabla siguiente).
3. En **Empresas asignadas**, elegir la **empresa** y luego su **rol**. La lista de roles muestra los de la empresa elegida; mientras no hay empresa elegida el selector de rol dice «No hay roles para esta empresa». La fila inferior permite sumar otra empresa con su propio rol, y el ícono de papelera rojo quita una asignación.
4. Hacer clic en **Crear**. Zoe muestra el mensaje «Operación exitosa — Usuario creado correctamente» y la ventana **Contraseña del usuario**.
5. Copiar las credenciales antes de cerrar la ventana y entregarlas a la persona.

| Campo | Obligatorio | Descripción |
| :--- | :--- | :--- |
| Nombre de usuario | Sí | Nombre con el que la persona inicia sesión. Debe ser personal. |
| Municipio | Sí | Municipio de la persona, elegido de una lista (por ejemplo «Bucarasica - Norte de Santander»). |
| Nombres | Sí | Nombres de la persona. |
| Apellidos | Sí | Apellidos de la persona. |
| Empresas asignadas | Sí | Empresa y rol del usuario. El botón **Crear rol** de esta sección permite crear un rol sin salir de la ventana. |

La ventana **Contraseña del usuario** muestra una tabla con tres filas:

| Fila | Contenido |
| :--- | :--- |
| Usuario | Nombre de usuario creado. |
| Código de cuenta | Código de 8 dígitos de la cuenta del administrador, con ícono para copiar. |
| Contraseña | Contraseña temporal generada, con ícono para copiar. |

El aviso de la ventana indica que, por motivos de seguridad, las credenciales **no se volverán a mostrar después de cerrar la ventana**.

---

## Contraseña temporal, identidad personal y auditoría

- **Contraseña temporal compleja y de un solo uso:** al crear un usuario, el sistema genera una contraseña temporal compleja. El usuario debe cambiarla en su primer inicio de sesión.
- **Cambio obligatorio:** en el primer inicio de sesión, el sistema obliga al usuario a cambiar la contraseña temporal antes de continuar. Ver [Primer inicio de sesión](#primer-inicio-de-sesión-del-usuario).
- **Identidad personal:** el usuario debe ser estrictamente personal. No se comparte un mismo usuario entre varias personas.
- **Auditoría y trazabilidad:** el sistema registra rigurosamente la trazabilidad de cada cambio de datos a nombre del usuario que lo ejecutó. Compartir un usuario impide saber quién hizo cada cambio.
- **Contraseña perdida:** si se cierra la ventana sin copiar la contraseña, no se puede volver a ver; hay que [restablecerla](#restablecer-la-contraseña).

---

## Código de cuenta

- Cada **usuario administrador** posee un **código único de 8 dígitos**, asignado por el sistema al crearse.
- El código **sirve para diferenciar cuentas dentro del sistema**.
- Se ve en la parte superior de `Control de acceso > Usuarios` (recuadro «Código de cuenta») y en la ventana «Contraseña del usuario» de cada usuario que se crea o cuya contraseña se restablece.
- Los subusuarios lo necesitan para iniciar sesión: la pantalla de ingreso, en la pestaña **Usuario**, pide **Código de cuenta**, **Nombre de usuario** y **Contraseña**. El texto de ayuda del campo dice «8 dígitos. Te lo comparte el administrador de la cuenta.»

---

## Primer inicio de sesión del usuario

1. En la pantalla **Ingresa a tu cuenta**, elegir la pestaña **Usuario** (la otra pestaña es **Administrador**).
2. Escribir el **Código de cuenta**, el **Nombre de usuario** y la **Contraseña** temporal, y hacer clic en **Ingresar**.
3. Zoe abre la pantalla **Cambiar contraseña** («Antes de continuar debes cambiar tu contraseña») con el campo **Nueva contraseña**.
4. La contraseña nueva debe cumplir cinco requisitos, que se marcan en verde al cumplirse:

| Requisito |
| :--- |
| Al menos 8 caracteres |
| Al menos 1 número |
| Al menos 1 letra minúscula |
| Al menos 1 letra mayúscula |
| Al menos 1 carácter especial |

5. Hacer clic en **Continuar** (o **Cerrar sesión** para salir). Zoe muestra «Operación exitosa — Se ha cambiado la contraseña» y la pantalla **Selección de Empresa**, solo con las empresas asignadas al usuario.
6. Al entrar a una empresa, el usuario trabaja en ella con los permisos de su rol.

---

## Editar un usuario

1. En la tabla, hacer clic en el lápiz de la fila del usuario. Se abre la ventana **Editar usuario** («Modifica los datos y permisos del usuario»).
2. Se pueden cambiar el **Municipio**, los **Nombres**, los **Apellidos** y las **Empresas asignadas** (empresa y rol). El **Nombre de usuario** aparece deshabilitado (en gris).
3. Hacer clic en **Actualizar**. Zoe muestra «Operación exitosa — Usuario actualizado correctamente» y la columna **Asignaciones** refleja el cambio.

Si se cambia el rol de un usuario, sus permisos en esa empresa cambian de inmediato.

---

## Restablecer la contraseña

Si un usuario olvida su contraseña, debe pedirle al administrador que genere una nueva clave temporal. El usuario tendrá que repetir el ciclo de cambio de contraseña en su próximo inicio de sesión.

1. En la fila del usuario, hacer clic en el ícono de restablecer (dos flechas circulares). Se abre la ventana **¿Estás seguro?** con el texto «La contraseña del usuario `<usuario>` será restablecida, al iniciar sesión deberás cambiarla».
2. Escribir el **Nombre de usuario** en el campo de confirmación. Zoe muestra el aviso «Información importante: para restablecer la contraseña necesitamos estar seguros de que quieres restablecerla escribiendo su nombre de usuario».
3. Hacer clic en **Sí, restablecer** (o **Cancelar**).
4. Zoe muestra «Operación exitosa — Contraseña restablecida correctamente» y la ventana **Contraseña del usuario** con el usuario, el código de cuenta y la nueva contraseña temporal. Se copian y se entregan a la persona antes de cerrar la ventana: no se vuelven a mostrar.

---

## Eliminar un usuario

1. En la fila del usuario, hacer clic en la papelera. Se abre la ventana **¿Estás seguro?** con el texto «El usuario `<usuario>` será eliminado de forma permanente. Esta acción no se puede deshacer.»
2. Escribir el **Nombre de usuario** en el campo de confirmación.
3. Leer el aviso: «Su huella en la aplicación seguirá apareciendo para efectos de auditoría, por este mismo motivo no podrás volver a utilizar este nombre de usuario.»
4. Hacer clic en **Sí, eliminar** (o **Cancelar**). Zoe muestra «Operación exitosa — Usuario eliminado correctamente» y el usuario desaparece de la tabla.

---

## Errores frecuentes

### No aparece Control de acceso en el menú
- **Causa:** la opción es exclusiva de los usuarios administradores y se está usando una cuenta de subusuario.
- **Solución:** iniciar sesión con el usuario administrador, en la pestaña **Administrador** de la pantalla de ingreso.

### El usuario no puede iniciar sesión
- **Causa:** no está usando la pestaña **Usuario**, o falta el código de cuenta de 8 dígitos, o la contraseña es incorrecta.
- **Solución:** confirmar que ingresa por la pestaña **Usuario** con el código de cuenta, su nombre de usuario y la contraseña. Si la perdió, restablecerla desde la tabla.

### Se cerró la ventana sin copiar la contraseña
- **Causa:** las credenciales no se vuelven a mostrar después de cerrar la ventana «Contraseña del usuario».
- **Solución:** restablecer la contraseña del usuario y entregar la nueva.

### El selector de rol dice «No hay roles para esta empresa»
- **Causa:** la empresa elegida todavía no tiene roles, o no se ha elegido empresa.
- **Solución:** elegir primero la empresa; si no tiene roles, crearlos en `Control de acceso > Roles y permisos` o con el botón **Crear rol** de la ventana de usuario.

---

## Resumen de reglas de negocio

| # | Regla de negocio |
| :--- | :--- |
| 1 | Control de acceso solo está disponible para usuarios administradores; no aparece en el menú de los subusuarios. |
| 2 | Todo acceso de un subusuario a una empresa se hace a través de un rol, que agrupa permisos. |
| 3 | Los roles y permisos se configuran y evalúan por empresa. |
| 4 | Sin el permiso requerido, el sistema impide la acción de manera definitiva. |
| 5 | Los cambios en roles y permisos se aplican de inmediato a los usuarios con ese rol. |
| 6 | Al crear un usuario, el sistema genera una contraseña temporal compleja que no se vuelve a mostrar al cerrar la ventana. |
| 7 | En el primer inicio de sesión, el usuario debe cambiar la contraseña temporal; la nueva exige 8 caracteres, un número, una minúscula, una mayúscula y un carácter especial. |
| 8 | El usuario debe ser personal: el sistema registra la trazabilidad de cada cambio a nombre de quien lo ejecutó. |
| 9 | El administrador tiene un código de cuenta único de 8 dígitos que diferencia las cuentas y que los subusuarios usan para iniciar sesión. |
| 10 | Un usuario que olvida su contraseña pide al administrador una nueva clave temporal y debe cambiarla en su siguiente inicio de sesión. |
| 11 | Restablecer o eliminar un usuario exige escribir su nombre de usuario como confirmación. |
| 12 | Eliminar un usuario es permanente; su huella queda para auditoría y su nombre de usuario no se puede reutilizar. |
| 13 | El nombre de usuario no se modifica al editar un usuario. |

---

## Preguntas frecuentes

**¿Quién puede ver Control de acceso?**
Solo los usuarios administradores. En el menú lateral aparece junto a Inicio y Mis Empresas.

**¿Cómo le doy acceso a una empresa a una persona de mi equipo?**
Con `Control de acceso > Usuarios > Crear usuario`: se completan sus datos y en **Empresas asignadas** se elige la empresa y el rol que cumplirá en ella.

**¿Puede una persona tener acceso a varias empresas con roles distintos?**
Sí. Se agrega una asignación por cada empresa, cada una con su propio rol, porque los roles y permisos se evalúan por empresa.

**¿Qué hago si un usuario olvidó su contraseña?**
Pedirle al administrador que la restablezca desde `Control de acceso > Usuarios` (ícono de las dos flechas circulares). El usuario recibe una nueva clave temporal y debe cambiarla al entrar.

**¿Para qué sirve el código de cuenta?**
Diferencia las cuentas dentro del sistema. Los subusuarios lo escriben, junto con su nombre de usuario y contraseña, en la pestaña **Usuario** de la pantalla de ingreso.

**¿Puedo volver a ver la contraseña temporal?**
No. Solo se muestra en la ventana «Contraseña del usuario». Si se cerró sin copiarla, hay que restablecer la contraseña.

**¿Se puede reutilizar el nombre de un usuario eliminado?**
No. La huella del usuario eliminado permanece en la aplicación para efectos de auditoría y su nombre de usuario no se puede volver a utilizar.

**¿Los cambios de rol se aplican de inmediato?**
Sí. Los cambios en roles y permisos se reflejan de forma automática en los usuarios asociados a ese rol.
