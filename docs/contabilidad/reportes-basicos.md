---
title: Cómo generar reportes básicos para validar tu información
description: Genera el Libro Auxiliar y el Balance de Comprobación para revisar que los movimientos registrados sean correctos.
module: contabilidad
category: primeros-pasos
slug: reportes-basicos
order: 5
tags:
  - reportes
  - libro-auxiliar
  - balance-de-comprobacion
  - validacion
  - excel
  - pdf
  - primeros-pasos
draft: false
rag_exclude: false
last_updated: 2026-08-19
---

# Cómo generar reportes básicos para validar tu información

Después de registrar tus primeros comprobantes, utiliza estos dos reportes para comprobar que la información quedó bien ingresada.

## Tabla de contenido

1. [Cuál reporte usar](#cuál-reporte-usar)
2. [Requisitos previos](#requisitos-previos)
3. [Los parámetros son los mismos para los dos reportes](#los-parámetros-son-los-mismos-para-los-dos-reportes)
4. [Genera el Libro Auxiliar](#1-genera-el-libro-auxiliar)
5. [Lee el Libro Auxiliar](#2-lee-el-libro-auxiliar)
6. [Genera el Balance de Comprobación](#3-genera-el-balance-de-comprobación)
7. [Lee el Balance de Comprobación](#4-lee-el-balance-de-comprobación)
8. [Errores frecuentes](#errores-frecuentes)

## Cuál reporte usar

Ambos reportes se generan desde **Contabilidad > Reportes**, en la pantalla **Reportes Financieros**, y responden preguntas distintas:

- **Balance de Comprobación:** muestra una fila por cuenta con sus totales. Úsalo para comprobar de un vistazo que la contabilidad esté cuadrada. Está en el grupo **Balances**.
- **Libro Auxiliar:** muestra cada movimiento individual de cada cuenta. Úsalo para revisar en detalle qué movimientos componen el saldo de una cuenta. Está en el grupo **Auxiliares**.

Lo habitual es revisar primero el Balance de Comprobación y, si alguna cuenta no cuadra, consultar su detalle en el Libro Auxiliar.

## Requisitos previos

- Tener una empresa seleccionada y su año fiscal disponible.
- Tener comprobantes registrados en el período que vas a consultar.

## Los parámetros son los mismos para los dos reportes

Al elegir cualquiera de los dos reportes, Zoe abre una ventana de parámetros. **Los campos son prácticamente los mismos**, así que basta con aprenderlos una vez.

### Campos obligatorios

- **Año fiscal:** año contable que vas a consultar.
- **Período:** define el tramo de tiempo del reporte. Elige el tipo y completa únicamente los campos que se habiliten:
  - **Mensual:** consulta un mes del año fiscal.
  - **Rango de meses:** indica el **Mes de inicio** y el **Mes de fin**. Para consultar un solo mes también puedes poner el mismo mes en los dos campos.

### Campos opcionales

Puedes dejarlos como están la primera vez:

- **Rango de cuentas:** limita el reporte a un tramo del PUC indicando una **Cuenta inicial** y una **Cuenta final**, identificadas por su código. Si lo dejas vacío, el reporte incluye todas las cuentas con movimiento.
- **Filtrado por:** acota el reporte según el criterio que elijas, por ejemplo un tercero. Déjalo en **No aplica** para incluir todo.

### Formato de salida

Los dos reportes se descargan en cualquiera de estos formatos:

- **Excel:** una hoja de cálculo, útil si necesitas filtrar o hacer cálculos sobre los datos.
- **PDF:** el reporte listo para imprimir o archivar como soporte.

También puedes salir con **Cancelar** sin generar nada.

### Lo único que cambia entre los dos

| | Libro Auxiliar | Balance de Comprobación |
| --- | --- | --- |
| Dónde está | Grupo **Auxiliares** | Grupo **Balances** |
| Nombre del campo de período | Tipo de Auxiliar | Tipo de Balance |
| Opciones de período | Mensual, Rango de meses, Rango de fechas | Mensual, Rango de meses |
| Campo adicional | Ocultar columna de concepto | — |

El Libro Auxiliar agrega la opción **Rango de fechas**, que permite delimitar el período con una **Fecha inicial** y una **Fecha final** en lugar de meses completos, y la casilla **Ocultar columna de concepto**, que deja sin marcar para conservar el concepto de cada movimiento.

## Paso a paso

### 1. Genera el Libro Auxiliar

En el menú lateral, abre **Contabilidad** y selecciona **Reportes**. En el grupo **Auxiliares**, elige **Libro auxiliar**.

Completa los parámetros descritos arriba y descarga el reporte en Excel o PDF.

### 2. Lee el Libro Auxiliar

El reporte comienza con el encabezado de la empresa: nombre, NIT, el rango de fechas consultado, la moneda y la fecha de impresión.

Después presenta **una sección por cada cuenta contable con movimiento**. Cada sección abre con el código, la naturaleza y el nombre de la cuenta —por ejemplo `110505 - D - CAJA GENERAL`— junto con su **Saldo Anterior**.

Debajo va una tabla con los movimientos del período. Los encabezados están abreviados:

| Columna | Qué contiene |
| --- | --- |
| CTE | Número del comprobante que originó el movimiento, por ejemplo `NC-1`. |
| F/CTE | Fecha del comprobante. |
| CONCP. | Concepto del movimiento. |
| DÉBITO | Valor del movimiento cuando es débito. |
| CRÉDITO | Valor del movimiento cuando es crédito. |
| Tercero | Tercero asociado al movimiento. |
| Nro. Factura | Número de factura o soporte. |

La sección cierra con una fila de **TOTALES**, que suma los débitos y los créditos de esa cuenta, y el **Saldo final**. Al terminar una cuenta, el reporte continúa con la siguiente y repite la misma estructura.

Revisa que los movimientos correspondan a los comprobantes que registraste y que el saldo final de cada cuenta sea el esperado.

### 3. Genera el Balance de Comprobación

En el menú lateral, abre **Contabilidad** y selecciona **Reportes**. En el grupo **Balances**, elige **Balance de comprobación**.

Zoe abre la ventana **Balance de comprobación**, cuyo propósito es verificar el equilibrio contable de tus cuentas. Completa los mismos parámetros del Libro Auxiliar —año fiscal y período como obligatorios; rango de cuentas y filtrado como opcionales— y descarga el reporte en Excel o PDF.

### 4. Lee el Balance de Comprobación

El reporte comienza con el encabezado de la empresa: razón social, identificación, el rango de fechas consultado, la moneda y la fecha de impresión.

A continuación presenta una tabla con una fila por cuenta y estas columnas:

| Columna | Qué contiene |
| --- | --- |
| Código | Código de la cuenta en el PUC. |
| Nombre | Nombre de la cuenta. |
| Nat. | Naturaleza de la cuenta: **D** para débito, **C** para crédito. |
| Saldo anterior | Saldo con el que la cuenta llegó al período consultado. |
| Débito | Suma de los movimientos débito del período. |
| Crédito | Suma de los movimientos crédito del período. |
| Saldo actual | Saldo de la cuenta al cierre del período. |

Las filas se presentan de forma jerárquica: primero la clase, luego el grupo, la cuenta, la subcuenta y por último la cuenta auxiliar. Cada nivel acumula los movimientos de los niveles que tiene debajo, así que el mismo valor se repite hacia arriba en la jerarquía.

Por ejemplo, el asiento de $ 12.500 registrado en la guía del primer asiento contable aparece así:

| Código | Nombre | Nat. | Débito | Crédito |
| --- | --- | --- | ---: | ---: |
| 1 | ACTIVO | D | 12.500,00 | 0,00 |
| 11 | DISPONIBLE | D | 12.500,00 | 0,00 |
| 1105 | CAJA | D | 12.500,00 | 0,00 |
| 110505 | caja general | D | 12.500,00 | 0,00 |
| 2 | PASIVO | C | 0,00 | 12.500,00 |
| 22 | PROVEEDORES | C | 0,00 | 10.000,00 |
| 2205 | NACIONALES | C | 0,00 | 10.000,00 |
| 220501 | proveedores nacionales | C | 0,00 | 10.000,00 |
| 23 | CUENTAS POR PAGAR | C | 0,00 | 2.500,00 |
| 2365 | RETENCION EN LA FUENTE | C | 0,00 | 2.500,00 |
| 236540 | COMPRAS GENERALES | C | 0,00 | 2.500,00 |
| 23654002 | compras generales (declarantes) 2.5% | C | 0,00 | 2.500,00 |

El reporte cierra con dos bloques de verificación:

- Una fila de **TOTALES** con la suma de todos los débitos y de todos los créditos del período.
- Un bloque de **TOTAL GENERAL** con el saldo débito anterior, el saldo crédito anterior, el saldo débito actual y el saldo crédito actual.

**La comprobación que debes hacer es sencilla: el total de débitos y el total de créditos tienen que ser iguales.** En el ejemplo, ambos suman $ 12.500,00. Si no coinciden, revisa los comprobantes del período en el Libro Auxiliar para ubicar el movimiento que falta o sobra.

### El mismo asiento en los dos reportes

Aunque los parámetros sean casi idénticos, el resultado descargado se ve muy distinto. El asiento de $ 12.500 del ejemplo produce:

- En el **Libro Auxiliar**, **tres secciones**: una por cada cuenta auxiliar que recibió movimiento (110505, 220501 y 23654002), cada una con el detalle del comprobante `NC-1` que la originó.
- En el **Balance de Comprobación**, **doce filas**: las mismas tres cuentas más todos sus niveles superiores, porque el balance acumula hacia arriba en la jerarquía del PUC.

Por eso el Balance sirve para ver el panorama y comprobar el cuadre, y el Auxiliar para rastrear de dónde salió cada saldo.

## Resultado esperado

Obtienes el reporte descargado en Excel o PDF, con los movimientos y saldos del período consultado, y puedes confirmar que la información registrada es correcta y que la contabilidad está cuadrada.

## Errores frecuentes

### El reporte sale vacío

Comprueba que el año fiscal y el período seleccionados correspondan a fechas en las que registraste comprobantes.

### No aparece una cuenta que esperabas

Si indicaste un **Rango de cuentas**, verifica que la cuenta esté dentro de ese rango. El reporte solo incluye cuentas con movimiento en el período.

### El total de débitos no coincide con el de créditos

Genera el Libro Auxiliar del mismo período y revisa cuenta por cuenta hasta ubicar el movimiento que causa la diferencia.

### No encuentras el reporte descargado

Revisa la carpeta de descargas de tu navegador y confirma que no esté bloqueando las descargas del sitio.

## Artículos relacionados

- [Cómo hacer tu primer asiento contable](./primer-asiento-contable.md)
- [Cómo configurar tu Plan Único de Cuentas (PUC)](./configurar-puc.md)
- [Primeros pasos con Contabilidad](./primeros-pasos.md)
