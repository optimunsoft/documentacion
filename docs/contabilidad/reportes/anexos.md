---
title: Reportes de Anexos
description: Reportes del grupo Anexos en Contabilidad > Reportes de Zoe Nube. Cubre el Reporte de Anexos (movimientos de las cuentas de un anexo en formato Agrupado o Detallado, con NIT, nombre del tercero, porcentaje, base, débito y crédito) y la Configuración de Anexos (cuentas de cada anexo con naturaleza y porcentaje en un año fiscal), con sus parámetros (año fiscal, anexo, formato, rango de fechas, rango de cuentas configuradas en el anexo, filtrado por tercero), sus salidas en Excel y PDF, la estructura del PDF generado y los errores frecuentes.
module: contabilidad
category: reportes
slug: reportes-anexos
order: 14
tags:
  - reportes
  - anexos
  - reporte-de-anexos
  - configuracion-de-anexos
  - anexo-agrupado
  - anexo-detallado
  - formato-agrupado
  - formato-detallado
  - base
  - porcentaje
  - naturaleza
  - debito
  - credito
  - tercero
  - nit
  - rango-de-fechas
  - rango-de-cuentas
  - cuentas-del-anexo
  - año-fiscal
  - excel
  - pdf
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-29
---

# Reportes de Anexos

