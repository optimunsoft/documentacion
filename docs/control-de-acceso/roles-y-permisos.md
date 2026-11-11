---
title: Roles y permisos
description: Administración de roles y permisos por empresa en Control de acceso de Zoe Nube, disponible solo para administradores. Cubre el selector de empresa, la tabla de roles, la creación de un rol con la opción «Todas mis empresas» (creación masiva), el catálogo de permisos de Contabilidad (Puc, Tipos de asiento, Terceros, Especiales y Comprobantes), la edición con la casilla «Modificar en todas las empresas» (edición sincronizada) y la eliminación de roles.
module: control-de-acceso
category: administracion
slug: roles-y-permisos
order: 2
tags: [control de acceso, usuarios, roles y permisos, administrador, codigo de cuenta, contraseña temporal, auditoria, permisos por empresa, creacion masiva, edicion sincronizada, rol, permisos, crear rol, editar rol, eliminar rol, todas mis empresas, modificar en todas las empresas, selector de empresa, subusuario]
draft: false
rag_exclude: false
last_updated: 2026-11-11
---

# Roles y permisos

Un **rol** es un conjunto de **permisos** con un nombre. Todo acceso de un subusuario a una empresa se hace a través de un rol, y lo que el usuario puede hacer en esa empresa depende de los permisos del rol. La opción **Roles y permisos** de Control de acceso sirve para crear, editar y eliminar roles por empresa, con opciones para crearlos y editarlos en todas las empresas del administrador en una sola operación. Los usuarios y su asignación de empresa y rol se administran en [Usuarios](usuarios.md).

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Restricción de acceso](#restricción-de-acceso)
3. [Arquitectura general del control de acceso](#arquitectura-general-del-control-de-acceso)
4. [Elementos de la pantalla de Roles y permisos](#elementos-de-la-pantalla-de-roles-y-permisos)
5. [Crear un rol](#crear-un-rol)
6. [Creación global: «Todas mis empresas»](#creación-global-todas-mis-empresas)
7. [Catálogo de permisos](#catálogo-de-permisos)
8. [Editar un rol](#editar-un-rol)
9. [Edición sincronizada: «Modificar en todas las empresas»](#edición-sincronizada-modificar-en-todas-las-empresas)
10. [Eliminar un rol](#eliminar-un-rol)
11. [Errores frecuentes](#errores-frecuentes)
12. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
13. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Control de acceso > Roles y permisos`.
- **Ubicación del menú:** en el menú lateral principal (sidebar), junto a **Inicio** y **Mis Empresas**, de forma independiente al módulo de Contabilidad.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `INICIO / CONTROL DE ACCESO / ROLES Y PERMISOS`.
- **Título de la pantalla:** «Roles y Permisos», con el subtítulo «Gestiona los roles y permisos de acceso al sistema, elige qué acciones pueden realizar tus usuarios por empresa».

---

## Restricción de acceso

Control de acceso está **disponible únicamente para usuarios con perfil de administrador**. Los subusuarios no ven la opción en el menú.

---

## Arquitectura general del control de acceso

| Principio | Descripción |
| :--- | :--- |
| Acceso mediante rol | Todo acceso de un subusuario a una empresa se hace obligatoriamente a través de un **Rol**, que agrupa un conjunto específico de **Permisos**. |
| Permisos por empresa | Los permisos y roles se configuran y se evalúan de forma independiente por cada empresa. |
| Protección del sistema | Las acciones críticas de los módulos están protegidas por permisos nativos definidos por la plataforma. Si un subusuario no tiene el permiso requerido, el sistema le impide ejecutar la acción de manera definitiva. |
| Reflejo inmediato | Los cambios que el administrador hace sobre roles y permisos se aplican de forma automática e instantánea a los usuarios asociados a ese rol. |

---

## Elementos de la pantalla de Roles y permisos

| Elemento | Función |
| :--- | :--- |
| **Selector de empresa** (arriba) | Define de qué empresa se consultan y administran los roles. Es necesario tener una empresa elegida para ver la tabla; Zoe deja seleccionada una empresa al abrir la pantalla y se puede cambiar por otra de las empresas del administrador. |
| Campo de búsqueda («Buscar por nombre o descripción») y botón **Filtrar** | Filtra la lista de roles. |
| **Roles y permisos** y contador de registros | Título de la tabla y número de roles de la empresa elegida (por ejemplo «6 registros»). |
| **Crear rol** | Abre la ventana «Nuevo rol». |
| **Columnas** | Selector para elegir qué columnas muestra la tabla. |
| Paginación y «7 por página» | Navegación entre páginas de la tabla. |

Columnas de la tabla:

| Columna | Qué muestra |
| :--- | :--- |
| ID | Número de la fila. |
| Nombre | Nombre del rol (por ejemplo Auxiliar, Contador, Junior). |
| Descripción | Para qué sirve el rol (por ejemplo «Auxiliar Contable»). |
| Acciones | Dos íconos: **editar** (lápiz) y **eliminar** (papelera). |

---

## Crear un rol

1. Elegir en el selector de la parte superior la empresa con la que se trabaja.
2. Hacer clic en **Crear rol**. Se abre la ventana **Nuevo rol** («Crea un nuevo rol con permisos específicos»).
3. Completar los campos (tabla siguiente).
4. En **Permisos asignados**, marcar los permisos del rol uno a uno, o marcar **Seleccionar todos los permisos de contabilidad** para asignarlos todos. Los permisos se muestran en un árbol por grupos que se puede recorrer con la barra de desplazamiento.
5. Hacer clic en **Crear** (o **Cancelar**). Zoe muestra «Operación exitosa — Rol creado correctamente» y el rol aparece en la tabla.

| Campo | Obligatorio | Descripción |
| :--- | :--- | :--- |
| Nombre | Sí | Nombre del rol. |
| Descripción | No | Frase que explica para qué sirve el rol. |
| Crear rol para | No | Viene en **Todas mis empresas**. Se puede elegir una empresa específica de la lista. |
| Permisos asignados | Sí | Permisos del rol. |

---

## Creación global: «Todas mis empresas»

El campo **Crear rol para** ofrece la opción **Todas mis empresas** (valor por defecto) y, además, una entrada por cada empresa del administrador. Junto al campo hay un ícono de información.

- Con **Todas mis empresas**, el rol se crea de forma simultánea en todas las empresas del administrador, sin repetir la configuración empresa por empresa.
- Según el mensaje informativo del ícono: «Cuando creas un rol para todas las empresas, se crea en todas aquellas que aún no tengan un rol con el mismo nombre.» Si una empresa ya tiene un rol con ese nombre, no se crea uno nuevo en ella.
- Con una empresa específica, el rol se crea solo en esa empresa.

---

## Catálogo de permisos

Los permisos que se pueden asignar a un rol están agrupados bajo **Contabilidad**. En total hay 17:

| Grupo | Permisos |
| :--- | :--- |
| Puc | Eliminar cuentas |
| Tipos de asiento | Eliminar tipos de asiento · Editar tipo de asiento |
| Terceros | Importar terceros desde excel · Editar nit de un tercero |
| Especiales | Agregar año fiscal a periodos disponibles · Cerrar año fiscal · Cerrar mes · Mover saldos finales a iniciales · Mover saldos de una cuenta a otra cuenta · Mover saldos de un tercero a otro tercero · Remover año fiscal de periodos disponibles · Reabrir año fiscal · Reabrir mes |
| Comprobantes | Anular comprobantes · Editar comprobantes · Activar/desactivar edición de comprobante |

Cada grupo se puede contraer o expandir con la flecha de su fila. La casilla **Seleccionar todos los permisos de contabilidad** marca o desmarca todos los permisos a la vez.

---

## Editar un rol

1. Elegir en el selector de la parte superior la empresa del rol.
2. Hacer clic en el lápiz de la fila del rol. Se abre la ventana **Editar rol** («Actualiza los permisos y configuración del rol»).
3. Se pueden cambiar la **Descripción** y los **Permisos asignados**. El **Nombre** aparece deshabilitado (en gris).
4. Opcionalmente, marcar **Modificar en todas las empresas** (ver siguiente sección).
5. Hacer clic en **Actualizar** (o **Cancelar**). Zoe muestra «Operación exitosa — Rol actualizado correctamente».

Los cambios se aplican de inmediato a todos los usuarios que tienen ese rol.

---

## Edición sincronizada: «Modificar en todas las empresas»

En la ventana **Editar rol**, sobre el árbol de permisos, aparece la casilla **Modificar en todas las empresas** (desmarcada por defecto).

- Si un rol con el mismo nombre existe en varias empresas del administrador, al marcar la casilla se actualiza de manera masiva en todas ellas en una sola operación.
- Si la casilla queda sin marcar, solo se actualiza el rol de la empresa elegida en el selector.

---

## Eliminar un rol

1. En la fila del rol, hacer clic en la papelera. Se abre la ventana **¿Estás seguro?** con el texto «El rol `<nombre>` será eliminado de forma permanente. Esta acción no se puede deshacer.»
2. Hacer clic en **Sí, eliminar** (o **Cancelar**). Zoe muestra «Operación exitosa — Rol eliminado correctamente» y el contador de registros baja en uno.

Antes de eliminar un rol conviene revisar en `Control de acceso > Usuarios` qué usuarios lo tienen asignado.

---

## Errores frecuentes

### No aparece un rol que sí se creó
- **Causa:** los roles se muestran por empresa y el selector de la parte superior está en otra empresa.
- **Solución:** cambiar el selector a la empresa donde se creó el rol.

### Se creó un rol para todas las empresas y falta en alguna
- **Causa:** esa empresa ya tenía un rol con el mismo nombre; la creación global no crea roles en empresas que ya lo tienen.
- **Solución:** revisar la lista de roles de esa empresa.

### No se puede crear el rol
- **Causa:** falta el **Nombre** o no hay ningún permiso marcado; ambos son obligatorios.
- **Solución:** escribir el nombre y marcar al menos un permiso antes de hacer clic en **Crear**.

### El cambio de un rol solo se aplicó en una empresa
- **Causa:** la casilla **Modificar en todas las empresas** estaba desmarcada.
- **Solución:** volver a editar el rol, marcar la casilla y hacer clic en **Actualizar**.

---

## Resumen de reglas de negocio

| # | Regla de negocio |
| :--- | :--- |
| 1 | Control de acceso solo está disponible para usuarios administradores. |
| 2 | Todo acceso de un subusuario a una empresa se hace a través de un rol que agrupa permisos. |
| 3 | Los roles y permisos se configuran y evalúan por empresa; la tabla muestra los roles de la empresa elegida en el selector. |
| 4 | Sin el permiso requerido, el sistema impide la acción de manera definitiva. |
| 5 | Los cambios en roles y permisos se aplican de inmediato a los usuarios con ese rol. |
| 6 | Para crear un rol son obligatorios el nombre y al menos un permiso. |
| 7 | «Crear rol para: Todas mis empresas» crea el rol en todas las empresas del administrador que aún no tengan un rol con el mismo nombre. |
| 8 | «Modificar en todas las empresas» actualiza el rol en todas las empresas donde existe con el mismo nombre, en una sola operación. |
| 9 | El nombre de un rol no se modifica al editarlo. |
| 10 | Eliminar un rol es permanente y no se puede deshacer. |

---

## Preguntas frecuentes

**¿Qué es un rol en Zoe?**
Un conjunto de permisos con un nombre. Un subusuario siempre accede a una empresa a través de un rol.

**¿Puedo tener el mismo rol en todas mis empresas sin crearlo una por una?**
Sí. En la ventana **Nuevo rol**, el campo **Crear rol para** viene en **Todas mis empresas**: el rol se crea en todas las empresas que aún no tengan uno con ese nombre.

**¿Cómo cambio los permisos de un rol en todas mis empresas a la vez?**
En `Control de acceso > Roles y permisos`, se edita el rol, se marca **Modificar en todas las empresas** y se hace clic en **Actualizar**.

**¿Los roles son iguales en todas las empresas?**
No necesariamente. Los roles y permisos se configuran y evalúan de forma independiente por empresa; las opciones de creación y edición masiva son las que permiten mantenerlos iguales.

**¿Cuándo se aplican los cambios de un rol?**
De inmediato, a todos los usuarios que tienen ese rol.

**¿Qué pasa si un usuario no tiene el permiso de una acción?**
El sistema le impide ejecutar la acción. Las acciones críticas de los módulos están protegidas por permisos de la plataforma.

**¿Se puede deshacer la eliminación de un rol?**
No. El rol se elimina de forma permanente.
