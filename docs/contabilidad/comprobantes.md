---
title: Comprobantes
description: Vista principal de gestión de comprobantes contables de la empresa en Zoe Nube. Cubre el listado de comprobantes (columnas, orden, selector de columnas, paginación y botón de recargar), la búsqueda general y los filtros avanzados (fecha, tercero, tipo, número de factura, número de comprobante, CUIP y estado), las acciones por registro (previsualizar con impresión e historial, descargar en PDF o Excel, editar, copiar y anular), el procedimiento de anulación con motivo y confirmación por número, las restricciones de los comprobantes que llegan por integración desde Optimun Escritorio, el bloqueo por periodo contable cerrado, la creación de comprobantes y la carga de un comprobante desde una plantilla de Excel.
module: contabilidad
category: comprobantes
slug: comprobantes
order: 11
tags:
  - comprobantes
  - comprobante-contable
  - asiento-contable
  - listado-de-comprobantes
  - busqueda-avanzada
  - filtros-avanzados
  - cuip
  - integracion
  - optimun-escritorio
  - previsualizar
  - descargar-comprobante
  - pdf
  - excel
  - editar-comprobante
  - copiar-comprobante
  - anular-comprobante
  - anulacion
  - historial-comprobante
  - periodo-cerrado
  - importacion-excel
  - plantilla-excel
  - conciliacion-bancaria
  - contabilidad
draft: false
rag_exclude: false
last_updated: 2026-09-22
---

# Comprobantes

