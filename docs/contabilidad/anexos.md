---
title: Anexos y calculadora de impuestos
description: Configuración de Anexos contables por empresa y año fiscal en Zoe Nube. Cubre la pantalla de Anexos (Contabilidad > Configuración > Anexos), la creación de un anexo con código, nombre y una o varias cuentas del PUC con porcentaje, naturaleza débito/crédito y factor, la copia de anexos desde otro año fiscal o empresa con la ventana «Copiar anexos», el carácter opcional de los anexos, la calculadora «Calculo Valor Retención» que se abre en los comprobantes al elegir una cuenta de un anexo, el Certificado de Retenciones y los reportes Reporte de Anexos y Configuración de Anexos.
module: contabilidad
category: configuracion
slug: anexos
order: 9
tags:
  - configuracion
  - anexos
  - anexo
  - retenciones
  - retencion-en-la-fuente
  - retefuente
  - iva
  - reteica
  - impuestos
  - puc
  - calculadora
  - valor-base
  - porcentaje
  - tarifa
  - naturaleza
  - factor
  - debito
  - credito
  - comprobantes
  - certificado-de-retenciones
  - reporte-de-anexos
  - copiar-anexos
  - ano-nuevo
  - configuracion-de-anexos
  - ano-fiscal
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-24
---

# Anexos y calculadora de impuestos