El grupo **Anexos** de la pantalla **Reportes Financieros** (`Contabilidad > Reportes`) tiene dos reportes de Zoe Nube: el **Reporte de Anexos**, que consulta los movimientos de las cuentas asociadas a un anexo, y la **Configuración de Anexos**, que muestra cómo están configurados los anexos de la empresa en un año fiscal. Cada reporte se abre en una ventana de parámetros y se descarga en Excel o en PDF.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Resumen de los dos reportes](#resumen-de-los-dos-reportes)
4. [Reporte de Anexos](#1-reporte-de-anexos)
5. [Configuración de Anexos](#2-configuración-de-anexos)
6. [Errores frecuentes](#errores-frecuentes)
7. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Reportes`.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `PANEL / REPORTES`.
- **Título de la pantalla:** «Reportes Financieros».
- **Grupo:** **ANEXOS**, con las tarjetas «Reporte de Anexos» y «Configuracion de Anexos», ambas con «Excel y PDF».
- Al descargar, Zoe muestra el aviso **«Operación exitosa»** con el texto «Reporte descargado correctamente».

---

## Requisitos previos

1. Tener una empresa seleccionada en Zoe.
2. Tener anexos creados, con sus cuentas, en el año fiscal que se consulta (ver `Contabilidad > Configuración > Anexos`).
3. Para el Reporte de Anexos, que las cuentas del anexo tengan movimientos en el período.

---

## Resumen de los dos reportes

| Reporte | Título de la ventana | Subtítulo | Qué muestra | Salidas |
| :--- | :--- | :--- | :--- | :--- |
| **Reporte de Anexos** | «Generar reporte de Anexos» | «Configura y genera reportes de anexos contables» | Movimientos de las cuentas de un anexo, Agrupado o Detallado | Excel y PDF |
| **Configuración de Anexos** | «Configuración de Anexos» | «Administra la configuración de anexos contables» | Cuentas de cada anexo con naturaleza y porcentaje | Excel y PDF |

---

## 1. Reporte de Anexos

Consulta los movimientos de las cuentas asociadas a un anexo durante el período seleccionado. El parámetro **Formato** determina cómo se presenta la información.

### Parámetros de la ventana

| Parámetro | Obligatorio | Descripción |
| :--- | :---: | :--- |
| **Año fiscal** | Sí | Año fiscal a consultar. La lista muestra los años fiscales de la empresa (por ejemplo 2026, 2023, 2022). |
| **Anexo** | Sí | Lista con buscador. Muestra código y nombre, por ejemplo `009 - Informacion Alistada`, `123 - Anticipos Y Avances`, `212 - Arqueo De Caja General`. Al elegirlo, Zoe muestra su **Código** y su **Nombre**. |
| **Formato** | Sí | **Agrupado** (valor inicial) o **Detallado**. |
| **Desde** y **Hasta** (Rango de fechas) | Sí | Por defecto, todo el año fiscal (01/Ene/2026 a 31/Dic/2026). Se pueden cambiar para consultar un período específico. |
| **Cuenta inicial** y **Cuenta final** (Rango de cuentas) | No | Limitan el reporte a un rango de cuentas. Zoe muestra el aviso «A TENER EN CUENTA: Sólo se listan las cuentas que fueron configuradas en el anexo seleccionado.» |
| **Filtrado por** | No | **No aplica** (valor inicial) o **Tercero**; con Tercero aparece el campo **Tercero** con el buscador «Buscar tercero...». |

Botones de la ventana: **Cancelar**, **Excel** y **PDF**.

### Formatos

| Formato | Cómo presenta la información | Cuándo usarlo |
| :--- | :--- | :--- |
| **Agrupado** | Un renglón por tercero y porcentaje aplicado, con los valores acumulados. | Resumen general. |
| **Detallado** | Un renglón por cada movimiento, con el código del comprobante que lo originó. | Revisar el origen de cada valor. |

### Cómo generarlo

1. En el grupo **Anexos**, elegir **Reporte de Anexos**.
2. Elegir el **Año fiscal**.
3. En **Anexo**, buscar y seleccionar el anexo.
4. En **Formato**, elegir **Agrupado** o **Detallado**.
5. Dejar el **Rango de fechas** del año completo o cambiar **Desde** y **Hasta**.
6. Opcionalmente, elegir la **Cuenta inicial** y la **Cuenta final**.
7. En **Filtrado por**, dejar **No aplica** o elegir **Tercero** y seleccionar el tercero.
8. Hacer clic en **Excel** o en **PDF**.

### Estructura del PDF

- **Encabezado:** título «REPORTE ANEXO AGRUPADO» o «REPORTE ANEXO DETALLADO», nombre de la empresa, NIT, «Valores en pesos colombianos (COP)» y fecha de impresión con zona horaria.
- **PARAMETROS:** **Anexo** (por ejemplo `123 - Anticipos y Avances`), **Año fiscal**, **Rango de fechas** (`Desde 2026-01-01 hasta 2026-12-31`) y **Rango de cuentas** (por ejemplo `110510 - 13301009`).
- **Un bloque por cuenta del anexo:** título `CUENTA código - nombre` (por ejemplo `CUENTA 110510 - Cajas menor`) y una tabla.

| Columna | Agrupado | Detallado | Contenido |
| :--- | :---: | :---: | :--- |
| **Comprobante** | — | Sí | Código del comprobante del movimiento (por ejemplo `IPC-2`, `NC-8`). Es la primera columna. |
| **NIT** | Sí | Sí | Identificación del tercero. |
| **Nombre** | Sí | Sí | Nombre del tercero. |
| **%** | Sí | Sí | Porcentaje aplicado. |
| **Base** | Sí | Sí | Base sobre la que se calculó el porcentaje. |
| **Débito** | Sí | Sí | Valor débito (acumulado en Agrupado; del movimiento en Detallado). |
| **Crédito** | Sí | Sí | Valor crédito (acumulado en Agrupado; del movimiento en Detallado). |

- **Cierre de cada cuenta:** fila **TOTALES** con la suma de débitos y créditos.

---

## 2. Configuración de Anexos

Muestra cómo están configurados los anexos contables de la empresa en el año fiscal seleccionado.

### Parámetros de la ventana

| Parámetro | Obligatorio | Descripción |
| :--- | :---: | :--- |
| **Año fiscal** | Sí | Año fiscal cuya configuración de anexos se quiere revisar. |

Botones de la ventana: **Cancelar**, **Excel** y **PDF**.

### Cómo generarlo

1. En el grupo **Anexos**, elegir **Configuración de Anexos**.
2. Elegir el **Año fiscal**.
3. Hacer clic en **Excel** o en **PDF**.

### Estructura del PDF

- **Encabezado:** título «CONFIGURACIÓN DE ANEXOS», nombre de la empresa, NIT, «Valores en pesos colombianos (COP)» y fecha de impresión.
- **PARAMETROS:** **Año fiscal**.
- **Un bloque por anexo:** título `Anexo: código - nombre` (por ejemplo `Anexo: 009 - INFORMACION ALISTADA`, `Anexo: 123 - Anticipos y Avances`, `Anexo: 212 - Arqueo de Caja General`) y una tabla con las cuentas del anexo:

| Columna | Contenido |
| :--- | :--- |
| **Código** | Código de la cuenta contable (por ejemplo `110510`, `13301002`). |
| **Nombre de Cuenta** | Nombre de la cuenta. |
| **Naturaleza** | `D` (débito) o `C` (crédito). |
| **Porcentaje** | Porcentaje configurado para la cuenta en el anexo (por ejemplo `11,25%`, `12,00%`). |

Este reporte permite verificar qué cuentas forman parte de cada anexo y bajo qué condiciones están configuradas.

---

## Errores frecuentes

| Situación | Causa y solución |
| :--- | :--- |
| No aparece el anexo en la lista | El anexo no existe en el año fiscal elegido. Cada año fiscal tiene su configuración de anexos. |
| No aparece una cuenta en el rango de cuentas | Solo se listan las cuentas configuradas en el anexo seleccionado. Revisar el reporte Configuración de Anexos y, si falta, agregarla en `Contabilidad > Configuración > Anexos`. |
| El reporte sale sin movimientos | El rango de fechas no incluye comprobantes que afecten las cuentas del anexo, o el tercero filtrado no tiene movimientos en ellas. |
| No se encuentra el archivo descargado | Revisar la carpeta de descargas del navegador y que no bloquee las descargas del sitio. |

---

## Preguntas frecuentes

**¿Cuál es la diferencia entre Agrupado y Detallado?**
Agrupado presenta un renglón por tercero y porcentaje con los valores acumulados, para un resumen general. Detallado presenta un renglón por movimiento e incluye el código del comprobante, para revisar el origen de cada valor.

**¿Puedo consultar solo una parte del año?**
Sí. El rango de fechas viene con el año fiscal completo; se cambian **Desde** y **Hasta** para un período específico.

**¿Por qué solo veo algunas cuentas en el rango de cuentas?**
Zoe solo lista las cuentas que fueron configuradas en el anexo seleccionado.

**¿Cómo veo qué cuentas tiene un anexo?**
Con el reporte **Configuración de Anexos**, que las agrupa por anexo con su naturaleza y porcentaje.

**¿En qué formatos se descargan?**
Ambos reportes se descargan en Excel y en PDF, con los botones **Excel** y **PDF** de la ventana de parámetros.