La pantalla de Comprobantes es el centro de gestión de los asientos contables de la empresa activa. Desde ella se visualizan, se buscan, se auditan y se administran todos los comprobantes registrados, ya sea que se hayan creado manualmente en Zoe, cargado desde una plantilla de Excel o recibido desde un sistema externo como Optimun Escritorio. Este documento explica los elementos de la pantalla, la búsqueda y los filtros avanzados, las acciones disponibles en cada comprobante, el procedimiento de anulación, las restricciones de los comprobantes de integración y de los periodos cerrados, y la carga de un comprobante desde Excel.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Elementos de la pantalla](#elementos-de-la-pantalla)
4. [Búsqueda y filtros avanzados](#búsqueda-y-filtros-avanzados)
5. [Acciones por comprobante](#acciones-por-comprobante)
6. [Anular un comprobante](#anular-un-comprobante)
7. [Comprobantes de integración](#comprobantes-de-integración)
8. [Comprobantes de un periodo cerrado](#comprobantes-de-un-periodo-cerrado)
9. [Crear un comprobante](#crear-un-comprobante)
10. [Cargar un comprobante desde una plantilla de Excel](#cargar-un-comprobante-desde-una-plantilla-de-excel)
11. [Solución de problemas](#solución-de-problemas)
12. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
13. [Preguntas frecuentes](#preguntas-frecuentes)

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Comprobantes` (al mismo nivel que `Configuración` y `Reportes` en el menú lateral).
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONTABILIDAD / COMPROBANTES`.
- **Título de la pantalla:** «Comprobantes».
- **Subtítulo de la pantalla:** «Gestiona y administra los comprobantes contables de tu empresa».
- **Contenido de la pantalla:** una barra de búsqueda y una tarjeta titulada «Listado de comprobantes», con la tabla de comprobantes y el contador de registros junto al título.

**Rutas complementarias:**

| Proceso | Ruta |
| --- | --- |
| Habilitar la edición de un comprobante de integración | `Contabilidad > Configuración > Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante` |
| Abrir o cerrar un mes contable | `Contabilidad > Configuración > Especiales > Periodos > Gestionar periodos contables` |
| Monitorear comprobantes recibidos por integración asíncrona | `Contabilidad > Configuración > Especiales > Comprobantes > Comprobantes en proceso` |
| Definir los tipos de documento y su numeración | `Contabilidad > Configuración > Tipos de documento` |

## Requisitos previos

- Tener una empresa creada y seleccionada en Zoe.
- Tener acceso al módulo de Contabilidad.
- Verificar el año fiscal activo, que aparece junto a **Contabilidad** en el menú lateral: los comprobantes pertenecen al año fiscal.
- Para cargar un comprobante desde Excel, disponer de la plantilla que entrega la opción **Importar datos > Descargar plantilla**.

## Elementos de la pantalla

**Columnas de la tabla:**

| Columna | Contenido |
| --- | --- |
| **ID** | Posición de la fila dentro de la página. |
| **Nro.Comprobante** | Prefijo del tipo de documento y consecutivo, por ejemplo `CI-8` o `GADIV-2`. Permite ordenar la tabla. |
| **Fecha** | Fecha contable del comprobante. Permite ordenar la tabla. |
| **Nro. Factura** | Número de factura asociado, o un guion si no tiene. |
| **Total** | Valor total del comprobante. |
| **Descripción** | Descripción general del asiento. |
| **Terceros** | Nombre y NIT del tercero del comprobante. |
| **Estado** | **Contabilizado** (verde) o **Anulado** (rojo). |
| **Acciones** | Botones disponibles para el comprobante según su origen y su estado. |

**Controles de la pantalla:**

| Control | Ubicación | Descripción |
| --- | --- | --- |
| **Consultar** | Parte superior | Campo de texto para la búsqueda general de un comprobante por su número. |
| **Filtrar** | Junto a **Consultar** | Ejecuta la búsqueda general. |
| **Busqueda avanzada** | Junto a **Filtrar** | Abre el panel **Filtros avanzados**. Ver [Búsqueda y filtros avanzados](#búsqueda-y-filtros-avanzados). |
| **Recargar** (ícono de flecha circular) | Junto a **Busqueda avanzada** | Actualiza la tabla en tiempo real sin recargar la página completa del navegador. |
| **Nuevo** | Sobre la tabla, a la derecha | Abre el formulario **Nuevo comprobante**. |
| **Columnas** | Sobre la tabla, a la derecha | Permite mostrar u ocultar columnas de la tabla. |
| **Paginación** | Debajo de la tabla, a la izquierda | Navegación entre páginas: primera, anterior, números de página, siguiente y última. |
| **Selector de registros por página** | Debajo de la tabla, a la derecha | Opciones de 1, 7, 10, 20, 50 y 100 registros por página. |

**Uso del botón Recargar:** sirve para ver comprobantes registrados por otros usuarios o recibidos desde un sistema externo después de haber abierto la pantalla, sin perder la página en la que se está trabajando.

## Búsqueda y filtros avanzados

**Búsqueda general:** se escribe el número del comprobante en **Consultar** y se selecciona **Filtrar**.

**Filtros avanzados:** al seleccionar **Busqueda avanzada** se abre el panel **Filtros avanzados**, con un botón por cada filtro. Al elegir uno aparece debajo el campo correspondiente, y la tabla se actualiza con los comprobantes que coinciden.

| Filtro | Campo | Descripción |
| --- | --- | --- |
| **Por fecha** | Rango de fechas | Comprobantes cuya fecha está dentro del rango. |
| **Por tercero** | **Tercero**, desplegable «Buscar por nombre o NIT» | Comprobantes de un tercero determinado. |
| **Tipo** | **Prefijo**, desplegable «Seleccionar prefijo» con los tipos de documento (por ejemplo `CI - Comprobante de ingreso`, `INOM - Nómina`) | Comprobantes de un tipo de documento. |
| **Nro. Factura** | Número de factura | Comprobantes asociados a una factura. |
| **Nro.Comprobante** | Número de comprobante | Un comprobante por su número. |
| **CUIP** | Código Único de Identificación de Plataforma | Comprobantes recibidos desde un sistema externo, por el código con el que ese sistema los identifica. |
| **Estado** | Estado | Comprobantes **Contabilizados** o **Anulados**. |
| **Limpiar** | — | Quita todos los filtros aplicados. |

**CUIP (Código Único de Identificación de Plataforma):** es la clave con la que un sistema externo, como Optimun Escritorio, identifica un documento que envió a Zoe. Permite rastrear en Zoe el comprobante generado a partir de un registro del sistema de origen.

**Indicador de filtro activo:** mientras haya un filtro aplicado, junto al título «Listado de comprobantes» aparece la etiqueta **Filtro Avanzado Aplicado**, con una **X** para quitarlo. El contador de registros refleja solo los comprobantes filtrados. Si ningún comprobante coincide, la tabla muestra «Sin registros».

## Acciones por comprobante

| Botón | Acción | Descripción |
| --- | --- | --- |
| Ojo | **Previsualizar** | Abre la ventana **Previsualizar comprobante** en pantalla, sin generar ni descargar archivos. |
| Flecha hacia abajo | **Descargar** | Despliega las opciones **PDF** y **Excel** para descargar el comprobante. |
| Lápiz | **Editar** | Abre el formulario **Editar [número] - [tipo]** para modificar fecha, tipo, descripción, cuentas, terceros, centros de costo y valores. Los cambios se guardan con **Actualizar**. |
| Tres puntos > **Copiar** | **Copiar** | Duplica la estructura y los valores del comprobante en el formulario de creación, para registrar un comprobante nuevo a partir de él. |
| Tres puntos > **Anular comprobante** | **Anular** | Marca el comprobante como anulado. Acción irreversible. Ver [Anular un comprobante](#anular-un-comprobante). |

**Acciones visibles según el comprobante:**

| Comprobante | Acciones disponibles |
| --- | --- |
| Contabilizado, creado en Zoe, en periodo abierto | Previsualizar, Descargar, Editar, Copiar, Anular |
| Anulado | Previsualizar, Descargar |
| Recibido por integración (bloqueado por defecto) | Previsualizar, Descargar |
| Recibido por integración con la edición activada desde Especiales | Previsualizar, Descargar, Editar y el menú de tres puntos |

**Ventana Previsualizar comprobante:**

- Encabezado con el logo y los datos de la empresa (razón social, documento, dirección, correo, ciudad) y el estado del comprobante.
- Recuadro con el **Número** y la **Fecha**.
- **Descripción** del comprobante.
- Tabla de líneas con las columnas **#**, **Cuenta contable**, **Concepto**, **Tercero** (con su NIT y el número de factura), **Centro de costo**, **Débito** y **Crédito**, y la fila **Totales**.
- Botón **Imprimir**: envía el comprobante a impresión.
- Botón **Historial**: abre la ventana **Historial del comprobante**, con el subtítulo «Este historial muestra cambios realizados sobre el comprobante, sus líneas y entidades relacionadas». Presenta una línea de tiempo (**Timeline**) con el número de eventos; cada evento indica qué ocurrió (por ejemplo «Comprobante IADS-2 creado»), la fecha y hora, a qué se aplicó y el usuario que lo hizo.

## Anular un comprobante

Anular deja el comprobante sin efecto contable, pero lo conserva en el listado con estado **Anulado** como registro de lo ocurrido. **La anulación es irreversible en la plataforma.**

**Procedimiento:**

1. En la fila del comprobante, seleccionar los tres puntos y elegir **Anular comprobante**.
2. Se abre la ventana **¿Estás seguro?**, con el mensaje «El comprobante número [número] será anulado. Esta acción no se puede deshacer».
3. Los campos **Fecha de la anulación** (fecha del día) y **Usuario que anula** (usuario de la sesión) se llenan automáticamente.
4. Diligenciar el **Motivo de la anulación**, que es obligatorio.
5. En **Número de comprobante**, escribir el número del comprobante tal como aparece en el mensaje, como confirmación.
6. Seleccionar **Sí, anular**. Con **Cancelar** se cierra la ventana sin anular.

**Resultado:** la plataforma muestra «Operación exitosa — Comprobante anulado correctamente». El estado del comprobante cambia a **Anulado** y en su fila quedan solo las acciones de previsualizar y descargar.

## Comprobantes de integración

Los comprobantes que llegan a Zoe desde un sistema externo (por ejemplo, Optimun Escritorio) quedan **bloqueados para edición por defecto**, para evitar diferencias con la fuente de origen.

| Operación | Comportamiento |
| --- | --- |
| Previsualizar y descargar | Disponibles siempre. |
| Editar | No disponible por defecto. Se habilita desde `Contabilidad > Configuración > Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante`, buscando el comprobante por prefijo y número. |
| Anular | No se puede anular desde Zoe. La anulación debe hacerse en el sistema de origen (por ejemplo, Optimun Escritorio). |

Los comprobantes de integración se localizan con el filtro **CUIP** usando el código del documento en el sistema de origen.

## Comprobantes de un periodo cerrado

Un comprobante cuya fecha pertenece a un mes contable cerrado queda bloqueado para modificación y anulación mientras el periodo no se reabra.

- Al abrir el comprobante, el formulario muestra la etiqueta **Periodo cerrado** (en ámbar) junto al título.
- Al intentar guardar con **Actualizar**, la plataforma responde con el error «No se pueden realizar operaciones contables en [mes] de [año]. El periodo está cerrado» y no guarda los cambios.
- Para modificarlo hay que reabrir el mes desde `Contabilidad > Configuración > Especiales > Periodos > Gestionar periodos contables`, hacer el cambio y volver a cerrar el mes.

El formulario de un comprobante en un mes abierto muestra la etiqueta **Periodo abierto**.

## Crear un comprobante

El botón **Nuevo**, sobre la tabla a la derecha, abre el formulario **Nuevo comprobante** («Complete los datos del asiento contable»). El formulario contiene los campos **Fijar mes**, **Fecha**, **Tipo de documento** y **Descripción**, la tabla **Cuentas del asiento** (Cuenta, Concepto, Factura, Tercero, C. Costo, Débito y Crédito), el botón **Agregar línea**, los totales (**Total débito**, **Total crédito**, **Diferencia**) y los botones **Cancelar** y **Crear**.

El procedimiento completo de creación de un asiento está en el documento `primer-asiento-contable`.

## Cargar un comprobante desde una plantilla de Excel

El formulario **Nuevo comprobante** incluye, arriba a la derecha, el botón desplegable **Importar datos**, con dos opciones: **Importar** y **Descargar plantilla**. Permite llenar las líneas del asiento desde un archivo de Excel en lugar de digitarlas una a una.

**Utilidad:** agiliza procesos repetitivos o de muchas líneas, como las conciliaciones bancarias, los movimientos recurrentes del mes o los registros masivos.

**Procedimiento:**

1. En el listado de comprobantes, seleccionar **Nuevo**.
2. En **Importar datos**, elegir **Descargar plantilla**. Se descarga el archivo `plantilla_comprobante_zoenube.xlsx`.
3. Diligenciar la plantilla con las líneas del asiento y guardarla.
4. En **Importar datos**, elegir **Importar** y seleccionar el archivo `.xlsx`.
5. La plataforma muestra «Operación exitosa — Datos importados correctamente» y llena la tabla **Cuentas del asiento** con la cuenta, el concepto, la factura, el tercero, el centro de costo y los valores débito y crédito de cada línea. La fecha del formulario también se ajusta.
6. Revisar la **Fecha**, seleccionar el **Tipo de documento** y escribir la **Descripción** (campos obligatorios).
7. Verificar que la **Diferencia** sea $ 0,00 y seleccionar **Crear**.

**Resultado:** la plataforma muestra «Operación exitosa — Comprobante creado correctamente» y el comprobante aparece de primero en el listado con estado **Contabilizado**. Las líneas importadas se pueden corregir en pantalla antes de crear el comprobante.

TODO(dato): listar las columnas de la plantilla de comprobantes e indicar cuáles son obligatorias.

## Solución de problemas

### Un comprobante no muestra el botón de editar ni el menú de tres puntos

El comprobante está anulado o fue recibido por integración. Un comprobante anulado ya no se puede modificar. Un comprobante de integración requiere activar su edición desde `Contabilidad > Configuración > Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante`.

### No se puede anular un comprobante que llegó de Optimun Escritorio

Es el comportamiento esperado. Los comprobantes de integración se anulan en el sistema de origen, no en Zoe.

### La ventana de anulación no permite confirmar

Debe diligenciarse el **Motivo de la anulación**, que es obligatorio, y el **Número de comprobante** debe coincidir exactamente con el que muestra el mensaje, incluidos el prefijo y el guion.

### Al guardar aparece «El periodo está cerrado»

La fecha del comprobante pertenece a un mes cerrado. Debe reabrirse el mes desde `Contabilidad > Configuración > Especiales > Periodos > Gestionar periodos contables` o, si la fecha era incorrecta, cambiarla a un mes abierto.

### El listado muestra «Sin registros»

Hay un filtro avanzado aplicado que no coincide con ningún comprobante. Se quita con la **X** de la etiqueta **Filtro Avanzado Aplicado** o con el botón **Limpiar** del panel de filtros.

### Un comprobante recién registrado no aparece en el listado

Debe usarse el botón **Recargar** para actualizar la tabla. Si hay un filtro aplicado, también puede estar ocultando el comprobante.

### Se importó la plantilla pero no se puede crear el comprobante

Deben diligenciarse el **Tipo de documento** y la **Descripción**, que la plantilla no llena, y la **Diferencia** debe ser $ 0,00. Si los débitos y los créditos no suman lo mismo, deben corregirse en pantalla o en la plantilla.

### Se anuló un comprobante por error

No se puede revertir. El comprobante debe registrarse de nuevo; la opción **Copiar** no está disponible en un comprobante anulado, así que debe crearse con **Nuevo**.

## Resumen de reglas de negocio

| # | Regla |
| --- | --- |
| 1 | La pantalla `Contabilidad > Comprobantes` muestra los comprobantes de la empresa activa en el año fiscal seleccionado. |
| 2 | El botón **Recargar** actualiza la tabla sin recargar la página completa del navegador. |
| 3 | La búsqueda general localiza un comprobante por su número; los filtros avanzados permiten buscar por fecha, tercero, tipo, número de factura, número de comprobante, CUIP y estado. |
| 4 | El CUIP (Código Único de Identificación de Plataforma) identifica los comprobantes recibidos desde sistemas externos. |
| 5 | Los estados de un comprobante son **Contabilizado** y **Anulado**. |
| 6 | Previsualizar muestra el comprobante en pantalla sin generar archivos; desde allí se puede imprimir y consultar el historial de cambios. |
| 7 | La descarga del comprobante se ofrece en PDF y en Excel. |
| 8 | Copiar lleva la estructura y los valores del comprobante al formulario de creación. |
| 9 | La anulación es irreversible, exige un motivo y la confirmación escribiendo el número del comprobante, y registra la fecha y el usuario que anula. |
| 10 | Un comprobante anulado permanece en el listado y solo admite previsualizar y descargar. |
| 11 | Los comprobantes de integración solo permiten previsualizar y descargar por defecto. |
| 12 | Los comprobantes de integración no se anulan desde Zoe; su anulación se hace en el sistema de origen. |
| 13 | La edición de un comprobante de integración se habilita desde `Configuración > Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante`. |
| 14 | Un comprobante de un periodo cerrado no se puede modificar ni anular hasta que el periodo se reabra. |
| 15 | El formulario del comprobante indica con una etiqueta si su periodo está abierto o cerrado. |
| 16 | La carga desde Excel se hace en el formulario **Nuevo comprobante** con **Importar datos**, sobre la plantilla que entrega **Descargar plantilla**. |
| 17 | La plantilla llena las líneas del asiento; el tipo de documento y la descripción se completan en pantalla antes de crear. |
| 18 | Un comprobante solo se crea si está cuadrado: la diferencia entre débitos y créditos debe ser cero. |

## Preguntas frecuentes

**¿Dónde se consultan los comprobantes contables?**
En `Contabilidad > Comprobantes`.

**¿Cómo se actualiza el listado sin recargar la página?**
Con el botón de flecha circular (Recargar), junto a **Busqueda avanzada**.

**¿Qué es el CUIP?**
El Código Único de Identificación de Plataforma: la clave con la que un sistema externo identifica un documento enviado a Zoe. Se usa como filtro para rastrear comprobantes de integración.

**¿En qué formatos se descarga un comprobante?**
En PDF y en Excel, desde el botón de descarga de la fila.

**¿Se puede ver un comprobante sin descargarlo?**
Sí, con la acción Previsualizar (ícono de ojo).

**¿Dónde se ve quién creó o modificó un comprobante?**
En la ventana Previsualizar comprobante, botón **Historial**.

**¿Se puede revertir una anulación?**
No. La anulación es irreversible.

**¿Por qué un comprobante de Optimun Escritorio no se puede editar?**
Porque los comprobantes de integración llegan bloqueados por defecto. La edición se habilita desde `Configuración > Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante`.

**¿Cómo se anula un comprobante que llegó de Optimun Escritorio?**
Desde Optimun Escritorio. Zoe no permite anular comprobantes de integración.

**¿Se puede editar un comprobante de un mes cerrado?**
No, hasta que se reabra el mes en `Configuración > Especiales > Periodos > Gestionar periodos contables`.

**¿Cómo se carga un comprobante desde Excel?**
En **Nuevo**, botón **Importar datos**: primero **Descargar plantilla**, luego **Importar** con el archivo diligenciado.

**¿Para qué sirve la carga por plantilla?**
Para agilizar asientos de muchas líneas o repetitivos, como las conciliaciones bancarias.
