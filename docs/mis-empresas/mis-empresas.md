---
title: Mis Empresas
description: Opción Mis Empresas de Zoe Nube, disponible para todos los usuarios desde el menú lateral principal. Cubre la ubicación del menú, qué empresas ve un administrador y un subusuario, el listado de empresas con su búsqueda, paginación y acciones, el ingreso a una empresa, el menú que se abre al hacer clic en el nombre de la empresa, la edición de los datos básicos (solo administradores), la carga del logo que se imprime en los comprobantes en PDF y la generación de una nueva API Key para integraciones externas.
module: mis-empresas
category: administracion
slug: mis-empresas
order: 1
tags: [mis empresas, listado de empresas, buscar empresa, filtrar empresas, paginacion, columnas, crear empresa, empresa, seleccion de empresa, entrar a una empresa, cambiar de empresa, editar empresa, datos basicos, nit, razon social, logo, logotipo, comprobante en pdf, api key, clave de api, integraciones, facturacion electronica, optimun, administrador, subusuario]
draft: false
rag_exclude: false
last_updated: 2026-11-25
---

# Mis Empresas

**Mis Empresas** es una opción de Zoe Nube independiente del módulo de Contabilidad y disponible para todos los usuarios. Reúne el trabajo sobre las empresas: saber a cuáles se tiene acceso, entrar a una para operar sus módulos y, si se es administrador, editar sus datos básicos, su logo y su API Key. El acceso de los subusuarios a cada empresa se asigna en [Usuarios](../control-de-acceso/usuarios.md).

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Empresas visibles según el tipo de usuario](#empresas-visibles-según-el-tipo-de-usuario)
3. [Listado de empresas](#listado-de-empresas)
4. [Entrar a una empresa](#entrar-a-una-empresa)
5. [Menú de la empresa](#menú-de-la-empresa)
6. [Editar una empresa](#editar-una-empresa)
7. [Logo de la empresa](#logo-de-la-empresa)
8. [API Key](#api-key)
9. [Errores frecuentes](#errores-frecuentes)
10. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
11. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Mis Empresas`.
- **Ubicación del menú:** en el menú lateral principal (sidebar), en la sección **Administración**, entre **Inicio** y **Control de acceso**.
- **Alcance:** es independiente del módulo de Contabilidad; no se necesita entrar a una empresa para abrirla.
- **Dentro de una empresa:** el menú lateral muestra las opciones de esa empresa (Inicio, Contabilidad y sus secciones). Para volver al listado se usa **Administrar empresas** en el [menú de la empresa](#menú-de-la-empresa).
- **Disponibilidad:** todos los usuarios, administradores y subusuarios.

---

## Empresas visibles según el tipo de usuario

| Tipo de usuario | Empresas que ve | Puede editar empresas |
| :--- | :--- | :--- |
| Administrador | Todas las empresas creadas en su cuenta. | Sí. |
| Subusuario (colaborador) | Únicamente las empresas a las que se le otorgó acceso. | No. |

En el encabezado de Zoe, cada persona figura con su rol: «Administrador» o «Subusuario».

---

## Listado de empresas

Al hacer clic en **Mis Empresas** se abre la pantalla «Empresas», con la ruta `INICIO / EMPRESAS` y el subtítulo «Gestiona tus empresas desde aquí».

### Elementos de la pantalla

| Elemento | Función |
| :--- | :--- |
| Buscador («Buscar por razón social, nombre comercial o NIT») y botón **Filtrar** | Filtra la lista. Admite una parte del dato. La **×** del buscador borra la búsqueda. |
| **Listado de empresas** y contador de registros | Título de la tabla y número de empresas listadas. |
| **Crear empresa** | Botón para registrar una nueva empresa. |
| **Columnas** | Selector de las columnas de la tabla. |
| Paginación | Botones de primera, anterior, siguiente y última página. |
| Registros por página | 1, 7, 10, 20, 50 o 100. El valor inicial es 7. |

### Columnas y acciones

| Columna | Contenido |
| :--- | :--- |
| ID | Número de la fila. |
| NIT | Número de identificación de la empresa. |
| Razón social | Nombre de la empresa. |
| Correo | Correo de la empresa. |
| Dirección | Dirección de la empresa. |
| Acciones | **Entrar** (ícono de flecha) y **Editar empresa** (ícono de engranaje). |

| Acción | Resultado | Quién puede usarla |
| :--- | :--- | :--- |
| Entrar | Abre el entorno de trabajo de la empresa. | Usuarios con acceso a la empresa. |
| Editar empresa | Abre la ventana de [edición](#editar-una-empresa). | Solo administradores. |

---

## Entrar a una empresa

Entrar a una empresa abre su entorno de trabajo, donde se operan sus módulos y opciones contables. Hay dos formas: el botón **Entrar** de la fila en el [listado de empresas](#listado-de-empresas), o la pantalla de **Inicio**.

Desde la pantalla de **Inicio** («Selección de Empresa», con el texto «Selecciona la empresa con la que deseas trabajar hoy»):

1. Cada empresa se presenta como una tarjeta con su nombre, NIT y país.
2. Hacer clic en la tarjeta de la empresa.
3. Zoe abre el panel de la empresa, con la ruta `EMPRESAS / <nombre de la empresa>`.

Para el administrador, la pantalla de selección incluye además la tarjeta **Crear empresa** («Añade una nueva razón social»).

El panel de la empresa muestra los **Accesos Directos**: PUC - Plan Único de Cuentas, Tipos de documentos, Centros de costo, Terceros, Anexos, Opciones Especiales, Comprobantes, Reportes, Formatos Exógena e Información Exógena.

---

## Menú de la empresa

Dentro de una empresa, al hacer clic en su nombre (arriba a la derecha) se despliega un menú:

| Opción | Función |
| :--- | :--- |
| Cambiar de empresa | Lista las otras empresas disponibles para pasar a una de ellas. |
| Todas mis empresas | Vuelve a la selección de empresa. |
| Administrar empresas | Lleva al listado de Mis Empresas. Solo administradores. |
| Editar esta empresa | Abre la ventana de edición de la empresa actual. Solo administradores. |

Un subusuario con una sola empresa asignada ve en este menú únicamente **Todas mis empresas**.

---

## Editar una empresa

La edición es **exclusiva de los usuarios administradores**.

1. Abrir la edición con el botón **Editar empresa** de la fila en el listado, o, dentro de la empresa, con clic en su nombre y la opción **Editar esta empresa**.
2. Se abre la ventana **Editando <nombre de la empresa>**, con el subtítulo «Actualiza los datos, el logo y la API Key de la empresa».
3. Modificar los datos necesarios.
4. Hacer clic en **Guardar**. El sistema confirma con «Empresa actualizada correctamente». El botón **Cancelar** cierra la ventana.

La ventana tiene tres secciones: **Datos básicos**, **Logo** y **API Key**.

### Datos básicos

| Campo | Obligatorio | Detalle |
| :--- | :---: | :--- |
| Tipo de identificación | Sí | Lista desplegable, por ejemplo «Nit». |
| NIT | Sí | Número de identificación de la empresa. |
| DV | — | Dígito de verificación; el campo aparece en gris. |
| Régimen de IVA | Sí | Lista desplegable. |
| Responsabilidad tributaria | Sí | Lista desplegable. |
| Tipo de persona | Sí | «Persona jurídica» o «Persona natural». |
| Razón social | Sí | Nombre de la empresa. |
| Municipio | Sí | Lista desplegable. |
| Dirección | Sí | Dirección de la empresa. |
| Correo electrónico | Sí | Correo de la empresa. |
| Nombre del contador | No | Nombre del contador. |
| N° Tarjeta profesional | No | Tarjeta profesional del contador. |

---

## Logo de la empresa

| Elemento | Detalle |
| :--- | :--- |
| Logo actual | Muestra el logo configurado. |
| Nuevo logo | Espacio «Seleccionar logo» para elegir una imagen. |
| Formatos admitidos | PNG, JPG o WEBP. |
| Tamaño máximo | 2 MB. |

Para cargar o reemplazar el logo se selecciona la imagen en **Seleccionar logo** y se hace clic en **Guardar**. El logo se puede cambiar por otro, pero no hay una opción para eliminarlo directamente.

**Logo en comprobantes PDF:** si la empresa tiene un logo configurado, aparece automáticamente en el encabezado al descargar cualquier comprobante contable a PDF (en [Comprobantes](../contabilidad/comprobantes.md), ícono de descarga, opción **PDF**).

---

## API Key

La API Key es la clave que usan los sistemas externos para conectarse con la empresa. Cada empresa administra la suya en la sección **API Key** de la ventana de edición.

### Elementos de la sección

| Elemento | Función |
| :--- | :--- |
| Campo **API Key** | Muestra la clave oculta, dejando ver solo sus últimos caracteres. |
| Ícono de ojo | Muestra la clave. |
| Ícono de copiar («Copiar Api key») | Copia la clave al portapapeles. |
| Aviso | «Si generas una nueva API Key, la anterior quedará inutilizada. Ingresa el NIT para continuar.» |
| **Verificar NIT** | Se escribe el NIT de la empresa para habilitar la generación. |
| **Generar nueva API Key** | Inicia la generación y pide confirmación. |

### Generar una nueva API Key

1. En la ventana de edición, desplegar la sección **API Key**.
2. Escribir el NIT de la empresa en **Verificar NIT**.
3. Hacer clic en **Generar nueva API Key**.
4. En la ventana **Confirmar generación de API Key**, hacer clic en **Confirmar y generar**.
5. El sistema confirma con «Api key generada correctamente».
6. Copiar la clave nueva, guardarla en un lugar seguro y actualizarla en los sistemas integrados.

### Precauciones

- La API Key anterior **deja de funcionar inmediatamente** y la acción **no se puede deshacer**.
- Las integraciones que usen la clave anterior, como Optimun o sistemas de facturación electrónica, no podrán conectarse hasta que se actualicen con la nueva.
- La nueva clave se aplica de inmediato, **aunque no se guarden los demás cambios del formulario**.
- Para anular una clave se genera una nueva.
- La clave se debe compartir solo con personas autorizadas.

El uso de la clave en las peticiones se describe en la documentación de la API de Contabilidad de Zoe.

---

## Errores frecuentes

| Situación | Causa probable | Solución |
| :--- | :--- | :--- |
| No aparece una empresa | El subusuario no la tiene asignada. | El administrador la asigna en `Control de acceso > Usuarios`. |
| No aparece «Editar esta empresa» | Se ingresó como subusuario. | Ingresar con el usuario administrador. |
| Una integración dejó de conectarse | Se generó una API Key nueva. | Actualizar la clave en el sistema integrado. |
| El comprobante en PDF sale sin logo | La empresa no tiene un logo guardado. | Cargar el logo, guardar y descargar de nuevo el comprobante. |

---

## Resumen de reglas de negocio

| N.° | Regla |
| :---: | :--- |
| 1 | Mis Empresas está disponible para todos los usuarios y es independiente del módulo de Contabilidad. |
| 2 | El administrador ve todas las empresas creadas en su cuenta. |
| 3 | El subusuario ve únicamente las empresas a las que se le otorgó acceso. |
| 4 | Solo el administrador puede editar la información de una empresa. |
| 5 | El logo admite PNG, JPG o WEBP de máximo 2 MB. |
| 6 | Si la empresa tiene logo, se imprime en el encabezado de los comprobantes contables en PDF. |
| 7 | Generar una API Key exige verificar el NIT de la empresa y confirmar. |
| 8 | Al generar una nueva API Key, la anterior queda invalidada de inmediato y la acción no se puede deshacer. |
| 9 | La nueva API Key se aplica aunque no se guarden los demás cambios del formulario. |

---

## Preguntas frecuentes

**¿Quién puede usar Mis Empresas?**
Todos los usuarios. Cada uno ve las empresas que le corresponden y solo el administrador puede editarlas.

**¿Dónde está Mis Empresas?**
En el menú lateral principal, en la sección Administración, entre Inicio y Control de acceso.

**¿Cómo busco una empresa?**
En Mis Empresas, escribiendo la razón social, el nombre comercial o el NIT y haciendo clic en **Filtrar**.

**¿Cómo edito la empresa en la que estoy trabajando?**
Con clic en el nombre de la empresa, arriba a la derecha, y la opción **Editar esta empresa**. Requiere usuario administrador.

**¿Cómo cambio de una empresa a otra?**
Desde el mismo menú, en **Cambiar de empresa**, o volviendo con **Todas mis empresas**.

**¿Cómo pongo mi logo en los comprobantes?**
Cargando el logo en la ventana de edición de la empresa y guardando. Aparece en el encabezado de los comprobantes descargados en PDF.

**¿Qué pasa si genero una nueva API Key?**
La anterior deja de funcionar de inmediato. Hay que actualizar la clave nueva en cada sistema integrado.

**¿Un subusuario puede editar una empresa?**
No. Su menú de empresa no ofrece **Editar esta empresa**.
