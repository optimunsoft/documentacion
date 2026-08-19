---
title: Cómo hacer tu primer asiento contable
description: Registra, cuadra y crea un comprobante directamente en Contabilidad.
module: contabilidad
category: primeros-pasos
slug: primer-asiento-contable
order: 4
tags:
  - demo
  - asiento-contable
  - comprobante
  - registro-contable
  - debito
  - credito
  - retencion
  - optimun
  - integracion
  - pdf
  - descargar-pdf
  - primeros-pasos
draft: false
rag_exclude: false
last_updated: 2026-08-18
---

# Cómo hacer tu primer asiento contable

Registra un comprobante directamente en Contabilidad, agrega sus movimientos débito y crédito y comprueba que el asiento quede cuadrado antes de crearlo.

## Tabla de contenido

1. [Cuándo registrar un asiento directamente](#cuándo-registrar-un-asiento-directamente)
2. [Abrir Comprobantes](#1-abre-comprobantes-y-selecciona-nuevo)
3. [Completar el comprobante](#2-completa-los-datos-del-comprobante)
4. [Agregar las líneas](#3-agrega-las-líneas-del-asiento)
5. [Calcular la retención](#4-calcula-la-retención-cuando-corresponda)
6. [Cuadrar y crear el asiento](#5-cuadra-y-crea-el-asiento)
7. [Descargar el comprobante en PDF](#6-descarga-el-comprobante-en-pdf)
8. [Errores frecuentes](#errores-frecuentes)

## Cuándo registrar un asiento directamente

Utiliza esta opción para comprobantes que no se originan en el administrativo, por ejemplo una compra de papelería, un documento soporte o el pago de servicios públicos.

> Las ventas, los pagos y otros documentos administrativos se registran en Optimun de escritorio. Después de realizar la integración, aparecerán en Contabilidad y no deben digitarse nuevamente.

## Requisitos previos

- Tener una empresa seleccionada y un período contable abierto.
- Tener configurados el PUC y el tipo de documento en Contabilidad.
- Crear previamente el tercero del comprobante.
- Para calcular una retención, configurar previamente la cuenta en **Anexos**.

## Paso a paso

### 1. Abre Comprobantes y selecciona Nuevo

En el menú lateral, abre **Contabilidad**, selecciona **Comprobantes** y luego elige **Nuevo** en el listado de comprobantes.

### 2. Completa los datos del comprobante

En **Nuevo comprobante**, revisa el mes y completa la fecha. Selecciona uno de los tipos de documento creados en Contabilidad y escribe la descripción del asiento.

- **Fijar mes:** período en el que se registrará el comprobante.
- **Fecha:** fecha contable del movimiento.
- **Tipo de documento:** documento configurado que utilizarás, por ejemplo una Nota de Contabilidad.
- **Descripción:** explicación general del comprobante.

### 3. Agrega las líneas del asiento

Completa cada movimiento del asiento y selecciona **Agregar línea** cuando necesites incluir otra cuenta. En cada línea debes indicar:

- Cuenta contable.
- Concepto.
- Número de factura o soporte.
- Tercero previamente creado.
- Valor débito o crédito.
- Centro de costo, cuando aplique.

El concepto puede conservar la descripción general o modificarse para identificar mejor el movimiento, por ejemplo **Causación compra de papelería**.

### 4. Calcula la retención, cuando corresponda

Al seleccionar una cuenta de retención configurada en **Anexos**, como la cuenta mostrada en el ejemplo, Zoe habilita la calculadora. Allí presenta la cuenta, el nombre del anexo, su naturaleza, el porcentaje y el factor.

1. Escribe el valor base de la operación.
2. Revisa el valor del impuesto calculado automáticamente.
3. Selecciona **Aplicar** para agregar el valor a la línea del asiento.

### 5. Cuadra y crea el asiento

Revisa los totales al final del comprobante. El **Total débito** y el **Total crédito** deben ser iguales y la **Diferencia** debe quedar en cero. Zoe no permite crear un comprobante descuadrado.

Cuando las sumas sean iguales, selecciona **Crear**. El comprobante aparecerá en el listado con su número, fecha, total, descripción, tercero y estado.

### 6. Descarga el comprobante en PDF

Una vez creado el asiento, puedes previsualizar el comprobante y descargarlo en formato PDF para conservarlo como soporte o compartirlo.

1. Ubica el comprobante en el listado de **Comprobantes**.
2. En la barra de acciones, selecciona **Descargar PDF**.
3. Revisa la previsualización del comprobante y confirma la descarga.

## Resultado esperado

El comprobante queda creado, contabilizado y disponible en el listado de **Comprobantes** para consultarlo, descargarlo en PDF o realizar las acciones permitidas.

## Errores frecuentes

### No aparece el tipo de documento

Comprueba que el tipo de documento haya sido creado previamente en Contabilidad.

### No encuentras el tercero

Crea primero el tercero en la configuración de Contabilidad y vuelve al comprobante.

### No aparece la calculadora de retención

Verifica que la cuenta de retención esté configurada correctamente en **Anexos**.

### No puedes crear el comprobante

Revisa que todos los campos obligatorios estén completos y que la diferencia entre débito y crédito sea cero.

## Artículos relacionados

- [Primeros pasos con Contabilidad](./primeros-pasos.md)
- [Cómo crear tu primera empresa (demo)](./crear-primera-empresa.md)
- [Cómo configurar tu Plan Único de Cuentas (PUC)](./configurar-puc.md)
- [Cómo generar reportes básicos para validar tu información](./reportes-basicos.md)
