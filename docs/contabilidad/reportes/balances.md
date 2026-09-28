---
title: Reportes de Balances
description: Reportes del grupo Balances en Contabilidad > Reportes de Zoe Nube. Cubre los seis reportes (Balance de comprobación, Balance de comprobación Agrupado, Mayor y balance, Estado de Resultados, Caja Diario y Estado de Situación Financiera), sus ventanas de parámetros (año fiscal, tipo de balance mensual o rango de meses, rango de cuentas por clases o por cuentas puntuales para ver solo cuentas auxiliares, filtrado por tercero o centro de costo, agrupación, tipo de consulta acumulado o del mes, cuenta de utilidad del ejercicio), sus salidas en Excel y PDF, la estructura de columnas y totales de cada reporte, las validaciones de los formularios y los errores frecuentes.
module: contabilidad
category: reportes
slug: reportes-balances
order: 12
tags:
  - reportes
  - balances
  - reportes-financieros
  - balance-de-comprobacion
  - balance-de-comprobacion-agrupado
  - mayor-y-balance
  - estado-de-resultados
  - caja-diario
  - estado-de-situacion-financiera
  - balance-general
  - saldo-anterior
  - saldo-actual
  - debito
  - credito
  - naturaleza
  - rango-de-meses
  - rango-de-cuentas
  - cuentas-auxiliares
  - tercero
  - centro-de-costo
  - utilidad-del-ejercicio
  - utilidad-bruta
  - utilidad-operacional
  - activo
  - pasivo
  - patrimonio
  - excel
  - pdf
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-28
---

# Reportes de Balances