Los Anexos en Zoe Nube son grupos de cuentas contables del Plan Único de Cuentas (PUC) que la empresa configura por año fiscal. A cada cuenta del grupo se le asigna un porcentaje, una naturaleza (débito o crédito) y un factor. Cuando en un comprobante se elige una cuenta que pertenece a un anexo, Zoe abre una calculadora que obtiene el valor del impuesto a partir de la base. La información registrada con esas cuentas se consulta después en el Certificado de Retenciones y en los reportes del grupo Anexos. Este documento describe la pantalla, la creación de un anexo, la calculadora, el certificado y los reportes.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Concepto: qué son los Anexos](#concepto-qué-son-los-anexos)
4. [Nota aclaratoria: uso no obligatorio](#nota-aclaratoria-uso-no-obligatorio)
5. [Elementos de la pantalla de Anexos](#elementos-de-la-pantalla-de-anexos)
6. [Crear un anexo: cuentas, porcentajes y naturaleza](#crear-un-anexo-cuentas-porcentajes-y-naturaleza)
7. [Copiar anexos desde otro año fiscal o empresa](#copiar-anexos-desde-otro-año-fiscal-o-empresa)
8. [Calculadora en comprobantes contables](#calculadora-en-comprobantes-contables)
9. [Certificado de Retenciones](#certificado-de-retenciones)
10. [Reportes del grupo Anexos](#reportes-del-grupo-anexos)
11. [Errores frecuentes](#errores-frecuentes)
12. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
13. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Anexos`.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / ANEXOS`.
- **Título de la pantalla:** «Anexos», con el subtítulo «Configura y gestiona los anexos contables de tu empresa».
- **Contexto:** el año fiscal de trabajo se muestra en el contenedor azul del menú lateral. Los anexos que se ven son los de ese año.

---

## Requisitos previos

1. Tener una empresa creada y seleccionada en Zoe.
2. Estar trabajando en el año fiscal que se quiere configurar.
3. Tener en el PUC las cuentas que se van a incluir en el anexo, por ejemplo subcuentas del grupo 2365 (retención en la fuente) o 1355 (anticipo de impuestos).

---

## Concepto: qué son los Anexos

Un **Anexo** es un registro por empresa y año fiscal que tiene:

- Un **Código** (por ejemplo `001`) y un **Nombre** (por ejemplo «Retenciones»).
- Una o varias **cuentas del PUC**. Cada cuenta lleva su propio **porcentaje**, **naturaleza** (Débito o Crédito) y **factor**.

Ejemplo real de configuración (tomado del reporte «Configuración de Anexos», año fiscal 2026):

| Anexo | Código cuenta | Nombre de cuenta | Naturaleza | Porcentaje |
| :--- | :--- | :--- | :--- | :--- |
| 001 - RETENCIONES | 23654001 | COMPRAS GENERALES (NO DECLARANTES) 3.5% | D | 3,50% |
| 001 - RETENCIONES | 23654002 | COMPRAS GENERALES (DECLARANTES) 2.5% | C | 2,50% |
| 002 - ANTICIPO RETEFTE 2.5% | 13551501 | ANTCIPO RETE FTE 2.5% | D | 2,50% |

### Flexibilidad

El uso más común es la retención en la fuente, pero la empresa puede armar anexos para IVA, ReteICA u otros impuestos, según su gestión interna.

---

## Nota aclaratoria: uso no obligatorio

> [!IMPORTANT]
> **El uso de Anexos NO es obligatorio en Zoe.**
>
> Se pueden registrar comprobantes y digitar los valores de los impuestos a mano sin haber creado ningún anexo.
>
> Se recomienda configurarlos porque:
> 1. Activan la calculadora en los comprobantes, que evita errores de digitación y de cálculo.
> 2. Organizan las cuentas de retenciones que luego se consultan en el Reporte de Anexos y en el Certificado de Retenciones.

---

## Elementos de la pantalla de Anexos

| Elemento | Función |
| :--- | :--- |
| **Campo Consultar + botón Filtrar** | Busca anexos en el listado. |
| **Botón Nuevo** | Abre la ventana «Nuevo anexo». |
| **Botón Copiar** | Abre la ventana «Copiar anexos» para traer los anexos de otro año fiscal o de otra empresa al año actual. |
| **Selector Columnas** | Elige qué columnas se muestran en la tabla. |
| **Tabla «Listado de anexos»** | Columnas: **ID**, **Código**, **Nombre**, **Cuentas configuradas** (número de cuentas del anexo) y **Acciones**. Muestra el total de registros junto al título. |
| **Acciones de fila** | Editar (ícono de lápiz) y eliminar (ícono de papelera). |
| **Paginación** | Navegación entre páginas y selector de registros por página (por defecto 7). |

---

## Crear un anexo: cuentas, porcentajes y naturaleza

1. Ingresar a `Contabilidad > Configuración > Anexos`.
2. Hacer clic en **Nuevo**. Se abre la ventana **Nuevo anexo** («Crea un nuevo anexo contable»).
3. Completar los campos obligatorios del encabezado:
   - **Código\***: identificador del anexo (ej. `004`).
   - **Nombre\***: nombre descriptivo (ej. `IVA Retenido 15%`).
4. Hacer clic en **Agregar cuenta**. Se agrega una fila con estas columnas:

   | Columna | Contenido |
   | :--- | :--- |
   | **Cuenta** | Lista desplegable para buscar la cuenta del PUC (se muestra como `código - nombre`, ej. `13551701 - Iva retenido 15%`). |
   | **%** | Porcentaje o tarifa (ej. `15`). |
   | **Nat.** | Naturaleza: `Débito` o `Crédito`. |
   | **Factor** | Lista desplegable con el divisor del cálculo (valor mostrado: `100`). |
   | **Acciones** | Ícono de papelera para quitar la fila. |

5. Repetir **Agregar cuenta** por cada cuenta adicional. Las filas se paginan dentro de la ventana.
6. Hacer clic en **Crear** (o **Cancelar** para salir sin guardar). El anexo aparece en el listado con su número de cuentas configuradas.

---

## Copiar anexos desde otro año fiscal o empresa

Como los anexos son por año fiscal, el botón **Copiar** permite traer la configuración de un año que ya la tenga, sin crear los anexos uno por uno.

1. Entrar al año fiscal de destino desde el contenedor azul del menú lateral.
2. En `Contabilidad > Configuración > Anexos`, hacer clic en **Copiar**. Se abre la ventana **Copiar anexos**.
3. Completar el bloque **Origen**:

   | Campo | Obligatorio | Contenido |
   | :--- | :--- | :--- |
   | **Empresa de origen** | Sí | Lista desplegable con las empresas del usuario (puede ser la misma empresa u otra). |
   | **Año fiscal de origen** | Sí | Lista desplegable con los años fiscales de la empresa elegida (ej. 2023, 2022, 2019…). |

4. Revisar el bloque **Destino**, que no es editable:
   - **Empresa de destino:** la empresa en la que se está trabajando.
   - **Año fiscal de destino:** el año fiscal de trabajo (ej. 2026).
5. Leer el aviso: «Esta acción sobreescribira la configuración de cuentas de anexos del año fiscal actual.»
6. Hacer clic en **Copiar anexos**, o en **Cancelar** para salir sin copiar.

> [!WARNING]
> La copia **sobrescribe** la configuración de cuentas de anexos del año fiscal actual. Si el año de destino ya tiene anexos configurados, conviene revisarlos antes de copiar.

---

## Calculadora en comprobantes contables

### Comportamiento en la interfaz

Al registrar un comprobante, cuando se elige en una línea una cuenta que pertenece a un anexo del año fiscal de trabajo, Zoe abre la ventana **Calculo Valor Retención** con:

- **Cuenta:** código de la cuenta (ej. `23654002`).
- **Nombre Anexo:** nombre del anexo (ej. `RETENCIONES`).
- **Nat:** naturaleza configurada (ej. `Crédito`).
- **%:** porcentaje configurado (ej. `2,5`).
- **Factor:** factor configurado (ej. `100`).
- **Devolución:** casilla de verificación.
- **Valor Base:** campo donde el usuario escribe la base de la operación.
- **Valor Impuesto:** resultado calculado.
- Botones **Cerrar** y **Aplicar**.

### Cálculo

`Valor Impuesto = Valor Base × Porcentaje ÷ Factor`

Ejemplo verificado: Valor Base `$ 100.000`, porcentaje `2,5`, factor `100` → Valor Impuesto `$ 2.500,00`.

**Aplicar** lleva el valor al comprobante. **Cerrar** cierra la ventana sin aplicarlo, y el valor se puede digitar a mano.

### Recomendación de uso

Usar la calculadora no es obligatorio, pero se recomienda usarla siempre que aparezca, para garantizar que el valor corresponda exactamente al porcentaje configurado en el anexo.

---

## Certificado de Retenciones

- **Ruta:** `Contabilidad > Reportes`, grupo **Certificados**, opción **Certificado de Retenciones**.
- **Ventana:** «Certificado de Retenciones — Genera certificados de retenciones».

| Campo | Obligatorio | Contenido |
| :--- | :--- | :--- |
| **Año fiscal** | Sí | Año a certificar. |
| **Tercero** | Sí | Tercero al que se expide el certificado; se busca por nombre o NIT. |
| **Cuenta inicial / Cuenta final** (Rango de cuentas) | No | Rango de cuentas que entra en el certificado. |
| **Tipo de certificado** | Sí | Clase de certificado (ej. `Retención en la fuente`). |

- **Salida:** botón **PDF**. Botón **Cancelar** para salir.
- El certificado se genera por tercero: el campo Tercero es obligatorio.

---

## Reportes del grupo Anexos

En `Contabilidad > Reportes`, el grupo **Anexos** tiene dos reportes, ambos marcados «Excel y PDF».

### Reporte de Anexos

El PDF se titula «REPORTE ANEXO AGRUPADO». Encabezado: razón social, NIT, «Valores en pesos colombianos (COP)», fecha y zona horaria de impresión. Bloque **PARAMETROS** con: Anexo, Año fiscal, Rango de fechas, Rango de cuentas y Tercero.

El cuerpo se agrupa por cuenta (`CUENTA 23654002 - COMPRAS GENERALES (DECLARANTES) 2.5%`) y cada grupo tiene las columnas:

| NIT | Nombre | % | Base | Débito | Crédito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 123456789 | Jhon Dario Sanchez | 2,50% | 100.000,00 | 0,00 | 2.500,00 |
| **TOTALES** | | - | - | 0,00 | 2.500,00 |

Sirve para revisar bases y retenciones por tercero y cuenta antes de declarar o de expedir certificados.

### Configuración de Anexos

El PDF se titula «CONFIGURACIÓN DE ANEXOS». Bloque **PARAMETROS** con el año fiscal. Lista cada anexo (`Anexo: 001 - RETENCIONES`) con sus cuentas y las columnas **Código**, **Nombre de Cuenta**, **Naturaleza** y **Porcentaje**. Sirve para revisar o archivar la configuración vigente del año.

---

## Errores frecuentes

### La calculadora no se abre al elegir la cuenta en el comprobante
- **Causa:** la cuenta no pertenece a ningún anexo del año fiscal de trabajo.
- **Solución:** verificar el año en el contenedor azul del menú lateral y confirmar en `Contabilidad > Configuración > Anexos` que la cuenta esté agregada a un anexo de ese año.

### Al cambiar de año fiscal no aparecen los anexos
- **Causa:** los anexos se configuran por año fiscal; cada año tiene su propio listado.
- **Solución:** traerlos del año anterior con el botón **Copiar** (ventana «Copiar anexos») o crearlos con **Nuevo**.

### No se puede crear el anexo
- **Causa:** falta el Código o el Nombre, que son obligatorios.
- **Solución:** completar ambos campos antes de hacer clic en **Crear**.

---

## Resumen de reglas de negocio

| # | Regla de negocio |
| :--- | :--- |
| 1 | Los Anexos se configuran por **empresa y año fiscal**. |
| 2 | El uso de Anexos **NO es obligatorio** para registrar comprobantes. |
| 3 | Un anexo tiene **Código** y **Nombre** obligatorios y una o varias cuentas del PUC. |
| 4 | Cada cuenta del anexo tiene su propio **porcentaje**, **naturaleza** (Débito/Crédito) y **factor**. |
| 5 | La calculadora «Calculo Valor Retención» se abre al elegir en un comprobante una cuenta que pertenece a un anexo del año de trabajo. |
| 6 | La calculadora calcula `Valor Base × Porcentaje ÷ Factor`; con factor 100 el porcentaje se aplica de la forma habitual. |
| 7 | Usar la calculadora es opcional (**Cerrar** permite digitar a mano), pero se recomienda. |
| 8 | El Certificado de Retenciones se genera por tercero (campo obligatorio) y sale en PDF. |
| 9 | «Copiar anexos» exige empresa y año fiscal de origen; el destino es siempre la empresa y el año de trabajo, y la copia sobrescribe la configuración de cuentas de anexos de ese año. |

---

## Preguntas frecuentes

**¿Qué diferencia hay entre un Anexo y una cuenta del PUC?**
La cuenta del PUC es el código donde se registra el movimiento (ej. 23654002). El anexo agrupa una o varias de esas cuentas y le indica a Zoe con qué porcentaje, naturaleza y factor calcular el valor en la calculadora.

**¿Se pueden incluir varias cuentas en un mismo anexo?**
Sí. Con **Agregar cuenta** se añaden tantas filas como cuentas se necesiten, y cada una lleva su propio porcentaje y naturaleza. Ejemplo: el anexo `001 - RETENCIONES` agrupa 23654001 al 3,50% (D) y 23654002 al 2,50% (C).

**¿Dónde veo cuánto se retuvo a cada tercero?**
En `Contabilidad > Reportes`, grupo **Anexos**, opción **Reporte de Anexos**: muestra por cuenta y tercero el porcentaje, la base, el débito y el crédito.
