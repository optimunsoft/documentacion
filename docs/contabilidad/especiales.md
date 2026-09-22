---
title: Especiales – Comprobantes y Terceros
description: Herramientas administrativas y de mantenimiento avanzado de Contabilidad en Zoe Nube. Cubre la sección Especiales > Comprobantes (saldos iniciales, cierre anual con comprobante CA, traslado de saldos finales a iniciales, bandeja de comprobantes en proceso por integración asíncrona, activación y desactivación de edición de comprobantes, traslado masivo de saldos entre cuentas con auditoría) y Especiales > Terceros (actualización controlada de tipo y número de documento de identificación con validaciones de formato, existencia y duplicados).
module: contabilidad
category: configuracion
slug: especiales
order: 10
tags:
  - especiales
  - saldos-iniciales
  - cierre-anual
  - cierre-de-ejercicio
  - comprobante-ca
  - mover-saldos
  - mover-saldos-iniciales
  - saldos-finales
  - comprobantes-en-proceso
  - integracion-asincrona
  - optimun-escritorio
  - bloqueo-comprobante
  - edicion-comprobante
  - traslado-masivo
  - mover-saldos-entre-cuentas
  - auditoria
  - auditoria-operacion
  - terceros
  - actualizacion-documento
  - nit
  - cedula
  - documento-identificacion
  - configuracion
  - contabilidad
  - ano-fiscal
draft: false
rag_exclude: false
last_updated: 2026-09-22
---

# Especiales – Comprobantes y Terceros