El grupo **Balances** de la pantalla **Reportes Financieros** (`Contabilidad > Reportes`) reúne los seis reportes de Zoe Nube para auditar saldos, movimientos y estados financieros de la empresa. Cada reporte se abre en una ventana de parámetros y se descarga en Excel, en PDF o en ambos. Este documento describe, para cada reporte, qué muestra, sus parámetros con sus reglas y validaciones, sus formatos de salida y la estructura del archivo generado.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Resumen de los seis reportes](#resumen-de-los-seis-reportes)
4. [Parámetros comunes](#parámetros-comunes)
5. [Balance de comprobación](#1-balance-de-comprobación)
6. [Balance de comprobación Agrupado](#2-balance-de-comprobación-agrupado)
7. [Mayor y balance](#3-mayor-y-balance)
8. [Estado de Resultados](#4-estado-de-resultados)
9. [Caja Diario](#5-caja-diario)
10. [Estado de Situación Financiera](#6-estado-de-situación-financiera)
11. [Errores frecuentes y mensajes de validación](#errores-frecuentes-y-mensajes-de-validación)
12. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
13. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Reportes`.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `PANEL / REPORTES`.
- **Título de la pantalla:** «Reportes Financieros», con el subtítulo «Genera reportes y conoce el estado de tu operación» y el aviso «Filtra, parametriza y genera tus reportes financieros en múltiples formatos.»
- **Grupo:** **BALANCES** (la pantalla también tiene los grupos Auxiliares, Anexos y Certificados). Cada tarjeta indica debajo del nombre los formatos disponibles.
- Al descargar, Zoe muestra el aviso **«Operación exitosa»** con un texto como «Reporte descargado correctamente» o «Estado de resultados descargado correctamente».

---

## Requisitos previos

1. Tener una empresa seleccionada en Zoe.
2. Tener comprobantes registrados en el año fiscal y período que se consultan.
3. Para filtrar o agrupar por tercero o centro de costo, que los movimientos tengan tercero o centro de costo asignado (ver `terceros.md` y `centros-costo.md`).

---

## Resumen de los seis reportes

| Reporte | Subtítulo de la ventana | Período | Nivel de cuentas | Filtros / opciones | Salidas (botones de la ventana) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Balance de comprobación** | «Verifica el equilibrio contable de tus cuentas» | Mensual o rango de meses | Todos los niveles, hasta auxiliares | Rango de cuentas; Filtrado por tercero o centro de costo | Excel y PDF |
| **Balance de comprobación Agrupado** | «Balance de comprobación con cuentas agrupadas» | Mensual (mes específico) o rango de meses | Todos los niveles, con desglose por agrupador | Agrupar por tercero o centro de costo (obligatorio); rango de cuentas | Excel y PDF |
| **Mayor y balance** | «Genera el reporte de mayor y balance de cuentas» | Mensual o rango de meses | Hasta cuentas de 4 dígitos | Rango de cuentas; Filtrado por tercero o centro de costo | Excel y PDF |
| **Estado de Resultados** | «Genera el estado de resultados financiero» | Un mes (con tipo de consulta) | Grupos del estado de resultados | Tipo de consulta: acumulado hasta la fecha o solo el mes | Solo PDF (la tarjeta dice «Excel y PDF», pero la ventana solo tiene el botón PDF) |
| **Caja Diario** | «Genera el reporte de caja diario» | Un mes | Cuentas de 4 dígitos con movimiento | — | Excel y PDF |
| **Estado de Situación Financiera** | «Genera el estado de situación financiera» | Corte a un mes | Cuentas principales y subcuentas de activo, pasivo y patrimonio | Cuenta de la utilidad del ejercicio | Solo PDF |

Ninguna de las ventanas tiene un botón para ver el reporte en pantalla: todas terminan en **Cancelar** y los botones de descarga (**Excel** verde, **PDF** rojo).

---

## Parámetros comunes

### Año fiscal
Campo obligatorio (**Año fiscal\***) en todas las ventanas. Lista desplegable con los años fiscales de la empresa (ej. 2026, 2023, 2022…).

### Tipo de Balance (Balance de comprobación, Agrupado y Mayor y balance)
Selector con dos opciones:
- **Mensual:** un solo mes. En el Agrupado el campo se llama **Mes específico**.
- **Rango de meses:** habilita **Mes de inicio\*** y **Mes de fin\*** (listas de Enero a Diciembre). Ejemplo: Enero a Octubre.

Si falta el mes, el formulario muestra: «Seleccione el mes o complete el rango de meses (inicio y fin)».

### Rango de cuentas (Cuenta inicial / Cuenta final)
Campos opcionales con buscador. Cada cuenta se muestra como `código - naturaleza - nombre` (ej. `1 - D - Activo`, `2 - C - Pasivo`, `7 - D - Costos de produccion o de operacion`, `7205 - D - Gastos de personal`). Se usan de dos formas:

1. **Por clases generales (nivel macro):** se eligen clases completas del PUC, desde `1 - D - Activo` hasta la última clase (`7 - D - Costos de produccion o de operacion`). Sirve para un balance completo con todos los movimientos de la empresa (activos, pasivos, patrimonio, ingresos, gastos y costos).
2. **Por cuentas puntuales (nivel específico):** se escribe en el buscador el código de una cuenta o subcuenta auxiliar (ej. `13551504`, o `7` para ver las cuentas que empiezan por 7). Sirve para analizar un grupo reducido de cuentas o una cuenta particular sin generar el reporte general.

### Ver solo cuentas auxiliares
Las ventanas no tienen una casilla «solo auxiliares»: la consulta de cuentas auxiliares se hace con el rango de cuentas. En **Cuenta inicial** y **Cuenta final** se busca por código la cuenta o subcuenta auxiliar que interesa (ej. `13551504`); para una sola auxiliar, se elige la misma en ambos campos, y para varias auxiliares consecutivas, la primera y la última del tramo. El reporte queda limitado a ese tramo del PUC en lugar de mostrar todas las cuentas. Aplica al Balance de comprobación, al Balance de comprobación Agrupado y a Mayor y balance (este último solo muestra cuentas de hasta 4 dígitos).

El rango elegido aparece en el bloque **PARAMETROS** del PDF (ej. «Rango de cuentas: 1 - 7») y, en el Excel de Mayor y balance, como «Rango de Códigos».

### Filtrado por (Balance de comprobación y Mayor y balance)
Bloque «Otros filtros» con la lista **Filtrado por**:
- **No aplica** (valor por defecto): todos los movimientos.
- **Tercero:** aparece el campo **Tercero\*** («Buscar por nombre o NIT»), con la lista de terceros como `nombre - NIT`. Si no se elige, el formulario muestra: «Seleccionó filtrar por tercero debe elegir un tercero».
- **Centro de costo:** aparece el campo **Centro de costo\***. Si no se elige, el formulario muestra: «Seleccionó filtrar por centro de costo debe elegir un centro de costo».

Cuando se usa el filtro, el bloque PARAMETROS del PDF lo muestra con la etiqueta «Agrupado por»: por ejemplo «Agrupado por: Tercero» y «Tercero: <nombre> - <NIT>» (Mayor y balance), o «Agrupado por: Centro de Costo» y «Centro de costo: Ventas» (Balance de comprobación).

### Encabezado de los PDF
Todos los PDF traen: nombre del reporte, razón social, tipo y número de identificación (ej. «NIT: 11111111»), el período («Desde 01/01/2026 hasta 31/10/2026») o la fecha de corte («A 31 de octubre de 2026»), «Valores en pesos colombianos (COP)», y la fecha, hora y zona horaria de impresión.

---

## 1. Balance de comprobación

Muestra, por cuenta contable, el saldo con que llegó al período, los débitos y créditos del período y el saldo final.

### Parámetros
| Campo | Obligatorio | Contenido |
| :--- | :--- | :--- |
| Año fiscal | Sí | Año a consultar. |
| Tipo de Balance | Sí | Mensual o Rango de meses (Mes de inicio y Mes de fin). |
| Cuenta inicial / Cuenta final | No | Rango de cuentas (por clases o por cuentas puntuales). |
| Filtrado por | No | No aplica, Tercero o Centro de costo. |

### Estructura del reporte (PDF)
- Bloque **PARAMETROS** con los filtros usados.
- Una fila por cuenta, en todos los niveles del PUC (clase, grupo, cuenta, subcuenta y auxiliar; ej. 1 ACTIVO, 11 DISPONIBLE, 1105 CAJA, 110505 caja general).
- Columnas: **Código**, **Nombre**, **Nat.** (D/C), **Saldo anterior**, **Débito**, **Crédito**, **Saldo actual**.
- Fila **TOTALES** con la suma de débitos y créditos.
- Bloque **TOTAL GENERAL**: Saldo débito anterior, Saldo crédito anterior, Saldo débito actual, Saldo crédito actual.

---

## 2. Balance de comprobación Agrupado

Misma información que el Balance de comprobación (saldo anterior, débitos, créditos y saldo actual por cuenta), separada por un agrupador:
- **Tercero:** saldos y movimientos por cliente, proveedor u otro tercero.
- **Centro de costo:** distribución de los movimientos por área, sede, proyecto o unidad interna.

### Parámetros
| Campo | Obligatorio | Contenido |
| :--- | :--- | :--- |
| Año fiscal | Sí | Año a consultar. |
| Agrupar por | Sí | Tercero o Centro de costo (bloque «Agrupación»; placeholder «Seleccione agrupación»). |
| Tipo de Balance Agrupado | Sí | Mensual (Mes específico) o Rango de meses (Mes de inicio y Mes de fin). |
| Cuenta inicial / Cuenta final | No | Rango de cuentas. |

No tiene el bloque «Filtrado por».

### Estructura del reporte (PDF, agrupado por tercero)
- Título «BALANCE DE COMPROBACIÓN AGRUPADO»; PARAMETROS con «Agrupado por: Tercero» y el rango de cuentas.
- Columnas: **Cuenta**, **Comp** (identificación del tercero), **Nombre Cuenta** (nombre de la cuenta o del tercero), **Nat.**, **Saldo anterior**, **Débito**, **Crédito**, **Saldo actual**.
- Debajo de cada cuenta auxiliar, una fila por tercero con su NIT y nombre. Los movimientos sin tercero aparecen como **[SIN TERCERO]**.
- Cierra con **TOTALES** y **TOTAL GENERAL**.
- Nombre del archivo observado: `balance-comprobacion-agrupado-terceros-<año>-<mes inicio>-<mes fin>.pdf`.

---

## 3. Mayor y balance

Resumen de saldos y movimientos por cuenta, limitado a las cuentas principales hasta **4 dígitos** (clase, grupo y cuenta; ej. 1, 11, 1105). Es una visión más resumida que el Balance de comprobación.

### Parámetros
Los mismos que el Balance de comprobación: Año fiscal, Tipo de Balance (Mensual / Rango de meses), Cuenta inicial / Cuenta final y Filtrado por (No aplica, Tercero, Centro de costo).

### Estructura del reporte
- **PDF** (título «MAYOR Y BALANCE»): columnas **Código**, **Nombre**, **Nat.**, **Saldo anterior**, **Débito**, **Crédito**, **Saldo actual**; fila **TOTALES** y bloque **TOTAL GENERAL** (saldo débito/crédito anterior y actual).
- **Excel**: encabezado con «Mayor y Balance», Empresa, NIT, Año Fiscal, Período (ej. «01/01/2026 - 30/09/2026»), Rango de Códigos y Fecha de Generación. Columnas **Código**, **Nombre de Cuenta**, **Saldo Anterior**, **Débito del Período**, **Crédito del Período**, **Saldo Actual** (sin columna de naturaleza). Fila final de totales: Saldo anterior, Total débito, Total crédito, Saldo actual.
- Nombre del archivo observado: `balance-de-mayor-<año>.pdf` / `.xlsx`.

---

## 4. Estado de Resultados

Resultado económico de la empresa a un mes del año: ingresos, costos, gastos y utilidad. Se genera para un mes puntual, no para un rango de meses.

### Parámetros
| Campo | Obligatorio | Contenido |
| :--- | :--- | :--- |
| Año fiscal | Sí | Año a consultar. |
| Mes | Sí | Mes de corte. |
| Tipo de consulta | Sí | «Acumulado hasta la fecha» (valor por defecto) o «Solo información del mes». |

Salida: solo **PDF**.

### Estructura del reporte (PDF)
Encabezado con la fecha de corte («A 31 de octubre de 2026»). Secciones, cada una con sus grupos de cuentas y valores:

| Línea | Contenido |
| :--- | :--- |
| 1. (+) INGRESOS OPERACIONALES | Ingresos operacionales (ej. comercio al por mayor y por menor). |
| 2. (-) COSTO DE VENTA | Costo de venta. |
| 1 - 2 = UTILIDAD BRUTA EN VENTAS | Ingresos operacionales menos costo de venta. |
| 3. (-) GASTOS GENERALES | Operacionales de administración (ej. gastos de personal, honorarios). |
| 1 - 2 - 3 = UTILIDAD OPERACIONAL | Utilidad bruta menos gastos generales. |
| 4. (+) INGRESOS NO OPERACIONALES | Ingresos no operacionales. |
| 5. (-) GASTOS NO OPERACIONALES | No operacionales (ej. financieros, gastos diversos). |
| 1 - 2 - 3 + 4 - 5 = RESULTADO EJERCICIO | Utilidad o pérdida del ejercicio. |

Nombre del archivo observado: `Estado-de-Resultados-<Mes>-<año>.pdf`.

---

## 5. Caja Diario

Para un mes específico, las cuentas contables de **4 dígitos** que tuvieron movimiento en ese período, con su débito y su crédito del mes. **No** muestra saldo anterior ni saldo final.

### Parámetros
| Campo | Obligatorio | Contenido |
| :--- | :--- | :--- |
| Año fiscal | Sí | Año a consultar. |
| Mes | Sí | Mes a consultar. |

Salidas: **Excel** y **PDF**.

### Estructura del reporte (Excel)
- Encabezado: «Caja Diario», Empresa, NIT, Año Fiscal, Mes (número), Período (ej. «01/10/2026 - 31/10/2026») y Fecha de Generación.
- Columnas: **Código**, **Nombre**, **Débito**, **Crédito** (ej. 1105 Caja, 1110 BANCOS, 3105 Capital suscrito y pagado).
- Fila **TOTALES** con la suma de débitos y de créditos del mes.
- Nombre del archivo observado: `Reporte-Caja-diario-Mes-<Mes>-<año>.xlsx`.

### Estructura del reporte (PDF)
- Título «CAJA DIARIO», razón social, NIT, período («Desde 01/05/2026 hasta 31/05/2026») y moneda.
- Bloque **PARAMETROS** con Año Fiscal y Mes (ej. «Mes: Mayo»).
- Columnas **Código**, **Nombre**, **Débito**, **Crédito**, y fila **TOTALES**.
- Nombre del archivo observado: `Reporte-Caja-diario-Mes-<Mes>-<año>.pdf`.

---

## 6. Estado de Situación Financiera

Situación financiera de la empresa a la fecha de corte del mes seleccionado (último día del mes).

### Parámetros
| Campo | Obligatorio | Contenido |
| :--- | :--- | :--- |
| Año fiscal | Sí | Año a consultar. |
| Mes | Sí | Mes de corte. |
| Cuenta | No (trae valor por defecto) | Cuenta del patrimonio donde se incluye la utilidad del ejercicio. Por defecto `360505 - C - Utilidad del ejercicio`; tiene buscador. |

El título de la ventana tiene un ícono de información (ⓘ). Salida: solo **PDF**.

### Estructura del reporte (PDF)
- Encabezado con la fecha de corte («A 31 de julio de 2026»).
- Tres bloques: **ACTIVO**, **PASIVO** y **PATRIMONIO**. En cada uno, las cuentas principales en negrita con su total (ej. DISPONIBLE, DEUDORES, INVENTARIOS; OBLIGACIONES FINANCIERAS, PROVEEDORES, CUENTAS POR PAGAR, IMPUESTOS GRAVAMENES Y TASAS) y debajo sus subcuentas con su valor.
- Totales: **TOTAL ACTIVO**, **TOTAL PASIVO**, **TOTAL PATRIMONIO**.
- La utilidad del ejercicio aparece en el patrimonio como **RESULTADOS DEL EJERCICIO > UTILIDAD DEL EJERCICIO**, en la cuenta indicada en el parámetro Cuenta.
- Línea final **PASIVO + PATRIMONIO = ACTIVO** con un valor.

> [!NOTE]
> En los tres PDF de prueba generados en septiembre de 2026 (cortes a abril, mayo y julio), la línea «PASIVO + PATRIMONIO = ACTIVO» mostraba el valor del Total Activo, y el reporte no presentaba ningún aviso aunque Total Pasivo + Total Patrimonio fuera distinto del Total Activo. Para verificar la ecuación contable hay que sumar los dos totales y compararlos con el Total Activo.

---

## Errores frecuentes y mensajes de validación

| Situación | Mensaje o síntoma | Solución |
| :--- | :--- | :--- |
| Falta el mes o el rango de meses | «Seleccione el mes o complete el rango de meses (inicio y fin)» | Elegir el mes (Mensual) o el Mes de inicio y el Mes de fin (Rango de meses). |
| Filtrado por Tercero sin tercero | «Seleccionó filtrar por tercero debe elegir un tercero» | Buscar y elegir el tercero, o volver a «No aplica». |
| Filtrado por Centro de costo sin centro | «Seleccionó filtrar por centro de costo debe elegir un centro de costo» | Elegir el centro de costo, o volver a «No aplica». |
| No aparece una cuenta esperada | La cuenta no sale en el reporte | Verificar que esté dentro del rango de cuentas; en Mayor y balance y Caja Diario solo salen cuentas de hasta 4 dígitos. |
| Se busca exportar Estado de Resultados a Excel | La ventana solo tiene el botón PDF | El reporte se descarga solo en PDF. |
| Total Pasivo + Total Patrimonio distinto del Total Activo | El Estado de Situación Financiera no cuadra | Revisar el Balance de comprobación del mismo período y la cuenta de utilidad elegida. |

---

## Resumen de reglas de negocio

| # | Regla de negocio |
| :--- | :--- |
| 1 | Los seis reportes se generan desde `Contabilidad > Reportes`, grupo Balances, y todos exigen **Año fiscal**. |
| 2 | Balance de comprobación, Agrupado y Mayor y balance se consultan por un mes o por un rango de meses. |
| 3 | Estado de Resultados, Caja Diario y Estado de Situación Financiera se consultan por un solo mes. |
| 4 | El rango de cuentas es opcional y admite clases completas o cuentas/auxiliares puntuales; así se consultan solo las cuentas auxiliares que interesan. |
| 5 | Balance de comprobación y Mayor y balance permiten filtrar por un tercero o por un centro de costo; si se elige el filtro, el tercero o centro de costo es obligatorio. |
| 6 | El Balance de comprobación Agrupado exige elegir el agrupador: Tercero o Centro de costo. |
| 7 | Mayor y balance y Caja Diario muestran solo cuentas de hasta 4 dígitos; el Balance de comprobación muestra todos los niveles. |
| 8 | Caja Diario muestra solo débitos y créditos del mes, sin saldo anterior ni saldo final. |
| 9 | Estado de Resultados permite ver el acumulado hasta la fecha o solo la información del mes. |
| 10 | Estado de Situación Financiera incluye la utilidad del ejercicio en la cuenta indicada (por defecto 360505). |
| 11 | Estado de Resultados y Estado de Situación Financiera solo se descargan en PDF; los demás, en Excel y PDF. |
| 12 | No hay vista en pantalla: los reportes se obtienen como archivo descargado. |

---

## Preguntas frecuentes

**¿Qué diferencia hay entre el Balance de comprobación y Mayor y balance?**
Tienen las mismas columnas y parámetros, pero el Balance de comprobación llega hasta las cuentas auxiliares y Mayor y balance se queda en las cuentas de hasta 4 dígitos, con una visión más resumida.

**¿Cómo veo los saldos de un solo cliente o proveedor?**
En el Balance de comprobación o en Mayor y balance, elegir **Filtrado por: Tercero** y seleccionar el tercero. Para ver todos los terceros separados en un mismo reporte, usar el **Balance de comprobación Agrupado** con **Agrupar por: Tercero**.

**¿Cómo saco un balance completo de todas las cuentas?**
En Cuenta inicial elegir `1 - D - Activo` y en Cuenta final la última clase (`7 - D - Costos de produccion o de operacion`).

**¿Cómo veo solo una cuenta auxiliar en el Balance de comprobación?**
En **Cuenta inicial** y **Cuenta final**, buscar por código la cuenta auxiliar (ej. `13551504`) y elegirla en los dos campos. El reporte muestra solo ese tramo del PUC.

**¿El Estado de Resultados se puede sacar por varios meses?**
No como rango: se elige un mes y, con «Acumulado hasta la fecha», se obtiene el resultado del año hasta ese mes.

**¿Puedo ver los reportes en pantalla sin descargarlos?**
No. Las ventanas solo tienen los botones de descarga (Excel y/o PDF) y Cancelar.

**¿Dónde veo el detalle de los movimientos de una cuenta?**
En el Libro Auxiliar (grupo Auxiliares), documentado en `reportes-basicos.md`.
