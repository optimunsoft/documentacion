---
title: Tipos de documento (tipos de asiento) y numeración de comprobantes
description: Clasificación de los comprobantes contables mediante tipos de documento, esquemas de numeración anual y mensual del consecutivo, tipos de documento generados por defecto en cada año fiscal, reglas de los tipos reservados SI y CA, tipos API de integración y comportamiento al abrir un año fiscal nuevo.
module: contabilidad
category: configuracion
slug: tipos-documento
order: 6
tags:
  - configuracion
  - tipos-de-documento
  - tipos-de-asiento
  - numeracion-anual
  - numeracion-mensual
  - consecutivos
  - consecutivo-de-comprobante
  - periodo
  - tipos-api
  - asientos-de-integracion
  - saldos-iniciales
  - cierre-de-ano
  - ano-fiscal
  - comprobantes
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-08-31
---

# Tipos de documento (tipos de asiento) y numeración de comprobantes

Los tipos de documento, también llamados tipos de asiento, son la clasificación con la que Zoe organiza todos los comprobantes contables de un año fiscal. Cada comprobante se registra con un tipo de documento, y de ese tipo dependen su categoría y el consecutivo con el que queda numerado. Este documento explica dónde está la pantalla, qué son los tipos de documento, cómo funcionan los dos esquemas de numeración (anual y mensual), qué tipos genera la plataforma automáticamente en cada año fiscal, cuáles son reservados, qué son los tipos API de integración y qué ocurre con los tipos personalizados al abrir un año fiscal nuevo.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Concepto: qué son los tipos de documento](#concepto-qué-son-los-tipos-de-documento)
4. [Contexto por año fiscal](#contexto-por-año-fiscal)
5. [Elementos de la pantalla](#elementos-de-la-pantalla)
6. [Numeración de comprobantes (consecutivos)](#numeración-de-comprobantes-consecutivos)
7. [Tipos de documento por defecto del año fiscal](#tipos-de-documento-por-defecto-del-año-fiscal)
8. [Crear un tipo de documento](#crear-un-tipo-de-documento)
9. [Editar un tipo de documento](#editar-un-tipo-de-documento)
10. [Asientos de integración (tipos API)](#asientos-de-integración-tipos-api)
11. [Comportamiento al abrir un año fiscal nuevo](#comportamiento-al-abrir-un-año-fiscal-nuevo)
12. [Solución de problemas](#solución-de-problemas)
13. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
14. [Preguntas frecuentes](#preguntas-frecuentes)

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Tipos de documento`.
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / TIPOS DE DOCUMENTO`.
- **Título de la pantalla:** «Tipos de Documento».
- **Subtítulo de la pantalla:** «Gestiona los tipos de documentos contables de tu empresa».
- **Contenido de la pantalla:** una tabla con todos los tipos de documento disponibles en el año fiscal activo.

## Requisitos previos

- Tener una empresa creada y seleccionada en Zoe.
- Tener acceso al módulo de Contabilidad.
- Saber en qué año fiscal se está trabajando, porque los tipos de documento que se muestran y se editan pertenecen a ese año.

## Concepto: qué son los tipos de documento

Un tipo de documento (o tipo de asiento) es la categoría con la que se clasifica un comprobante contable. Su función principal es **clasificar y organizar los comprobantes registrados en el sistema**, de modo que después puedan filtrarse, buscarse y auditarse por tipo de operación.

Cada tipo de documento aporta dos elementos al comprobante:

1. **La clasificación funcional.** Identifica de qué operación se trata: una nota de contabilidad, un comprobante de egreso, una conciliación bancaria, etc.
2. **El consecutivo.** El código del tipo de documento es el prefijo del número consecutivo con el que queda numerado el comprobante.

A diferencia del PUC, la tabla de tipos de documento **sí se precarga automáticamente** al crear una empresa nueva y al habilitar cada año fiscal.

## Contexto por año fiscal

Los tipos de documento pertenecen al **año fiscal**, no a la empresa. Cada año fiscal tiene su propia tabla de tipos de documento, igual que ocurre con el PUC, los anexos, los comprobantes y la exógena.

| Información | Alcance |
| --- | --- |
| Tipos de documento | Por año fiscal |
| PUC (Plan Único de Cuentas) | Por año fiscal |
| Comprobantes | Por año fiscal |
| Centros de costo | Global |
| Terceros | Global |

**Consecuencia práctica:** un tipo de documento creado en un año fiscal solo existe en ese año. Ver [Comportamiento al abrir un año fiscal nuevo](#comportamiento-al-abrir-un-año-fiscal-nuevo).

## Elementos de la pantalla

La pantalla presenta una tabla en la que cada fila corresponde a un tipo de documento del año fiscal activo.

| Elemento | Posición | Función |
| --- | --- | --- |
| Campo **Consultar** | Superior izquierda | Caja de búsqueda de texto libre para localizar un tipo de documento. |
| Botón **Filtrar** | Superior izquierda, junto a **Consultar** | Aplica la búsqueda escrita en el campo **Consultar**. |
| Casilla **Ver Tipos API** | Superior izquierda, junto al botón **Filtrar** | Casilla de verificación. Al marcarla, la tabla cambia y muestra los tipos de documento reservados para integraciones. Ver [Asientos de integración (tipos API)](#asientos-de-integración-tipos-api). |
| Contador de registros | Encabezado de la tabla | Etiqueta «Tipos de documento» con el número de registros mostrados (por ejemplo, «10 registros»). |
| Botón **+ Nuevo** | Superior derecha de la tabla | Abre la ventana **Nuevo tipo de documento** para crear un tipo personalizado. |
| Control **Columnas** | Superior derecha de la tabla | Permite elegir qué columnas se muestran. |
| Columna **ID** | Tabla principal | Número de orden de la fila dentro del listado. |
| Columna **Nombre** | Tabla principal | Nombre descriptivo del tipo de documento. |
| Columna **Código** | Tabla principal | Código corto del tipo de documento, mostrado como etiqueta. Es el prefijo del consecutivo de los comprobantes registrados con ese tipo. Corresponde al campo **Prefijo** del formulario. |
| Columna **Periodo** | Tabla principal | Muestra la modalidad de numeración configurada para ese tipo: **Anual** o **Mensual**. |
| Columna **Acciones** | Tabla principal | Contiene el icono de **lápiz**, que abre la ventana de edición, y el icono de **papelera**, que elimina el tipo de documento. |

**Identificación visual de los tipos reservados:** en las filas de `SI` (Saldos Iniciales) y `CA` (Cierre de Año) la columna **Acciones** aparece vacía, sin icono de lápiz ni de papelera. Es la forma en que la pantalla indica que son tipos reservados que no se pueden editar ni eliminar.

## Numeración de comprobantes (consecutivos)

Al crear un comprobante, el sistema le asigna un número consecutivo tomando como base el código del tipo de documento seleccionado. Zoe soporta **dos esquemas de numeración**, y cada tipo de documento se configura de forma independiente.

| Esquema | Reinicio del consecutivo | Formato del número | Ejemplo |
| --- | --- | --- | --- |
| **Anual** (por defecto) | Una vez al año, al comenzar el período fiscal | `CÓDIGO-N` | `PP-1` |
| **Mensual** | Cada mes, de enero a diciembre | `CÓDIGO-MES-N` | `PP-EN-1` |

### Modalidad ANUAL (por defecto)

El consecutivo **inicia en 1 al comienzo del período fiscal** y se incrementa de forma continua hasta N durante todo el año, **independientemente de la fecha o el mes de registro** del comprobante.

**Ejemplo:** en un tipo de documento con código `PP` (Pago a Proveedores), el primer comprobante del año queda numerado como `PP-1`. El siguiente comprobante de ese mismo tipo será `PP-2`, sin importar si se registra en febrero o en noviembre. La numeración es una única secuencia que recorre el año fiscal completo.

Es la modalidad que traen los tipos de documento por defecto.

### Modalidad MENSUAL

El consecutivo **se reinicia en 1 al inicio de cada mes** (de enero a diciembre). El número incluye la abreviatura del mes y **la numeración se asigna según la fecha del comprobante**, no según la fecha en que se digita.

**Ejemplos:**

- `PP-EN-1`: primer comprobante de Pago a Proveedores registrado en enero.
- `CONBAN-DC-1`: primera Conciliación Bancaria registrada en diciembre.
- `CCM-SP-1`: primer comprobante de un tipo «Cierre Contable Mensual» (prefijo `CCM`, periodo Mensual) registrado con fecha del 1 de septiembre. El número se visualiza en la columna **Nro. Comprobante** de la pantalla `Contabilidad > Comprobantes`.

**Estructura del número:** `PREFIJO` + `-` + `ABREVIATURA DEL MES` (dos letras) + `-` + `CONSECUTIVO DEL MES`.

**Abreviaturas de los meses:** son de dos letras y no siempre corresponden a las dos primeras letras del nombre del mes. Abreviaturas confirmadas: `EN` (enero), `SP` (septiembre), `DC` (diciembre).

Cada mes mantiene su propia secuencia independiente. Como el mes lo determina la fecha del comprobante, un comprobante digitado en diciembre pero fechado en enero toma el consecutivo correspondiente a enero.

### Dónde se configura la modalidad

La modalidad de numeración se define **por cada tipo de documento**, no de forma global para la empresa o el año fiscal:

- **Visualización:** la columna **Periodo** de la tabla principal muestra si el consecutivo de cada tipo es Anual o Mensual.
- **Configuración:** en el campo **Periodo** de la ventana de creación (**+ Nuevo**) o de edición (icono de lápiz de la columna **Acciones**). Es una lista desplegable con dos opciones: **Mensual** y **Anual**.

Es válido que en un mismo año fiscal convivan tipos de documento con numeración anual y tipos con numeración mensual.

### Número inicial del consecutivo

El valor desde el que arranca la numeración también es configurable, y el formulario cambia según la modalidad seleccionada en el campo **Periodo**:

| Modalidad seleccionada | Campo que muestra el formulario | Contenido |
| --- | --- | --- |
| **Anual** | **Consecutivo anual** (obligatorio) | Un único campo con el número desde el que inicia la secuencia del año fiscal. Valor por defecto: `1`. |
| **Mensual** | Bloque **Consecutivos mensuales** (obligatorio) | Doce campos, uno por cada mes (Enero a Diciembre), con el número desde el que inicia la secuencia de ese mes. Valor por defecto de cada uno: `1`. |

**Caso de uso de un valor distinto de 1:** continuar la numeración proveniente de otro sistema contable durante una migración, en lugar de reiniciar los consecutivos desde uno.

## Tipos de documento por defecto del año fiscal

Al crear o habilitar un nuevo año fiscal, la plataforma **genera automáticamente** los tipos de asiento base necesarios para la operación contable. No requieren configuración previa por parte del usuario.

| Código | Nombre | Tipo / Uso | Reglas de edición |
| --- | --- | --- | --- |
| `SI` | Saldos Iniciales | INITIAL | Tipo reservado. No se puede editar. |
| `CA` | Cierre de Año | FINAL | Tipo reservado. No se puede editar. |
| `NC` | Nota de Contabilidad | NORMAL | Editable / Uso general |
| `CI` | Comprobante de Ingreso | NORMAL | Editable / Uso general |
| `CE` | Comprobante de Egreso | NORMAL | Editable / Uso general |
| `NOBAN` | Notas Bancarias | NORMAL | Editable / Uso general |
| `CONBAN` | Conciliación Bancaria | NORMAL | Editable / Uso general |
| `GADIV` | Gastos Diversos | NORMAL | Editable / Uso general |
| `GANOM` | Gastos de Nómina | NORMAL | Editable / Uso general |
| `PROIMP` | Provisión de Impuestos | NORMAL | Editable / Uso general |

### Tipos reservados

Dos de los tipos por defecto están protegidos porque de ellos dependen la apertura y el cierre contable del año fiscal:

- **`SI` (Saldos Iniciales), de tipo `INITIAL`:** registra los saldos con los que abre el año fiscal.
- **`CA` (Cierre de Año), de tipo `FINAL`:** registra el asiento de cierre del período.

Ambos son **tipos reservados y no se pueden editar**. Los ocho tipos restantes son de tipo `NORMAL`, editables y de uso general.

## Crear un tipo de documento

Cuando la operación de la empresa requiere clasificaciones que no cubren los tipos por defecto (por ejemplo, pagos a proveedores, caja menor o legalización de anticipos), se crean tipos de documento personalizados.

Al seleccionar el botón **+ Nuevo** se abre la ventana **Nuevo tipo de documento**, con el subtítulo «Crea un nuevo tipo de documento contable».

**Campos del formulario:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Nombre** | Texto | Sí | Nombre descriptivo del tipo de documento (por ejemplo, «Cierre Contable Mensual»). |
| **Prefijo** | Texto | Sí | Código corto que encabeza el consecutivo de los comprobantes (por ejemplo, `CCM`). Es el valor que se muestra en la columna **Código** de la tabla principal. |
| **Periodo** | Lista desplegable | Sí | Modalidad de numeración del consecutivo. Opciones: **Mensual** y **Anual**. |
| **Consecutivo anual** | Numérico | Sí, si **Periodo** = Anual | Número desde el que inicia la secuencia del año fiscal. Valor por defecto: `1`. |
| **Consecutivos mensuales** | Doce campos numéricos (Enero a Diciembre) | Sí, si **Periodo** = Mensual | Número desde el que inicia la secuencia de cada mes. Valor por defecto de cada campo: `1`. |
| **Cancelar** | Botón | — | Cierra la ventana sin guardar. |
| **Crear** | Botón | — | Guarda el nuevo tipo de documento. |

**Pasos:**

1. Ir a `Contabilidad > Configuración > Tipos de documento`.
2. Seleccionar el botón **+ Nuevo**, ubicado en la parte superior derecha de la tabla.
3. Diligenciar el campo **Nombre**.
4. Diligenciar el campo **Prefijo**. Se recomienda que sea corto y reconocible (por ejemplo, `PP` para Pago a Proveedores).
5. Seleccionar la modalidad en el campo **Periodo**: Mensual o Anual.
6. Definir el número inicial en el campo **Consecutivo anual** o en el bloque **Consecutivos mensuales**, según la modalidad seleccionada. Se dejan en `1` salvo que se requiera continuar una numeración anterior.
7. Seleccionar el botón **Crear**.

Resultado: el tipo de documento queda disponible de inmediato para registrar comprobantes en ese año fiscal, y aparece en la tabla principal con su modalidad reflejada en la columna **Periodo**.

## Editar un tipo de documento

Para modificar un tipo de documento existente se utiliza el **icono de lápiz** de la columna **Acciones**. Se abre la ventana **Editar tipo de documento**, con el subtítulo «Modifica la configuración del tipo de documento».

El formulario es el mismo de la creación (**Nombre**, **Prefijo**, **Periodo** y los campos de consecutivo correspondientes a la modalidad). El botón de confirmación se llama **Actualizar** en lugar de **Crear**.

**Eliminar:** el **icono de papelera** de la columna **Acciones** elimina el tipo de documento.

**Restricción:** los tipos reservados `SI` (INITIAL) y `CA` (FINAL) no se pueden editar ni eliminar. Sus filas no muestran ningún icono en la columna **Acciones**.

**Advertencia:** cambiar la modalidad de numeración de un tipo de documento que ya tiene comprobantes registrados hace que convivan dos formatos de consecutivo distintos dentro del mismo año fiscal, lo que dificulta la búsqueda y la trazabilidad. La modalidad debe definirse antes de empezar a registrar comprobantes con ese tipo.

## Asientos de integración (tipos API)

Los **tipos API**, también llamados **asientos de integración**, son tipos de documento **reservados para sistemas externos**. No los crea ni los administra el usuario: la plataforma los utiliza para registrar los comprobantes que llegan desde otras aplicaciones.

**Caso de uso principal:** la sincronización automática de facturación desde la versión de escritorio **Optimun** hacia **Zoe Contable**. Cada documento que se sincroniza entre los dos sistemas se registra con su tipo de integración, lo que permite distinguir los asientos generados automáticamente de los registrados manualmente por un usuario.

**Cómo consultarlos:** se marca la casilla **Ver Tipos API**, ubicada en la parte superior de la pantalla, junto al botón **Filtrar**. Al marcarla, la tabla deja de mostrar los tipos de documento normales y pasa a mostrar los tipos de integración. Para volver al listado habitual se desmarca la casilla.

**Nomenclatura:** los códigos de los tipos API comienzan por la letra `I` (de integración). Ejemplos observados: `IFC` (Factura De Compra), `INCFC` (Nota Crédito De Factura De Compra), `INDFC` (Nota Débito De Factura De Compra), `IPP` (Pago De Proveedores), `IFV` (Factura De Venta), `INCFV` (Nota Crédito De Factura De Venta), `INDFV` (Nota Débito De Factura De Venta), `IDS` (Documento Soporte), `IADS` (Ajuste Documento Soporte), `INOM` (Nómina).

**Restricciones:** son registros de **solo consulta**. Su columna **Acciones** aparece vacía: no tienen icono de lápiz ni de papelera, por lo que no pueden editarse ni eliminarse. Pueden revisarse para identificar el origen de un comprobante.

## Comportamiento al abrir un año fiscal nuevo

Al agregar un nuevo año fiscal, la plataforma **genera únicamente los tipos de documento por defecto del sistema**.

**Los tipos de asiento personalizados creados por el usuario en el año fiscal anterior NO se copian al año nuevo.**

Este comportamiento es distinto al del PUC, que sí puede copiarse desde un año anterior con la opción **Cargar Puc Año Anterior**. En el caso de los tipos de documento no existe una función de copia entre años: los tipos personalizados deben volverse a crear manualmente en el año nuevo con el botón **+ Nuevo**.

**Recomendación:** documentar la estructura de tipos personalizados de la empresa (código, nombre y modalidad de numeración de cada uno) para poder reproducirla de forma idéntica en el año fiscal siguiente y mantener la comparabilidad de los consecutivos entre años.

## Solución de problemas

### Los tipos de documento personalizados no aparecen en el año fiscal nuevo

Es el comportamiento esperado: al agregar un año fiscal solo se generan los tipos por defecto del sistema, y los tipos personalizados del año anterior no se copian. Solución: volver a crearlos con el botón **+ Nuevo**.

### El consecutivo no se reinicia al comenzar el mes

El tipo de documento está configurado con modalidad **Anual**, en la que el consecutivo corre de forma continua durante todo el año fiscal. Verificar la columna **Periodo** de la tabla principal y, si corresponde, cambiar la modalidad a **Mensual** desde el icono de lápiz.

### Un comprobante quedó con un mes distinto al esperado en su consecutivo

En la modalidad Mensual el mes del consecutivo lo determina la **fecha del comprobante**, no la fecha de digitación. Verificar la fecha con la que se registró el comprobante.

### No se puede editar el tipo de documento SI o CA

Son tipos reservados: `SI` es de tipo `INITIAL` y `CA` es de tipo `FINAL`. La plataforma los protege porque de ellos dependen la apertura y el cierre contable del año fiscal.

### Aparecen comprobantes con un tipo de documento que nadie creó

Probablemente correspondan a asientos de integración generados por un sistema externo. Consultarlos marcando la casilla **Ver Tipos API** de la parte superior de la pantalla.

### No se encuentra un tipo de documento que sí fue creado

Verificar que se esté trabajando en el **año fiscal correcto**, porque los tipos de documento pertenecen al año fiscal en el que fueron creados.

## Resumen de reglas de negocio

| # | Regla |
| --- | --- |
| 1 | Los tipos de documento (tipos de asiento) clasifican y organizan los comprobantes contables registrados en el sistema. |
| 2 | Los tipos de documento pertenecen al año fiscal. Cada año fiscal tiene su propia tabla. |
| 3 | Al crear o habilitar un año fiscal, la plataforma genera automáticamente los tipos de documento por defecto. |
| 4 | Los tipos de documento personalizados no se copian de un año fiscal al siguiente. |
| 5 | El código del tipo de documento es el prefijo del consecutivo del comprobante. |
| 6 | La modalidad de numeración es **Anual** por defecto: el consecutivo inicia en 1 con el período fiscal y se incrementa hasta N durante todo el año, independientemente del mes de registro. |
| 7 | En la modalidad **Mensual** el consecutivo se reinicia en 1 al inicio de cada mes y el número incluye la abreviatura del mes. |
| 8 | En la modalidad Mensual el consecutivo se asigna según la fecha del comprobante, no según la fecha de digitación. |
| 9 | La modalidad de numeración se configura por cada tipo de documento, al crearlo (**+ Nuevo**) o al editarlo (icono de lápiz), y se visualiza en la columna **Periodo**. |
| 10 | Los tipos reservados `SI` (INITIAL, saldos iniciales) y `CA` (FINAL, cierre de año) no se pueden editar. |
| 11 | Los tipos API o asientos de integración están reservados para sistemas externos, como la sincronización de facturación desde Optimun de escritorio hacia Zoe Contable. |
| 12 | Los tipos API se consultan marcando la casilla **Ver Tipos API**, junto al botón **Filtrar**, y son de solo lectura: su columna **Acciones** aparece vacía. |
| 13 | El campo del formulario que define el código se llama **Prefijo**; en la tabla principal ese valor se muestra en la columna **Código**. |
| 14 | El número inicial del consecutivo es configurable: un campo **Consecutivo anual** en la modalidad Anual, o doce campos **Consecutivos mensuales** (Enero a Diciembre) en la modalidad Mensual. Todos vienen en `1` por defecto. |
| 15 | Los tipos de documento no reservados se pueden eliminar con el icono de papelera de la columna **Acciones**. |
| 16 | En la modalidad Mensual el número tiene la estructura `PREFIJO-MES-CONSECUTIVO`, donde el mes es una abreviatura de dos letras que no siempre coincide con las dos primeras del nombre (`SP` para septiembre, `DC` para diciembre). |
| 17 | El consecutivo asignado se visualiza en la columna **Nro. Comprobante** de la pantalla `Contabilidad > Comprobantes`. |

## Preguntas frecuentes

**¿Qué son los tipos de documento o tipos de asiento?**
Son la clasificación con la que Zoe organiza los comprobantes contables. Cada comprobante se registra con un tipo de documento, que define su categoría y el prefijo de su consecutivo.

**¿Los tipos de documento personalizados se migran de un año a otro?**
No. Al agregar un nuevo año fiscal, no se copian los tipos de asiento personalizados creados por el usuario en el año fiscal anterior; únicamente se generan los tipos por defecto del sistema.

**¿Qué esquemas de numeración soporta Zoe?**
Dos: **Anual**, que es la modalidad por defecto y mantiene un consecutivo continuo durante todo el año fiscal, y **Mensual**, que reinicia el consecutivo en 1 al inicio de cada mes.

**¿Dónde se ve si un tipo de documento es anual o mensual?**
En la columna **Periodo** de la tabla principal de `Contabilidad > Configuración > Tipos de documento`.

**¿Dónde se cambia la modalidad de numeración?**
Al crear el tipo de documento con el botón **+ Nuevo**, o al editarlo con el icono de lápiz de la columna **Acciones**.

**¿El consecutivo siempre empieza en 1?**
Por defecto sí, pero es configurable. En la modalidad Anual el formulario muestra el campo **Consecutivo anual**, y en la modalidad Mensual muestra doce campos (**Consecutivos mensuales**, de Enero a Diciembre). Todos vienen con el valor `1` y pueden modificarse, por ejemplo para continuar la numeración de un sistema anterior durante una migración.

**¿Cómo se llama el campo donde se escribe el código del tipo de documento?**
En el formulario de creación y edición el campo se llama **Prefijo**. En la tabla principal, ese mismo valor se muestra en la columna **Código**.

**¿Se puede eliminar un tipo de documento?**
Sí, con el icono de papelera de la columna **Acciones**, salvo en los tipos reservados `SI` y `CA`, cuyas filas no muestran iconos de acción.

**¿La modalidad de numeración es igual para todos los tipos de documento?**
No. Se configura de forma individual por tipo de documento, de modo que en un mismo año fiscal pueden convivir tipos anuales y tipos mensuales.

**¿Dónde se ve el consecutivo que quedó asignado a un comprobante?**
En la columna **Nro. Comprobante** de la pantalla `Contabilidad > Comprobantes`.

**¿Qué significan las letras del medio en un número como `CCM-SP-1`?**
Son la abreviatura de dos letras del mes al que pertenece el comprobante: `SP` es septiembre. El número se compone del prefijo del tipo de documento, la abreviatura del mes y el consecutivo de ese mes. Las abreviaturas no siempre son las dos primeras letras del nombre del mes.

**¿En la modalidad mensual, qué fecha determina el consecutivo?**
La fecha del comprobante. Un comprobante digitado en un mes pero fechado en otro toma el consecutivo del mes de su fecha.

**¿Por qué no se pueden editar los tipos SI y CA?**
Porque son tipos reservados del sistema: `SI` (INITIAL) registra los saldos iniciales del año fiscal y `CA` (FINAL) registra el cierre del año. De ellos dependen la apertura y el cierre contable.

**¿Qué son los asientos de integración o tipos API?**
Son tipos de documento reservados para sistemas externos, como la sincronización automática de facturación desde la versión de escritorio Optimun hacia Zoe Contable.

**¿Cómo se consultan los tipos API?**
Marcando la casilla **Ver Tipos API**, ubicada en la parte superior de la pantalla junto al botón **Filtrar**. La tabla pasa a mostrar los registros protegidos en modo de solo consulta.

**¿Se pueden editar los tipos API?**
No. Son registros protegidos que administra la plataforma; solo pueden consultarse.

**¿Una empresa nueva trae tipos de documento cargados?**
Sí. A diferencia del PUC, que nace vacío, la tabla de tipos de documento se precarga automáticamente con los tipos por defecto del sistema.