La sección **Especiales** de Contabilidad en Zoe Nube agrupa las herramientas de administración y mantenimiento avanzado del módulo contable. Se divide en dos pestañas: **Comprobantes** (operaciones sobre el ciclo de vida del año fiscal y correcciones masivas) y **Terceros** (corrección controlada de documentos de identificación). Estas operaciones afectan datos contables reales y requieren permisos de administrador.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Especiales › Comprobantes](#especiales--comprobantes)
   - [Saldos Iniciales](#saldos-iniciales)
   - [Cierre Anual](#cierre-anual)
   - [Mover Saldos Finales a Iniciales](#mover-saldos-finales-a-iniciales)
   - [Comprobantes en Proceso](#comprobantes-en-proceso)
   - [Activar / Desactivar Edición de Comprobante](#activar--desactivar-edición-de-comprobante)
   - [Mover Saldos entre Cuentas](#mover-saldos-entre-cuentas)
   - [Auditoría de Operación](#auditoría-de-operación)
4. [Especiales › Terceros](#especiales--terceros)
   - [Actualización de Documento de Identificación](#actualización-de-documento-de-identificación)
5. [Errores frecuentes](#errores-frecuentes)
6. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Especiales`.
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / ESPECIALES`.
- **Título de la pantalla:** «Acciones Especiales».
- **Subtítulo de la pantalla:** «Gestiona periodos fiscales, saldos iniciales y procesos de cierre contable, además de otras opciones que sólo encontrarás aquí».
- **Contenido de la pantalla:** tres paneles — **Periodos**, **Comprobantes** y **Terceros**. Cada opción tiene un ícono de información que despliega un aviso con el efecto de la acción.

Este documento cubre los paneles **Comprobantes** y **Terceros**. El panel **Periodos** (agregar/quitar años fiscales, abrir y cerrar meses, historial de aperturas y cierres) se documenta en [Años fiscales y periodos contables](./anio-fiscal-periodos.md), que también describe la pantalla completa de Acciones Especiales y su estructura de tres paneles.

**Rutas complementarias:**

| Proceso | Ruta |
| --- | --- |
| Saldos iniciales | `Contabilidad > Configuración > Especiales > Comprobantes > Saldos iniciales` |
| Cierre anual | `Contabilidad > Configuración > Especiales > Comprobantes > Cierre anual` |
| Mover Saldos Finales a Iniciales | `Contabilidad > Configuración > Especiales > Comprobantes > Mover Saldos Finales a Iniciales` |
| Comprobantes en proceso | `Contabilidad > Configuración > Especiales > Comprobantes > Comprobantes en proceso` |
| Activar/Desactivar Edición de Comprobante | `Contabilidad > Configuración > Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante` |
| Mover saldos entre cuentas | `Contabilidad > Configuración > Especiales > Comprobantes > Mover saldos entre cuentas` |
| Auditoría de Operación | `Contabilidad > Configuración > Especiales > Comprobantes > Auditoría de Operación` |
| Actualizar documento de un tercero | `Contabilidad > Configuración > Especiales > Terceros > Actualizar documento` |

---

## Requisitos previos

- Empresa creada y seleccionada en Zoe.
- Acceso al módulo de Contabilidad con permisos de administrador.
- Año fiscal activo correctamente configurado (la mayoría de operaciones actúan sobre el año en el que está parado el usuario).
- Para el Cierre Anual: **diciembre debe estar abierto**. El CA es un comprobante con fecha del 31 de diciembre y está sujeto a las mismas validaciones de periodo que cualquier asiento; si diciembre o el año fiscal están cerrados, no se puede crear. Por eso el orden correcto es registrar el Cierre Anual **antes** de cerrar los periodos del año, no después.
- Para Mover Saldos Finales a Iniciales: el año origen debe tener su comprobante CA confirmado y estar cerrado.

---

## Especiales › Comprobantes

La pestaña **Comprobantes** reúne herramientas de mantenimiento del ciclo contable anual, integraciones externas y correcciones masivas sobre comprobantes de la empresa activa.

### Saldos Iniciales

Permite registrar o importar el comprobante de **saldos iniciales** con el tipo reservado **SI**.

**Descripción funcional:**
- Carga manual: el usuario ingresa los saldos cuenta por cuenta en la pantalla.
- Importación por Excel: el usuario descarga una plantilla, la diligencia con los saldos y la sube. El sistema valida el formato antes de crear el comprobante SI.
- El comprobante SI está vinculado al **año fiscal activo**: cambiar de año muestra o solicita el SI de ese periodo.
- Si el año ya tiene un comprobante SI, la pantalla lo muestra para edición o reemplazo.

**Conceptos clave:**
- Tipo de comprobante: `SI` (reservado, no se puede usar en comprobantes regulares).
- Contexto: aplica al año fiscal seleccionado en el momento de ejecutar la operación.

---

### Cierre Anual

Genera la propuesta automática del comprobante de **Cierre Anual** (tipo `CA`, tipo y fecha fijos). Es el paso que cierra contablemente el ejercicio fiscal.

**No abre un formulario de configuración sino un comprobante.** La opción abre la pantalla **Nuevo CA - Cierre De Año**, con el subtítulo «Complete los datos del asiento contable»: es el formulario estándar de comprobante, precargado para el cierre.

**Valores precargados del encabezado:**

| Campo | Valor |
| --- | --- |
| **Fijar mes** | Diciembre. |
| **Fecha** | 31 de diciembre del año fiscal activo. |
| **Tipo de documento** | **CA - Cierre de año**, uno de los tipos reservados de la plataforma. |
| **Descripción** | «Cierre de ejercicio fiscal [año]». |

El resto del formulario es la tabla **Cuentas del asiento** habitual (cuenta, concepto, factura, tercero, centro de costo, débito y crédito), con **Total débito**, **Total crédito** y **Diferencia**; como en cualquier asiento, la diferencia debe quedar en cero para poder grabarlo.

**Regla de negocio: el cierre anual exige diciembre abierto.** Al ser un comprobante con fecha del 31 de diciembre, está sujeto a las mismas validaciones de periodo que cualquier otro asiento. Si diciembre o el año fiscal están cerrados, el Cierre Anual no se puede crear. Ver también [Años fiscales y periodos contables](./anio-fiscal-periodos.md#cierre-anual) para la relación entre este proceso y el cierre de periodos.

**Mecanismo de generación:**
1. El sistema identifica los saldos finales de todas las cuentas de resultado (ingresos, gastos, costos y cuentas de orden aplicables).
2. Aplica movimientos inversos por cada cuenta de resultado para dejarlas en saldo cero al finalizar el año.
3. Utiliza la cuenta contrapartida **590505** para saldar el comprobante antes de la confirmación final, garantizando que el CA quede cuadrado.

**Comportamiento:**
- El comprobante CA generado es una **propuesta**: el usuario debe revisarla y confirmarla.
- Una vez confirmado el CA, el año queda listo para el traslado de saldos al año siguiente (ver [Mover Saldos Finales a Iniciales](#mover-saldos-finales-a-iniciales)).
- Después de confirmar el CA, se cierran los periodos del año (incluido diciembre) desde `Especiales > Periodos > Gestionar periodos contables`. Cerrar los periodos antes del CA obliga a reabrir diciembre para poder registrarlo.

**Conceptos clave:**
- Tipo de comprobante: `CA` (reservado, generado automáticamente).
- Cuenta contrapartida de cierre: `590505`.
- Cuentas de resultado: ingresos, gastos y similares que se zerorizan al cierre.

---

### Mover Saldos Finales a Iniciales

Traslada los saldos de cierre de un año fiscal finalizado como **saldos iniciales (SI)** al 1 de enero del periodo siguiente. No tiene relación con la apertura o el cierre de periodos: no cambia el estado de ningún mes.

Abre una ventana con el subtítulo «Transfiere saldos finales a iniciales».

**Campos de la ventana:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Año fiscal origen** | Lista desplegable | Sí | Año del que se toman los saldos finales. |
| **Año fiscal destino** | Lista desplegable | Sí | Año al que se transfieren como saldos iniciales. |
| **Cancelar** | Botón | — | Cierra la ventana sin ejecutar el proceso. |
| **Guardar** | Botón | — | Ejecuta la transferencia. |

**Independencia del año activo:** origen y destino se eligen en la propia ventana, así que el proceso puede ejecutarse desde cualquier año fiscal activo. Conviene verificar el orden de los dos campos antes de guardar, porque son visualmente idénticos.

**Validaciones previas al traslado:**
- El **año origen** debe estar cerrado con su comprobante CA confirmado.
- El **año destino** debe estar abierto y no contener un comprobante SI previo.
- Si el año destino **no tiene plan de cuentas (PUC)**, el sistema intenta copiarlo automáticamente del año origen antes de crear el comprobante SI.

**Restricciones:**
- Si el año destino ya tiene un comprobante SI (creado manualmente), el sistema rechaza el traslado para evitar duplicados. El usuario debe eliminar o limpiar ese SI antes de reintentar.

---

### Comprobantes en Proceso

Bandeja de monitoreo para comprobantes recibidos vía **integración asíncrona** desde sistemas externos (por ejemplo, Optimun Escritorio).

**Comportamiento de la integración:**
- Los comprobantes que llegan por integración **síncrona** no pasan por esta bandeja: van directo a la tabla principal de comprobantes. Sus errores se gestionan en la aplicación de origen.
- Los comprobantes **asíncronos** pasan por esta bandeja y pueden quedar en estado pendiente, procesado o con error.

**Funcionalidades de la bandeja:**
- **Filtro por estado**: pendiente, procesado, con error, etc.
- **Búsqueda por número**: localiza comprobantes por prefijo o número.
- **Revisión de reintentos**: número de intentos de procesamiento y sus marcas de tiempo.
- **Payload recibido**: estructura JSON original enviada por el sistema externo.
- **Logs de error/validación**: motivo exacto del fallo (cuenta inexistente en el PUC, tercero no registrado, etc.).
- **Marcas de tiempo**: fecha/hora de recepción y del último intento.

**Causa más frecuente de errores:** cuenta del PUC que no existe en Zoe o tercero no registrado. La corrección se hace en el sistema de origen y se reintenta el envío.

---

### Activar / Desactivar Edición de Comprobante

Bloquea o desbloquea la edición manual de un comprobante específico, identificado por su **prefijo y número** (por ejemplo, `RC-15` o `NOM-EN-1`).

**Contexto:**
- Los comprobantes que provienen de Optimun Escritorio llegan **bloqueados por defecto** para evitar discrepancias con la fuente de origen.
- Esta herramienta permite desbloquear un comprobante puntualmente para corregirlo desde Zoe Nube.

**Comportamiento:**
- La operación altera **únicamente el permiso de edición**; los datos contables del comprobante (cuentas, importes, terceros) permanecen intactos hasta que el usuario los edite manualmente.
- El cambio de estado (bloqueado / desbloqueado) es reversible.

**Aclaración necesaria: bloquear la edición de comprobantes no es cerrar un periodo.** Son mecanismos con alcances distintos:

| Mecanismo | Qué impide | Dónde se controla |
| --- | --- | --- |
| Cerrar un periodo | Registrar y modificar movimientos con fecha de ese mes. | `Especiales > Periodos > Gestionar periodos contables` |
| Activar/Desactivar Edición de Comprobante | Modificar comprobantes, con independencia del estado del periodo. | `Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante` |

Ver [Años fiscales y periodos contables](./anio-fiscal-periodos.md#distinciones-que-evitan-errores) para el resto de confusiones habituales entre cierre de periodo y cierre anual.

---

### Mover Saldos entre Cuentas

Reemplaza masivamente una **cuenta origen por una cuenta destino**, o un **tercero origen por uno destino**, en los comprobantes seleccionados. Es la herramienta para reorganizaciones del PUC o correcciones masivas de terceros mal registrados.

**Reglas de negocio:**

| Regla | Detalle |
|---|---|
| Mínimo un comprobante seleccionado | Debe marcarse al menos un comprobante antes de ejecutar el traslado. |
| Origen ≠ Destino | La cuenta origen y la cuenta destino deben ser diferentes; lo mismo aplica para los terceros. |
| Cuenta destino activa | La cuenta que va a recibir los movimientos debe estar activa en el PUC del año actual. |
| No aplica en anulados | Los comprobantes en estado anulado quedan excluidos del proceso. |
| Periodo abierto | El periodo contable del comprobante debe estar abierto; los periodos cerrados no se pueden modificar. |
| Registro de auditoría | Cada traslado deja una entrada en Auditoría de Operación con el usuario, la fecha y el lote de cambio. |

**Efectos del traslado:**
- Recomputa los saldos contables de las cuentas involucradas.
- No es reversible de forma automática: se recomienda verificar el resultado en reportes de saldos.

---

### Auditoría de Operación

Historial completo y agrupado de los cambios realizados sobre comprobantes mediante las herramientas de Especiales.

**Información disponible por entrada de auditoría:**
- **Usuario**: quién ejecutó la operación.
- **Lote de modificación**: conjunto de comprobantes afectados en una misma ejecución.
- **Marca de tiempo**: fecha y hora exacta del cambio.
- **Detalle del cambio**: cuenta o tercero original vs. el nuevo valor aplicado.

**Uso habitual:** verificar el resultado de un traslado masivo reciente o rastrear quién modificó un comprobante específico.

**Distinta del Historial del panel Periodos:** Auditoría de Operación registra los cambios sobre comprobantes hechos con las herramientas de este panel (traslados, bloqueos, etc.); el **Historial** de `Especiales > Periodos` se limita a las aperturas y los cierres de periodos. Ver [Años fiscales y periodos contables](./anio-fiscal-periodos.md#historial-de-aperturas-y-cierres).

---

## Especiales › Terceros

La pestaña **Terceros** concentra las operaciones de corrección controlada sobre los datos de identificación de terceros registrados en la empresa.

### Actualización de Documento de Identificación

Permite corregir el **tipo o número de documento** (NIT, cédula u otro) de un tercero ya registrado. Existe como operación aislada del módulo estándar de edición de terceros para preservar la coherencia del historial contable: el campo de documento permanece bloqueado en la pantalla de edición normal de Terceros porque es la llave con la que se identifica al tercero en la empresa.

**Pasos:**
1. Ir a `Contabilidad > Configuración > Especiales`.
2. Ubicar el panel **Terceros**, que contiene una única opción.
3. Seleccionar **Actualizar documento**.
4. En el campo **Tercero**, buscar y seleccionar el tercero cuyo documento se va a modificar.
5. Ajustar **Tipo de identificación** y **NIT/Documento**.
6. Seleccionar **Guardar**.

**Campos de la ventana Actualizar documento de tercero** («Modifica el documento de identificación»):

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Tercero** | Buscador | Sí | Identifica al tercero que se va a modificar. Una vez seleccionado, muestra su nombre junto al documento actual. |
| **Tipo de identificación** | Lista desplegable | Sí | Permite cambiar también la clase de documento, no solo el número. |
| **NIT/Documento** | Texto | Sí | Número de documento nuevo. |
| **DV** | Texto | No | Dígito de verificación correspondiente al número nuevo. |
| **Cancelar** | Botón | — | Cierra la ventana sin guardar. |
| **Guardar** | Botón | — | Aplica el cambio de documento. |

Documentación completa, incluida la lógica de por qué el campo se bloquea en la edición estándar: [Terceros › Actualizar el documento o NIT de un tercero](./terceros.md#actualizar-el-documento-o-nit-de-un-tercero).

**Casos de uso:**
- El tercero fue creado con un NIT o cédula incorrectos y ya tiene comprobantes asociados.
- El tipo de documento está mal configurado (p. ej., cédula en vez de NIT).
- Notificación de DIAN o del contador indicando que el documento registrado no coincide con la base oficial.

**Validaciones previas:**
1. **Existencia del tercero**: el sistema verifica que el tercero con el documento actual exista en la empresa.
2. **Formato del nuevo documento**: valida que el número y tipo nuevo cumplan con el formato esperado.
3. **Sin duplicados**: verifica que no exista otro tercero con el nuevo documento dentro de la misma empresa.

**Efectos:**
- Actualiza el documento en **todos los comprobantes históricos** donde aparece ese tercero.
- Registra el evento en **Auditoría de Operación**.
- No es reversible de forma automática.

---

## Errores frecuentes

| Error | Causa | Solución |
|---|---|---|
| El CA no se genera | Diciembre o el año fiscal están cerrados. El CA es un comprobante con fecha del 31 de diciembre y necesita ese periodo abierto | Abrir diciembre en `Especiales > Periodos > Gestionar periodos contables`, registrar el cierre y volver a cerrar el periodo después |
| "El año destino ya tiene un SI" | Existía un comprobante SI previo en el año destino | Eliminar o limpiar el SI del año destino antes del traslado |
| "Cuenta destino inactiva" en traslado masivo | La cuenta seleccionada como destino está inactiva en el PUC | Reactivar la cuenta desde Configuración > PUC |
| Comprobante asíncrono días en "pendiente" | Cuenta inexistente en el PUC o tercero no registrado | Corregir en sistema de origen y reintentar el envío |
| "Ya existe" al actualizar documento de tercero | El nuevo NIT ya está en otro tercero de la misma empresa | Revisar duplicados y definir cuál tercero conserva el documento |
| Año origen no cumple condiciones para traslado | Falta el comprobante CA confirmado o periodos abiertos | Completar el Cierre Anual del año origen primero |

---

## Resumen de reglas de negocio

- El comprobante SI depende del año fiscal activo; no se hereda automáticamente entre años.
- El comprobante CA usa el tipo reservado `CA` con fecha fija (31 de diciembre); la cuenta de cierre es la `590505`.
- El Cierre Anual exige diciembre abierto: es un comprobante con fecha del 31 de diciembre, sujeto a las mismas validaciones de periodo que cualquier asiento. Debe registrarse **antes** de cerrar los periodos del año, no después.
- Mover Saldos Finales a Iniciales toma el año origen y el año destino de su propia ventana, con independencia del año fiscal activo.
- Bloquear la edición de un comprobante no es cerrar un periodo: son controles distintos y con alcances distintos.
- Los comprobantes de integración asíncrona tienen su propia bandeja de monitoreo; los síncronos van directo a la tabla principal.
- Los comprobantes de Optimun Escritorio llegan bloqueados por defecto; se desbloquean puntualmente desde Especiales.
- El traslado masivo de saldos entre cuentas excluye comprobantes anulados y periodos cerrados, y siempre genera registro en Auditoría.
- Auditoría de Operación registra los cambios hechos con las herramientas de Especiales; es distinta del Historial de aperturas y cierres del panel Periodos.
- La actualización de documento de un tercero aplica a todos sus comprobantes históricos y requiere que el nuevo documento no exista en otro tercero de la misma empresa.
