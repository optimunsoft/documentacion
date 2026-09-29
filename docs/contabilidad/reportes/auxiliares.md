---
title: Reportes Auxiliares
description: Reportes del grupo Auxiliares en Contabilidad > Reportes de Zoe Nube. Cubre el Libro auxiliar (movimientos por cuenta con saldo anterior, comprobante, concepto, tercero, factura, débito, crédito y saldo final) y la Relación de Documentos (comprobantes consolidados de un período), con sus parámetros (año fiscal, tipo de período mensual, rango de meses o rango de fechas, rango de cuentas, filtrado por tercero o centro de costo, ocultar columna de concepto, estado del comprobante), sus salidas en Excel y PDF, la estructura del PDF y del Excel generados y los errores frecuentes.
module: contabilidad
category: reportes
slug: reportes-auxiliares
order: 13
tags:
  - reportes
  - auxiliares
  - libro-auxiliar
  - relacion-de-documentos
  - comprobantes-consolidados
  - movimientos-por-cuenta
  - saldo-anterior
  - saldo-final
  - debito
  - credito
  - naturaleza
  - tercero
  - centro-de-costo
  - factura
  - rango-de-meses
  - rango-de-fechas
  - rango-de-cuentas
  - ocultar-columna-de-concepto
  - conciliacion-bancaria
  - estado-del-comprobante
  - comprobante-anulado
  - excel
  - pdf
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-29
---

# Reportes Auxiliares

