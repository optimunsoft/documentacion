---
title: Centros de costo
description: Clasificación analítica de ingresos, costos y gastos por área, sede, proyecto o departamento en los asientos contables. Cubre la pantalla de Centros de Costo, la creación y edición de registros, la exigencia del dato desde el campo Solicitar del PUC, su captura al registrar comprobantes, el filtrado de reportes y el Balance de Comprobación agrupado por centro de costo, y la regla de que los centros de costo no se migran al habilitar un año fiscal nuevo.
module: contabilidad
category: configuracion
slug: centros-costo
order: 7
tags:
  - configuracion
  - centros-de-costo
  - centro-de-costo
  - puc
  - plan-unico-de-cuentas
  - solicitar
  - cuenta-auxiliar
  - asientos-contables
  - comprobantes
  - balance-de-comprobacion
  - reportes-contables
  - control-contable
  - clasificacion-analitica
  - nuevo-ano-fiscal
  - ano-fiscal
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-03
---

# Centros de costo

Los centros de costo son la propiedad de clasificación analítica con la que Zoe segmenta ingresos, costos y gastos por áreas, proyectos, sedes o departamentos dentro de los asientos contables. Son una herramienta de control interno y seguimiento contable: no modifican los estados financieros oficiales ni la información que se reporta a la DIAN, sino que agregan una dimensión de análisis definida por cada empresa. Este documento explica dónde está la pantalla, cómo se crean y editan los centros de costo, cómo se activa su exigencia desde el Plan Único de Cuentas, cómo se capturan al registrar un comprobante, qué reportes los aprovechan y qué ocurre con ellos al habilitar un año fiscal nuevo.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Concepto: qué es un centro de costo](#concepto-qué-es-un-centro-de-costo)
4. [Contexto por año fiscal](#contexto-por-año-fiscal)
5. [Elementos de la pantalla](#elementos-de-la-pantalla)
6. [Crear un centro de costo](#crear-un-centro-de-costo)
7. [Editar y eliminar un centro de costo](#editar-y-eliminar-un-centro-de-costo)
8. [Vinculación con el Plan Único de Cuentas (PUC)](#vinculación-con-el-plan-único-de-cuentas-puc)
9. [Captura del centro de costo en el comprobante](#captura-del-centro-de-costo-en-el-comprobante)
10. [Reportes e impacto financiero](#reportes-e-impacto-financiero)
11. [Comportamiento al abrir un año fiscal nuevo](#comportamiento-al-abrir-un-año-fiscal-nuevo)
12. [Solución de problemas](#solución-de-problemas)
13. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
14. [Preguntas frecuentes](#preguntas-frecuentes)

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Centros de Costo`.
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / CENTROS DE COSTO`.
- **Título de la pantalla:** «Centros de Costo».
- **Subtítulo de la pantalla:** «Configura y gestiona los centros de costo de tu empresa».
- **Contenido de la pantalla:** una tarjeta titulada «Centros de costo» con la tabla de los centros de costo registrados en el año fiscal activo.

## Requisitos previos

- Tener una empresa creada y seleccionada en Zoe.
- Tener acceso al módulo de Contabilidad.
- Saber en qué año fiscal se está trabajando, porque los centros de costo que se muestran y se crean pertenecen a ese año.
- Para que el dato se exija al registrar comprobantes, tener cargado el Plan Único de Cuentas del año fiscal.

## Concepto: qué es un centro de costo

Un centro de costo es una etiqueta de clasificación que se asocia a un movimiento contable para identificar a qué unidad de la empresa pertenece. La cuenta del PUC indica la naturaleza del movimiento (qué ocurrió) y el centro de costo indica su origen organizacional (dónde ocurrió).

Su función es segmentar ingresos, costos y gastos por áreas, proyectos, sedes o departamentos, de modo que la información contable pueda analizarse por unidad y no únicamente como un total consolidado. Es una herramienta de control interno y seguimiento contable, definida por cada empresa según su operación.

**Criterios habituales de segmentación:**

| Criterio | Ejemplos | Uso analítico |
| --- | --- | --- |
| Área o departamento | Administración, Ventas, Producción, Logística | Determinar el gasto de cada departamento. |
| Sede o punto | Sede Norte, Sede Sur, Bodega Principal | Comparar el desempeño entre sucursales. |
| Proyecto | Proyecto Torre A, Contrato Municipio, Obra 2026 | Medir el costo total de un proyecto de duración plurimensual. |
| Línea de negocio | Servicios, Comercialización, Mantenimiento | Evaluar el margen por línea. |

**Alcance:** los centros de costo no alteran los estados financieros oficiales ni la información exógena. Constituyen una capa de análisis adicional sobre los mismos movimientos contables.

## Contexto por año fiscal

Los centros de costo pertenecen al **año fiscal**, no a la empresa. Cada año fiscal tiene su propia lista de centros de costo.

| Información | Alcance |
| --- | --- |
| Centros de costo | Por año fiscal |
| PUC (Plan Único de Cuentas) | Por año fiscal |
| Tipos de documento | Por año fiscal |
| Comprobantes | Por año fiscal |
| Terceros | Global |

**Consecuencia práctica:** un centro de costo creado en un año fiscal solo existe en ese año. Ver [Comportamiento al abrir un año fiscal nuevo](#comportamiento-al-abrir-un-año-fiscal-nuevo).

## Elementos de la pantalla

La pantalla presenta una tabla en la que cada fila corresponde a un centro de costo del año fiscal activo.

**Columnas de la tabla:**

| Columna | Descripción |
| --- | --- |
| **ID** | Identificador numérico asignado automáticamente por la plataforma. No lo digita el usuario. |
| **Nombre** | Nombre descriptivo del centro de costo. Es el valor que se muestra en los comprobantes y en los reportes. |

**Controles de la pantalla:**

| Control | Ubicación | Descripción |
| --- | --- | --- |
| **Consultar** | Parte superior | Campo de texto para buscar un centro de costo por su nombre. |
| **Filtrar** | Junto a **Consultar** | Ejecuta la búsqueda según el criterio ingresado. |
| **Nuevo** | Sobre la tabla, a la derecha | Abre la ventana de creación de un centro de costo. |
| **Columnas** | Sobre la tabla, a la derecha | Permite mostrar u ocultar columnas de la tabla. |
| **Acciones** | En cada fila | Permite editar o eliminar el centro de costo. |
| **Paginación** | Debajo de la tabla | Navegación entre páginas y selección de registros por página. |

**Estado vacío:** cuando el año fiscal no tiene centros de costo registrados, la tabla muestra el mensaje «Sin registros». Es el estado inicial de todo año fiscal, porque la plataforma no crea centros de costo por defecto.

## Crear un centro de costo

La plataforma **no crea centros de costo por defecto**: no los genera al habilitar la empresa ni al iniciar un año fiscal nuevo. Todos los centros de costo los define el usuario.

Al seleccionar el botón **Nuevo** se abre la ventana **Nuevo centro de costo**, con el subtítulo «Crea un nuevo centro de costo para tu empresa».

**Campos del formulario:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Nombre** | Texto | Sí | Nombre descriptivo del centro de costo (por ejemplo, «Ventas» o «Administración»). |
| **Cancelar** | Botón | — | Cierra la ventana sin guardar. |
| **Crear** | Botón | — | Guarda el nuevo centro de costo. |

El formulario no solicita código, naturaleza ni cuenta contable asociada: el identificador lo asigna la plataforma.

**Pasos:**

1. Ir a `Contabilidad > Configuración > Centros de Costo`.
2. Verificar que el año fiscal activo sea el correcto.
3. Seleccionar el botón **Nuevo**.
4. Diligenciar el campo **Nombre**.
5. Seleccionar el botón **Crear**.

Resultado: el centro de costo queda disponible de inmediato para asociarlo a los movimientos de los comprobantes de ese año fiscal, y aparece en la tabla principal con el ID asignado.

**Recomendación de nomenclatura:** los nombres de los centros de costo aparecen en cada comprobante y en cada reporte del año, y son el criterio con el que se comparan las unidades entre sí. Conviene definirlos con un mismo criterio y mantenerlos estables a lo largo del año fiscal.

## Editar y eliminar un centro de costo

Desde las acciones de cada fila se abre la ventana **Editar centro de costo**, con el subtítulo «Modifica la información del centro de costo».

El formulario es el mismo de la creación (campo **Nombre**). El botón de confirmación se llama **Actualizar** en lugar de **Crear**.

**Eliminar:** las acciones de la fila también permiten eliminar el centro de costo.

**Efecto del cambio de nombre:** los movimientos de los comprobantes quedan asociados al centro de costo por su ID, no por su nombre. Al modificar el nombre, el cambio se refleja también en los movimientos ya registrados. Por eso la edición sirve para corregir el nombre de un centro de costo existente, pero no para reutilizar un registro con un significado distinto a mitad de año fiscal: los movimientos anteriores quedarían agrupados bajo la nueva etiqueta.

## Vinculación con el Plan Único de Cuentas (PUC)

La exigencia del centro de costo **no se configura en la pantalla de Centros de Costo**, sino en las cuentas contables del Plan Único de Cuentas.

En `Contabilidad > Configuración > PUC`, las ventanas **Nueva cuenta** y **Editar cuenta** («Modifica la información de la cuenta contable») contienen el campo **Solicitar**, cuyo desplegable ofrece dos valores: **Centro de costo** y **Tercero**. Cuando en una cuenta se selecciona **Centro de costo** y se confirma con **Actualizar** (o **Crear**, si la cuenta es nueva), la plataforma obliga a seleccionar un centro de costo cada vez que esa cuenta se utiliza en un asiento contable.

**Reglas del campo Solicitar:**

| # | Regla |
| --- | --- |
| 1 | El campo **Solicitar** solo aparece cuando la cuenta está marcada con la casilla **¿Es auxiliar?**, porque las cuentas auxiliares son las que reciben los movimientos. |
| 2 | El campo admite **Tercero**, **Centro de costo** o ambos valores en la misma cuenta. Cada marca exige su dato de forma independiente en el comprobante. |
| 3 | La marca vive en la cuenta del PUC del año fiscal correspondiente. |

**Criterio de uso:** se marca **Centro de costo** en las cuentas cuyo movimiento tiene sentido segmentar por unidad organizacional, típicamente cuentas de gasto, de costo o de ingreso (gastos de personal, servicios públicos, arrendamientos, mantenimiento, ingresos por línea de negocio). No aporta valor analítico en cuentas de bancos, cuentas por pagar u otras cuentas de balance sin dimensión organizacional.

## Captura del centro de costo en el comprobante

Al registrar un comprobante en `Contabilidad > Comprobantes`, el bloque **Detalle del asiento** contiene la tabla **Cuentas del asiento**, con una línea por movimiento. Sus columnas son **ID**, **Cuenta**, **Concepto**, **Factura**, **Tercero**, **C. Costo**, **Débito**, **Crédito** y **Acciones**.

Cuando la cuenta seleccionada en una línea está marcada con **Solicitar > Centro de costo**, la celda de la columna **C. Costo** de esa línea se habilita. Al abrirla despliega la lista de los centros de costo del año fiscal activo, con un campo **Buscar** en la parte superior para filtrarla. El usuario selecciona el que corresponde y continúa con el asiento.

**Estado «No requerido»:** en las líneas cuya cuenta no exige un dato, la celda correspondiente muestra el texto **No requerido** en gris y no admite valor. Cada columna responde de forma independiente a lo que tenga marcado la cuenta en el campo **Solicitar**: si la cuenta exige los dos valores, la línea pide **Tercero** y **C. Costo** simultáneamente.

**Ejemplo:** en un asiento con la cuenta `510506 - Sueldos` (marcada únicamente con Centro de costo) y la cuenta `110505 - Caja general` (marcada únicamente con Tercero), la primera línea pide **C. Costo** y muestra **No requerido** en **Tercero**; la segunda línea hace lo contrario.

Si la celda exige el dato y se deja vacía, la plataforma no permite guardar el comprobante: esa es la función de la marca configurada en el PUC.

**Lista vacía en el desplegable:** si el campo aparece sin opciones, el año fiscal activo no tiene centros de costo creados. Deben crearse en `Contabilidad > Configuración > Centros de Costo` antes de continuar con el comprobante.

## Reportes e impacto financiero

La información capturada en los comprobantes es la que hace utilizables los centros de costo en los reportes contables.

**Filtrado de reportes:** varios reportes contables permiten acotar la consulta a un centro de costo, para obtener únicamente los movimientos de esa unidad.

**Balance de Comprobación agrupado por centro de costo:** en la ventana de parámetros del Balance de Comprobación, el campo opcional **Filtrado por** —cuyo valor predeterminado es **No aplica**— permite seleccionar **Centro de costo**, de modo que el reporte se genera agrupado por centro de costo para el análisis por áreas o departamentos. El resto de parámetros del reporte (año fiscal, tipo de balance, rango de cuentas y formato de descarga) se describen en el documento de reportes básicos.

**Limitación:** los reportes solo pueden mostrar la información que se capturó en el momento de registrar cada comprobante. Los movimientos registrados antes de marcar la cuenta con **Solicitar > Centro de costo** no tienen centro de costo asignado y aparecerán sin clasificar. Por esa razón conviene definir los centros de costo y marcar las cuentas al inicio del año fiscal.

## Comportamiento al abrir un año fiscal nuevo

**Los centros de costo no se migran ni se copian de un año fiscal a otro.** Al habilitar un año fiscal nuevo, la plataforma no traslada los centros de costo del año anterior. El año nuevo inicia con la lista vacía y los centros de costo deben crearse nuevamente para el período.

Esto los diferencia del PUC, que sí puede copiarse desde el año anterior mediante la opción disponible en la pantalla del Plan Único de Cuentas, y de los tipos de documento, que se precargan automáticamente con los tipos por defecto del sistema.

**Implicación para la comparación entre años:** para poder comparar una misma unidad entre dos años fiscales, los centros de costo deben recrearse con los mismos nombres. Se recomienda documentar la lista de centros de costo del año antes del cierre, de manera que pueda reproducirse íntegramente en el año siguiente.

**Nota sobre la marca del PUC:** si el Plan Único de Cuentas del año nuevo se copia desde el año anterior, la marca **Solicitar > Centro de costo** viaja con las cuentas. Sin embargo, los valores que ofrecerá el desplegable en los comprobantes serán los centros de costo del año nuevo, que deben crearse por separado.

## Solución de problemas

### La lista de centros de costo aparece vacía en el año fiscal nuevo

Es el comportamiento esperado. Los centros de costo no se migran de un año fiscal a otro. Deben crearse nuevamente con el botón **Nuevo**.

### La pantalla muestra «Sin registros» en una empresa recién creada

Es el comportamiento esperado. La plataforma no crea centros de costo por defecto al habilitar la empresa. La lista inicia vacía y los define el usuario.

### Un comprobante exige seleccionar un centro de costo

La cuenta utilizada en el movimiento tiene el valor **Centro de costo** en el campo **Solicitar** de su configuración en el PUC. Debe diligenciarse el dato o, si la exigencia no corresponde a esa cuenta, retirarse la marca desde `Contabilidad > Configuración > PUC`.

### El desplegable de centro de costo aparece vacío en el comprobante

El año fiscal activo no tiene centros de costo creados. Deben crearse en `Contabilidad > Configuración > Centros de Costo`.

### La columna C. Costo de una línea del comprobante muestra «No requerido»

La cuenta de esa línea no está marcada con **Solicitar > Centro de costo** en el PUC. Si el dato debe capturarse en esa cuenta, la marca se agrega desde `Contabilidad > Configuración > PUC`.

### El campo Solicitar no aparece en la cuenta del PUC

El campo **Solicitar** solo se muestra en las cuentas marcadas con la casilla **¿Es auxiliar?**, que son las que reciben movimientos contables.

### El reporte por centro de costo aparece incompleto

Los reportes solo reflejan la información capturada al registrar cada comprobante. Los movimientos registrados antes de marcar la cuenta con **Solicitar > Centro de costo** no tienen el dato asignado.

### No se encuentra un centro de costo que sí fue creado

Debe verificarse el año fiscal activo: los centros de costo pertenecen al año fiscal en el que se crearon.

## Resumen de reglas de negocio

| # | Regla |
| --- | --- |
| 1 | Los centros de costo son una propiedad de clasificación analítica que segmenta ingresos, costos y gastos por áreas, proyectos, sedes o departamentos en los asientos contables. |
| 2 | Son una herramienta de control interno y seguimiento contable: no modifican los estados financieros oficiales ni la información exógena. |
| 3 | Los centros de costo pertenecen al año fiscal. Cada año fiscal tiene su propia lista. |
| 4 | La plataforma no crea centros de costo por defecto: ni al habilitar la empresa, ni al iniciar un año fiscal nuevo. La lista inicia siempre vacía. |
| 5 | Al habilitar un año fiscal nuevo, los centros de costo del año anterior no se migran ni se copian: deben crearse nuevamente para el nuevo período. |
| 6 | El formulario de creación y edición tiene un único campo obligatorio: **Nombre**. El identificador (**ID**) lo asigna automáticamente la plataforma. |
| 7 | La tabla principal tiene dos columnas: **ID** y **Nombre**. |
| 8 | La exigencia del centro de costo se activa desde la configuración de las cuentas contables en el PUC, mediante el campo **Solicitar**. |
| 9 | Al marcar una cuenta contable con **Solicitar > Centro de costo**, la plataforma obliga a seleccionar un centro de costo al registrar esa cuenta en un asiento contable. |
| 9.1 | En el comprobante, el dato se captura en la columna **C. Costo** de la tabla **Cuentas del asiento**. Su desplegable incluye un campo **Buscar** para filtrar la lista. |
| 9.2 | En las líneas cuya cuenta no exige el dato, la celda de **C. Costo** (o la de **Tercero**) muestra el texto **No requerido** y no admite valor. |
| 10 | El campo **Solicitar** solo aparece en cuentas marcadas como auxiliares (casilla **¿Es auxiliar?**). |
| 11 | El campo **Solicitar** admite **Tercero**, **Centro de costo** o ambos valores en la misma cuenta. Cada marca exige su dato de forma independiente. |
| 12 | Los centros de costo permiten filtrar la información en diversos reportes contables. |
| 13 | El Balance de Comprobación puede generarse agrupado por centro de costo, seleccionando **Centro de costo** en el campo **Filtrado por** de su ventana de parámetros. |
| 14 | Los reportes solo reflejan la información capturada en los comprobantes: los movimientos registrados antes de marcar la cuenta no tienen centro de costo asignado. |
| 15 | Los movimientos quedan asociados al centro de costo por su ID; al modificar el nombre, el cambio se refleja también en los movimientos ya registrados. |
| 16 | Los centros de costo se pueden editar y eliminar desde las acciones de cada fila de la tabla. |

## Preguntas frecuentes

**¿Los centros de costo se copian automáticamente al cambiar de año fiscal?**
No. Al habilitar un nuevo año fiscal, no se migran ni se copian los centros de costo del año anterior, por lo que deben crearse nuevamente para el nuevo período.

**¿Qué es un centro de costo?**
Es una propiedad de clasificación analítica que permite segmentar ingresos, costos o gastos por áreas, proyectos, sedes o departamentos dentro de los asientos contables.

**¿Los centros de costo modifican los estados financieros?**
No. Son una herramienta de control interno y seguimiento contable. Agregan una dimensión de análisis sobre los mismos movimientos, sin alterar los estados financieros oficiales ni la información exógena.

**¿Zoe trae centros de costo creados por defecto?**
No. La plataforma no crea centros de costo al habilitar la empresa ni al iniciar un año fiscal. La lista inicia vacía y la define el usuario.

**¿Dónde se crean los centros de costo?**
En `Contabilidad > Configuración > Centros de Costo`, con el botón **Nuevo**.

**¿Qué datos pide el formulario de creación?**
Un único campo obligatorio: **Nombre**. El **ID** lo asigna automáticamente la plataforma.

**¿Cómo se hace obligatorio el centro de costo al registrar un comprobante?**
Marcando la cuenta contable con el valor **Centro de costo** en el campo **Solicitar**, desde `Contabilidad > Configuración > PUC`. Con esa marca, la plataforma obliga a seleccionar un centro de costo cada vez que la cuenta se usa en un asiento contable.

**¿Por qué no aparece el campo Solicitar en una cuenta del PUC?**
Porque el campo solo se muestra en las cuentas marcadas con la casilla **¿Es auxiliar?**, que son las que reciben movimientos.

**¿Se puede exigir tercero y centro de costo en la misma cuenta?**
Sí. El campo **Solicitar** admite **Tercero**, **Centro de costo** o ambos valores. Si la cuenta tiene los dos, la línea del comprobante exigirá tanto el tercero como el centro de costo.

**¿En qué cuentas conviene exigir centro de costo?**
En las cuentas cuyo movimiento tiene sentido segmentar por unidad organizacional: gastos de personal, servicios públicos, arrendamientos, mantenimiento y cuentas de ingreso que se quieran repartir por línea de negocio.

**¿Qué reportes aprovechan los centros de costo?**
Diversos reportes contables permiten filtrar la información por centro de costo. Además, el Balance de Comprobación puede generarse agrupado por centro de costo para el análisis por áreas o departamentos.

**¿Cómo se genera el Balance de Comprobación agrupado por centro de costo?**
En la ventana de parámetros del reporte, el campo opcional **Filtrado por** —predeterminado en **No aplica**— permite seleccionar **Centro de costo**.

**¿Por qué el reporte por centro de costo aparece incompleto?**
Porque los reportes solo reflejan la información capturada al registrar cada comprobante. Los movimientos registrados antes de marcar la cuenta con **Solicitar > Centro de costo** no tienen el dato asignado.

**¿Qué pasa si se cambia el nombre de un centro de costo?**
Los movimientos quedan asociados al centro de costo por su ID, de modo que el cambio de nombre se refleja también en los movimientos ya registrados.

**¿Se puede eliminar un centro de costo?**
Sí, desde las acciones de la fila correspondiente en la tabla principal.

**¿Cómo se llama el campo del comprobante donde se registra el centro de costo?**
La columna **C. Costo** de la tabla **Cuentas del asiento**, dentro del bloque **Detalle del asiento**. Su desplegable incluye un campo **Buscar** para filtrar la lista.

**¿Qué significa «No requerido» en la columna C. Costo de un comprobante?**
Que la cuenta de esa línea no está marcada con **Solicitar > Centro de costo**, por lo que la plataforma no pide el dato. Cada columna responde de forma independiente a lo que tenga marcado la cuenta: una cuenta puede exigir solo tercero, solo centro de costo, ambos o ninguno.

**¿Por qué el desplegable de centro de costo aparece vacío al registrar un comprobante?**
Porque el año fiscal activo no tiene centros de costo creados. Deben crearse en `Contabilidad > Configuración > Centros de Costo`.

**¿Los centros de costo son iguales para todos los años fiscales de la empresa?**
No. Pertenecen al año fiscal en el que se crearon. Un centro de costo creado en un año solo existe en ese año.
