---
title: Certificado de Retenciones
description: Reporte del grupo Certificados en Contabilidad > Reportes de Zoe Nube. Cubre el Certificado de Retenciones de un tercero para todo un año fiscal (retención en la fuente, retención de IVA, retención de ICA, avisos y tableros, tasa bomberil y dividendos), sus parámetros (año fiscal, tercero, rango de cuentas, tipo de certificado), su única salida en PDF, la estructura del certificado (datos de la empresa, datos del tercero, período, conceptos con base, porcentaje y valor retenido, total en letras, texto legal y fecha de expedición) y los errores frecuentes.
module: contabilidad
category: reportes
slug: reportes-certificados
order: 15
tags:
  - reportes
  - certificados
  - certificado-de-retenciones
  - retencion-en-la-fuente
  - retencion-de-iva
  - retencion-de-ica
  - avisos-y-tableros
  - tasa-bomberil
  - dividendos
  - tercero
  - nit
  - base
  - porcentaje
  - valor-retenido
  - rango-de-cuentas
  - año-fiscal
  - dian
  - pdf
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-29
---

# Certificado de Retenciones

El grupo **Certificados** de la pantalla **Reportes Financieros** (`Contabilidad > Reportes`) tiene una sola opción: el **Certificado de Retenciones**. Genera el certificado de un tercero para todo el año fiscal seleccionado, del 1 de enero al 31 de diciembre, y se descarga únicamente en PDF.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Tipos de certificado](#tipos-de-certificado)
4. [Parámetros de la ventana](#parámetros-de-la-ventana)
5. [Cómo generarlo](#cómo-generarlo)
6. [Estructura del certificado](#estructura-del-certificado)
7. [Errores frecuentes](#errores-frecuentes)
8. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Reportes`.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `PANEL / REPORTES`.
- **Grupo:** **CERTIFICADOS**, con la tarjeta «Certificado de Retenciones».
- **Ventana:** título «Certificado de Retenciones», subtítulo «Genera certificados de retenciones».

---

## Requisitos previos

1. Tener una empresa seleccionada en Zoe.
2. Que el tercero exista en Zoe (ver `terceros.md`).
3. Que el tercero tenga movimientos en el año fiscal, en las cuentas de retención que se certifican.

---

## Tipos de certificado

| Tipo de certificado |
| :--- |
| Retención en la fuente |
| Retención de IVA |
| Retención de ICA |
| Avisos y tableros |
| Tasa bomberil |
| Dividendos |

Cada tipo tiene su título y su texto legal. Por ejemplo, el de ICA se titula «CERTIFICADO DE RETENCIÓN DE ICA» y el de IVA «CERTIFICADO DE RETENCIÓN EN LA FUENTE POR IVA».

---

## Parámetros de la ventana

| Parámetro | Obligatorio | Descripción |
| :--- | :---: | :--- |
| **Año fiscal** | Sí | Año fiscal a certificar. El período certificado es del 1 de enero al 31 de diciembre de ese año. |
| **Tercero** | Sí | Buscador «Buscar por nombre o NIT». Cada opción muestra nombre y NIT (por ejemplo `Grupo Fortex S.a - 900539512`). Al elegirlo, se muestra con su NIT. |
| **Cuenta inicial** y **Cuenta final** (Rango de cuentas) | No | Limitan el certificado a los conceptos tributarios de un rango de cuentas. Las listas muestran las clases del PUC, por ejemplo `1 - D - Activo` y `5 - D - Gastos`. |
| **Tipo de certificado** | Sí | Lista con los seis tipos. |

Botones de la ventana: **Cancelar** y **PDF**. No existe botón de Excel.

---

## Cómo generarlo

1. En el grupo **Certificados**, elegir **Certificado de Retenciones**.
2. Elegir el **Año fiscal**.
3. En **Tercero**, buscar por nombre o NIT y seleccionar el tercero.
4. Opcionalmente, elegir la **Cuenta inicial** y la **Cuenta final** para incluir solo los conceptos tributarios deseados.
5. En **Tipo de certificado**, elegir uno de los seis tipos.
6. Hacer clic en **PDF**.

Si no existen movimientos para el tercero y los criterios seleccionados, el certificado no se genera.

---

## Estructura del certificado

| Parte | Contenido |
| :--- | :--- |
| **Encabezado** | Nombre, NIT y correo de la empresa que expide el certificado. |
| **Título** | Tipo de certificado, por ejemplo «CERTIFICADO DE RETENCIÓN DE ICA». |
| **Texto legal inicial** | Fórmula legal propia del tipo de certificado, seguida de «CERTIFICA» y de «1. Que durante el año gravable 2026 efectuamos retenciones a:» (en los certificados de IVA, «efectuamos retenciones en la fuente a:»). |
| **Datos del tercero** | **Nombre del Contribuyente**, **NIT**, **Dirección** y **Teléfono**. |
| **Período** | **Periodo inicial** (Enero 1 de 2026) y **Periodo final** (Diciembre 31 de 2026). |
| **Tabla de conceptos** | Columnas **Concepto**, **Base**, **%** y **Vlr. Retención**; una fila por concepto (por ejemplo `Cajas menor`, `Proveedores nacionales`, `VENTAS EXCLUIDAS`). |
| **Total** | «Total: $ 60.000,00» y el valor en letras, «SON: SESENTA MIL PESOS M/CTE». |
| **Cierre** | «2. Que la totalidad de las retenciones antes indicadas fueron consignadas oportunamente en las entidades autorizadas por la Dirección de Impuestos y Aduanas Nacionales DIAN, de dentro de los terminos legales.», la nota «Esta certificación se expide sin firma autógrafa de acuerdo con el Art. 10 del Decreto 836 del 23 de Marzo de 1991» y la **FECHA DE EXPEDICIÓN** (por ejemplo «Septiembre 29 de 2026»). |
| **Pie de página** | Fecha de impresión con zona horaria, «Zoe Contabilidad» y número de página. |

---

## Errores frecuentes

| Situación | Causa y solución |
| :--- | :--- |
| No se genera el certificado | El tercero no tiene movimientos para el año fiscal, el rango de cuentas y el tipo de certificado elegidos. Probar con otro tipo, ampliar el rango de cuentas o revisar los comprobantes del tercero. |
| No aparece el tercero en el buscador | Buscar por nombre y por NIT. Si no aparece, confirmar que esté creado en Terceros. |
| El certificado no incluye un concepto esperado | La cuenta del concepto está fuera del rango de cuentas elegido o no corresponde al tipo de certificado. |
| No se encuentra el archivo descargado | Revisar la carpeta de descargas del navegador y que no bloquee las descargas del sitio. |

---

## Preguntas frecuentes

**¿Qué período cubre el certificado?**
Todo el año fiscal elegido: del 1 de enero al 31 de diciembre.

**¿Puedo generar el certificado en Excel?**
No. El Certificado de Retenciones se descarga únicamente en PDF.

**¿Qué tipos de certificado puedo generar?**
Retención en la fuente, retención de IVA, retención de ICA, avisos y tableros, tasa bomberil y dividendos.

**¿Para qué sirve el rango de cuentas?**
Para que el certificado incluya solo los conceptos tributarios de las cuentas que se necesitan.

**¿Quién firma el certificado?**
Ninguno: el certificado se expide sin firma autógrafa, con base en el Art. 10 del Decreto 836 de 1991, como lo indica el propio documento.

**¿Se puede certificar a varios terceros a la vez?**
No. Cada certificado se genera para un solo tercero.