El grupo **Auxiliares** de la pantalla **Reportes Financieros** (`Contabilidad > Reportes`) tiene dos reportes de Zoe Nube para auditar al detalle los movimientos contables: el **Libro auxiliar**, que muestra los movimientos de cada cuenta, y la **Relación de Documentos**, que muestra los comprobantes contables consolidados de un período. Cada reporte se abre en una ventana de parámetros y se descarga en Excel o en PDF.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Resumen de los dos reportes](#resumen-de-los-dos-reportes)
4. [Libro auxiliar](#1-libro-auxiliar)
5. [Relación de Documentos](#2-relación-de-documentos)
6. [Errores frecuentes](#errores-frecuentes)
7. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Reportes`.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `PANEL / REPORTES`.
- **Título de la pantalla:** «Reportes Financieros», con el subtítulo «Genera reportes y conoce el estado de tu operación» y el aviso «Filtra, parametriza y genera tus reportes financieros en múltiples formatos.»
- **Grupo:** **AUXILIARES** (la pantalla también tiene los grupos Balances, Anexos y Certificados). Cada tarjeta indica debajo del nombre los formatos disponibles: «Excel y PDF».
- Al descargar, Zoe muestra el aviso **«Operación exitosa»** con el texto «Reporte descargado correctamente».

---

## Requisitos previos

1. Tener una empresa seleccionada en Zoe.
2. Tener comprobantes registrados en el año fiscal y período que se consultan.
3. Para filtrar por tercero o centro de costo, que los movimientos tengan tercero o centro de costo asignado (ver `terceros.md` y `centros-costo.md`).

---

## Resumen de los dos reportes

| Reporte | Subtítulo de la ventana | Período | Filtros / opciones | Salidas (botones de la ventana) |
| :--- | :--- | :--- | :--- | :--- |
| **Libro auxiliar** | «Genera el libro auxiliar de cuentas contables» | Mensual, rango de meses o rango de fechas | Rango de cuentas; Filtrado por tercero o centro de costo; Ocultar columna de concepto | Excel y PDF |
| **Relación de Documentos** | «Genera la relación consolidada de comprobantes contables» | Mensual, rango de meses o rango de fechas | Estado del comprobante | Excel y PDF |

---

## 1. Libro auxiliar

Muestra, cuenta por cuenta, los movimientos de un período: el saldo con el que la cuenta llegó al período, cada comprobante que la afectó con su tercero y su factura, y el saldo final.

### Parámetros de la ventana

| Parámetro | Obligatorio | Descripción |
| :--- | :---: | :--- |
| **Año fiscal** | Sí | Año fiscal a consultar (por ejemplo 2026). |
| **Tipo de Auxiliar** | Sí | Define el período: **Mensual** (un solo mes), **Rango de meses** (con **Mes de inicio** y **Mes de fin**) o **Rango de fechas**. |
| **Fecha inicial** y **Fecha final** | Sí | Fechas exactas del período. Con **Rango de meses**, Zoe las completa a partir de los meses elegidos (por ejemplo, de enero a octubre de 2026 queda 01/Ene/2026 a 31/Oct/2026). |
| **Cuenta inicial** y **Cuenta final** (Rango de cuentas) | No | Limitan el reporte a un rango de cuentas. Las listas tienen buscador por código y muestran las clases del PUC, por ejemplo `1 - D - Activo`, `2 - C - Pasivo`, `3 - C - Patrimonio`, `4 - C - Ingresos`, `5 - D - Gastos`. |
| **Filtrado por** | No | **No aplica** (todos los movimientos), **Tercero** (aparece el campo Tercero) o **Centro de costo** (aparece el campo Centro de costo). |
| **Ocultar columna de concepto** | No | Casilla. El ícono de información indica: «Oculta la columna 'Concepto' del reporte PDF para comprimir el número de páginas generadas. Útil para conciliación bancaria manual.» |

Botones de la ventana: **Cancelar**, **Excel** (verde) y **PDF** (rojo).

### Cómo generarlo

1. En el grupo **Auxiliares**, elegir **Libro auxiliar**.
2. Elegir el **Año fiscal**.
3. En **Tipo de Auxiliar**, elegir el período (Mensual, Rango de meses o Rango de fechas) y completar sus campos.
4. Opcionalmente, elegir la **Cuenta inicial** y la **Cuenta final**.
5. En **Filtrado por**, elegir **No aplica**, **Tercero** o **Centro de costo** y, si aplica, seleccionar el tercero o el centro de costo.
6. Opcionalmente, marcar **Ocultar columna de concepto**.
7. Hacer clic en **Excel** o en **PDF**.

### Estructura del PDF

- **Encabezado:** título «LIBRO AUXILIAR», nombre de la empresa, NIT, período (`Desde dd/mm/aaaa hasta dd/mm/aaaa`), «Valores en pesos colombianos (COP)» y fecha de impresión con zona horaria.
- **PARAMETROS:** rango de cuentas usado (por ejemplo `Rango de cuentas: 1 - 3`).
- **Un bloque por cuenta:** título con `código - naturaleza - nombre` (por ejemplo `110505 - D - CAJA GENERAL`) y, a la derecha, **Saldo Anterior**.

| Columna | Contenido |
| :--- | :--- |
| **CTE** | Código del comprobante que originó el movimiento (por ejemplo `IFC-2`, `NC-8`, `CE-AB-3`). |
| **F/CTE** | Fecha del comprobante (formato aaaa-mm-dd). |
| **CONCP.** | Concepto del movimiento. No aparece si se marcó Ocultar columna de concepto. |
| **DÉBITO** | Valor débito. |
| **CRÉDITO** | Valor crédito. |
| **Tercero** | Tercero relacionado con el movimiento. |
| **Nro. Factura** | Número de factura asociada; `N/A` si no tiene. |

- **Cierre de cada cuenta:** fila **TOTALES** con la suma de débitos y créditos, y **Saldo final** de la cuenta.
- **Pie de página:** fecha de impresión, «Zoe Contabilidad» y número de página.

### Estructura del Excel

El Excel es más completo que el PDF: incluye base, porcentaje, saldo después de cada movimiento y NIT del tercero.

- **Encabezado (filas 1 a 7):** `Libro Auxiliar`, `Empresa`, `NIT`, `Año Fiscal`, `Período` (`dd/mm/aaaa - dd/mm/aaaa`), `Rango de Códigos` (por ejemplo `1 - 3`) y `Fecha de Generación`.
- **Un bloque por cuenta:** fila **Saldo Anterior** con el código, el nombre con su naturaleza (por ejemplo `Caja general - DÉBITO`) y el valor; fila de encabezados; movimientos; fila **Totales** con la suma de débitos y créditos; y fila **Saldo Final** con el código, el nombre y el saldo.

| Columna | Contenido |
| :--- | :--- |
| **# Comprobante** | Código del comprobante que originó el movimiento (por ejemplo `CE-FB-1`). |
| **Código** | Código de la cuenta. |
| **Cuenta** | Nombre de la cuenta. |
| **Naturaleza** | `DÉBITO` o `CRÉDITO`. |
| **Base** | Base del cálculo, cuando corresponde (por ejemplo `5000000` en una cuenta de retención); vacía en los demás movimientos. |
| **Porcentaje** | Porcentaje aplicado, cuando corresponde (por ejemplo `10`); vacío en los demás movimientos. |
| **Débito** | Valor débito. |
| **Crédito** | Valor crédito. |
| **Saldo Actual** | Saldo de la cuenta después del movimiento. |
| **Fecha** | Fecha del comprobante (aaaa-mm-dd). |
| **Concepto** | Concepto del movimiento. |
| **# Factura** | Número de factura asociada; `N/A` si no tiene. |
| **Tercero** | Nombre del tercero. |
| **NIT** | Identificación del tercero. |

---

## 2. Relación de Documentos

Muestra los comprobantes contables consolidados de un período, cada uno con sus movimientos.

### Parámetros de la ventana

| Parámetro | Obligatorio | Descripción |
| :--- | :---: | :--- |
| **Año fiscal** | Sí | Año fiscal a consultar. |
| **Tipo de período** | Sí | **Mensual**, **Rango de meses** (con **Mes de inicio** y **Mes de fin**, ambos obligatorios) o **Rango de fechas**. |
| **Fecha inicial** y **Fecha final** | Sí | Fechas del período; con Rango de meses se completan a partir de los meses elegidos (por ejemplo, enero a julio queda 01/Ene/2026 a 31/Jul/2026). |
| **Estado del comprobante** | No | **Todos los estados** (valor inicial), **Activo** o **Anulado**. |

Botones de la ventana: **Cancelar**, **Excel** y **PDF**.

### Cómo generarlo

1. En el grupo **Auxiliares**, elegir **Relación de Documentos**.
2. Elegir el **Año fiscal**.
3. En **Tipo de período**, elegir el período y completar sus campos.
4. En **Estado del comprobante**, elegir **Todos los estados**, **Activo** o **Anulado**.
5. Hacer clic en **Excel** o en **PDF**.

### Estructura del PDF

- **Encabezado:** título «COMPROBANTES CONSOLIDADOS», nombre de la empresa, identificación (por ejemplo `CÉDULA DE CIUDADANÍA: 11111111`), período, «Valores en pesos colombianos (COP)» y fecha de impresión.
- **Resumen:** **Total de comprobantes**, **Estado** filtrado (por ejemplo `ACTIVO`), **Anulados**, suma de **Débito** y suma de **Crédito**.
- **Presentación:** los comprobantes están ordenados por fecha ascendente y, dentro de una misma fecha, por número de comprobante ascendente.
- **Un bloque por comprobante:** encabezado con código, **Fecha**, **Tipo** de documento y **Concepto**, y una tabla con estas columnas:

| Columna | Contenido |
| :--- | :--- |
| **Cuenta** | Código y nombre de la cuenta afectada. |
| **Concepto** | Descripción del movimiento. |
| **NIT** | Identificación del tercero. |
| **Tercero** | Nombre del tercero. |
| **Factura** | Número de factura asociada. |
| **C.C.** | Centro de costo. |
| **Débito** / **Crédito** | Valores del movimiento. |

- **Cierre de cada comprobante:** fila **Total comprobante** con la suma de débitos y créditos, que deben ser iguales.

---

## Errores frecuentes

| Situación | Causa y solución |
| :--- | :--- |
| No aparece una cuenta en el Libro auxiliar | La cuenta está fuera del rango de cuentas elegido, no tiene movimientos en el período, o el filtro por tercero o centro de costo la excluye. |
| El PDF del Libro auxiliar tiene demasiadas páginas | Marcar **Ocultar columna de concepto** o reducir el rango de cuentas o de fechas. |
| La Relación de Documentos no muestra comprobantes anulados | El **Estado del comprobante** está en **Activo**. Elegir **Todos los estados** o **Anulado**. |
| No se encuentra el archivo descargado | Revisar la carpeta de descargas del navegador y que no bloquee las descargas del sitio. |

---

## Preguntas frecuentes

**¿Qué diferencia hay entre el Libro auxiliar y la Relación de Documentos?**
El Libro auxiliar se organiza por cuenta contable: muestra los movimientos de cada cuenta con su saldo anterior y su saldo final. La Relación de Documentos se organiza por comprobante: muestra cada comprobante con todas las cuentas que afectó.

**¿Dónde veo la base, el porcentaje, el NIT del tercero o el saldo después de cada movimiento?**
En el Excel del Libro auxiliar. El PDF muestra una versión reducida, sin esas columnas.

**¿Para qué sirve Ocultar columna de concepto?**
Oculta la columna Concepto del PDF del Libro auxiliar para que el reporte ocupe menos páginas. Zoe la indica como útil para la conciliación bancaria manual.

**¿Puedo ver solo los comprobantes anulados?**
Sí. En la Relación de Documentos, elegir **Anulado** en **Estado del comprobante**.

**¿Puedo consultar un solo tercero o un solo centro de costo en el Libro auxiliar?**
Sí. En **Filtrado por**, elegir **Tercero** o **Centro de costo** y seleccionar el que se necesita.

**¿En qué formatos se descargan?**
Ambos reportes se descargan en Excel y en PDF, con los botones **Excel** y **PDF** de la ventana de parámetros.
