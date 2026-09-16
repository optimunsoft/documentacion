---
title: Anexos y calculadora de impuestos
description: Configuración de tablas de anexos contables por empresa y año fiscal para la liquidación de retenciones, IVA y otros tributos. Cubre la pantalla de Anexos, la creación y edición de registros, la vinculación de cuentas contables del PUC con porcentajes y naturaleza débito/crédito, la copia de configuración entre años fiscales, la activación automática de la calculadora de impuestos en los comprobantes contables, la no obligatoriedad de su uso, la generación masiva de certificados de retenciones y la consulta de reportes analíticos de anexos.
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
  - base-gravable
  - porcentaje
  - tarifa
  - naturaleza
  - debito
  - credito
  - comprobantes
  - certificados-de-retencion
  - reportes-anexos
  - cierre-fiscal
  - ano-fiscal
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-16
---

# Anexos y calculadora de impuestos

Los Anexos en Zoe Nube son tablas de parametrización tributaria estructuradas por empresa y año fiscal que permiten agrupar cuentas contables del Plan Único de Cuentas (PUC) asignándoles un porcentaje (tarifa) y una naturaleza contable específica (débito o crédito). Su objetivo principal es automatizar el cálculo de retenciones e impuestos en los comprobantes contables mediante una calculadora rápida, garantizar la exactitud en la captura de las bases gravables y permitir la generación masiva e instantánea de certificados de retención y reportes analíticos al cierre del ejercicio. Este documento detalla la ubicación de la pantalla, la lógica de configuración, el comportamiento de la calculadora en los comprobantes, su carácter opcional y su impacto en reportes y certificados.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Concepto: qué son los Anexos](#concepto-qué-son-los-anexos)
4. [Alcance: configuración por empresa y año fiscal](#alcance-configuración-por-empresa-y-año-fiscal)
5. [Nota aclaratoria: uso no obligatorio](#nota-aclaratoria-uso-no-obligatorio)
6. [Elementos de la pantalla de Anexos](#elementos-de-la-pantalla-de-anexos)
7. [Asociación de cuentas, porcentajes y naturaleza](#asociación-de-cuentas-porcentajes-y-naturaleza)
8. [Copiar Anexos entre años fiscales](#copiar-anexos-entre-años-fiscales)
9. [Calculadora automática en comprobantes contables](#calculadora-automática-en-comprobantes-contables)
10. [Impacto en reportes y certificados al cierre de año](#impacto-en-reportes-y-certificados-al-cierre-de-año)
11. [Solución de problemas y errores frecuentes](#solución-de-problemas-y-errores-frecuentes)
12. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
13. [Preguntas frecuentes](#preguntas-frecuentes)

---

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Anexos`.
- **Ruta de navegación mostrada en pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / ANEXOS`.
- **Título de la pantalla:** «Anexos».
- **Contexto visual:** El año fiscal activo y la empresa seleccionada se muestran permanentemente en el contenedor azul del sidebar.

---

## Requisitos previos

1. Contar con una empresa creada y seleccionada en Zoe.
2. Disponer de permisos de acceso al módulo de `Contabilidad`.
3. Tener activo el año fiscal correspondiente en el que se aplicarán las operaciones.
4. Tener previamente creadas en el PUC las cuentas auxiliares imputables donde se contabilizarán las retenciones o impuestos (por ejemplo, subcuentas del grupo 2365 para retención en la fuente, 2408 para IVA, o 2368 para ReteICA).

---

## Concepto: qué son los Anexos

Un **Anexo** es una regla de parametrización contable que asocia una o varias cuentas auxiliares del PUC con:
- Una tarifa o **porcentaje** de cálculo.
- Una **naturaleza contable** predeterminada (Débito o Crédito).
- Un **factor de cálculo** (base divisora estándar de 100).
- Un **nombre descriptivo** que identifica el concepto fiscal.

### Flexibilidad tributaria

Aunque la aplicación más extendida de los Anexos es la configuración de las **Retenciones en la fuente a título de renta** (compras 2.5%, servicios 4%, honorarios 10% o 11%, arrendamientos 3.5%), la herramienta es completamente flexible y se utiliza para:
- **Retenciones de IVA (ReteIVA):** Cuentas de retención aplicadas en operaciones con régimen común / responsables de IVA.
- **Retenciones de Industria y Comercio (ReteICA):** Retenciones municipales según la actividad económica y tarifas distritales/municipales (por ejemplo, 4.14‰, 6.9‰, 9.66‰, 11.04‰).
- **IVA descontable y generado:** Automatización de bases e impuestos sobre ventas o compras.
- **Autorretenciones:** Autorretención especial a título de renta u otras retenciones autorreguladas.

---

## Alcance: configuración por empresa y año fiscal

A diferencia de los Terceros (que son globales y pertenecen a la empresa completa sin importar el año), los **Anexos pertenecen al año fiscal activo**:
- Cada año fiscal contiene su propio catálogo de anexos.
- Esto permite que si la normativa tributaria nacional o municipal modifica las tarifas de retención o las bases de un año a otro, los cambios se configuren en el nuevo año fiscal sin alterar ni recalcular la información histórica contabilizada en años anteriores.
- Al habilitar un año fiscal nuevo, los anexos no se trasladan automáticamente en blanco: el usuario dispone de la función **Copiar** para replicar la estructura del año previo en un solo paso.

---

## Nota aclaratoria: uso no obligatorio

> [!IMPORTANT]
> **El uso de Anexos NO es obligatorio en Zoe.**
> 
> La plataforma permite a los usuarios registrar comprobantes contables y cuadrar asientos ingresando las cuentas y los importes de impuestos manualmente línea por línea. No existe ninguna restricción de guardado que exija que una cuenta deba estar en un anexo.
>
> **Sin embargo, su uso es altamente recomendado por tres razones críticas:**
> 1. **Prevención de errores humanos:** Evita discrepancias por errores de digitación o cálculo mental de tarifas y centavos.
> 2. **Captura de la base gravable:** Al usar la calculadora, el sistema almacena internamente la base del cálculo vinculada al movimiento contable.
> 3. **Generación automática de certificados:** Sin anexos y sin base registrada, el módulo de Certificados de Retención no puede consolidar automáticamente la información para los proveedores al cierre del año.

---

## Elementos de la pantalla de Anexos

En la vista principal de `Contabilidad > Configuración > Anexos` se encuentran los siguientes elementos de control:

| Elemento | Tipo | Función |
| :--- | :--- | :--- |
| **Campo de búsqueda** | Filtro de texto | Permite filtrar el listado de anexos por nombre, código de cuenta o concepto. |
| **Botón Nuevo** | Botón de acción | Despliega el formulario para crear un anexo nuevo en el año fiscal activo. |
| **Botón Copiar** | Botón de acción | Permite seleccionar otro año fiscal para copiar masivamente sus anexos hacia el año actual. |
| **Tabla de Anexos** | Vista de datos | Muestra el listado de registros con las columnas: Nombre del Anexo, Cuentas asociadas, Naturaleza, Porcentaje (%) y Factor. |
| **Acciones de fila** | Menú por registro | Permite **Editar** los parámetros de un anexo existente o **Eliminarlo** si no es requerido. |

---

## Asociación de cuentas, porcentajes y naturaleza

Para configurar un Anexo en el sistema:

1. Ingresa a `Contabilidad > Configuración > Anexos`.
2. Haz clic en el botón **Nuevo**.
3. Diligencia los campos requeridos en el formulario:
   - **Nombre del Anexo:** Texto descriptivo del tributo y tarifa (ej. *Retención en la fuente 2.5% compras declarantes*).
   - **Naturaleza:** Selecciona entre:
     - **Crédito:** Utilizado en retenciones practicadas que representan un pasivo por pagar a la administración tributaria (DIAN / Municipio).
     - **Débito:** Utilizado para retenciones que le practicaron a la empresa (anticipos de impuestos / activo) o IVA descontable.
   - **Porcentaje (%):** Valor numérico de la tarifa tributaria aplicable (ej. `2.5`, `3.5`, `4.0`, `19.0`).
   - **Factor:** Denominador de cálculo porcentual (valor predeterminado: `100`).
   - **Cuentas contables asociadas:** Selecciona del PUC la cuenta o subcuenta contable a la que aplicará esta parametrización.
4. Presiona **Guardar**.

---

## Copiar Anexos entre años fiscales

Cuando la empresa crea o habilita un año fiscal nuevo (por ejemplo, el paso de 2025 a 2026):

1. Cambia al nuevo año fiscal desde el selector ubicado en el contenedor azul del sidebar.
2. Dirígete a `Contabilidad > Configuración > Anexos`.
3. Haz clic en el botón **Copiar**.
4. En la ventana emergente, selecciona el año fiscal de origen desde el cual deseas traer la información (ej. 2025).
5. Confirma la acción.
6. Zoe creará en el año activo una réplica exacta de todos los anexos del año origen, vinculando las cuentas del PUC homologadas del nuevo año. Si alguna tarifa varió para el nuevo año (por reforma tributaria o cambio de UVT), se edita puntualmente el anexo correspondiente.

---

## Calculadora automática en comprobantes contables

La principal ventaja operativa de parametrizar los anexos se manifiesta en la pantalla de **Nuevo Comprobante** (o edición de comprobantes).

### Comportamiento en la interfaz

Cuando el usuario agrega una línea a un asiento y digita o selecciona una cuenta contable que pertenece a un anexo:
1. El sistema detecta automáticamente la asociación y despliega la ventana modal **Cálculo Valor Retención**.
2. La ventana presenta los datos del anexo en modo de solo lectura:
   - **Cuenta:** Código contable seleccionado.
   - **Nombre Anexo:** Nombre asignado al anexo.
   - **Nat:** Naturaleza contable predeterminada (Débito o Crédito).
   - **%:** Tarifa parametrizada.
   - **Factor:** Factor divisor (100).
   - **Devolución:** Casilla de verificación para registrar reversiones de retenciones por notas crédito o devoluciones de compras/ventas.
3. El cursor se posiciona en el campo **Valor Base**.
4. El usuario escribe el monto base de la transacción (por ejemplo, el subtotal antes de impuestos).
5. En tiempo real, el sistema calcula el **Valor Impuesto** mediante la fórmula:
   $$\text{Valor Impuesto} = \frac{\text{Valor Base} \times \text{Porcentaje}}{\text{Factor}}$$
6. Al presionar el botón **Aplicar**, Zoe:
   - Inserta el valor calculado en la columna débito o crédito según la naturaleza fijada.
   - Vincula el valor de la base gravable a la línea del comprobante para alimentar los reportes y certificados.
7. Si el usuario presiona **Cerrar** o cancela la ventana, la línea permanece disponible para digitación manual del valor.

### Recomendación de uso

Se recomienda utilizar **siempre** la calculadora cuando aparezca disponible. Omitir la calculadora e ingresar el valor a mano impide que la base gravable quede registrada en los metadatos del asiento, lo que generará que los certificados de retención aparezcan con bases en cero o incompletas.

---

## Impacto en reportes y certificados al cierre de año

Al finalizar el periodo contable o al cierre del año fiscal, la información registrada a través de los Anexos alimenta directamente dos módulos esenciales:

### 1. Certificados de Retenciones (`Reportes > Certificados > Certificados de Retenciones`)
- **Propósito:** Expedir los certificados oficiales de retención en la fuente a título de renta, IVA e ICA que las empresas están obligadas por ley a entregar a sus proveedores.
- **Funcionamiento masivo:** Zoe totaliza los movimientos del año filtrando por tercero (NIT/nombre) y por anexo/concepto.
- **Resultado:** En lugar de revisar comprobante por comprobante o extraer hojas de cálculo auxiliares, el usuario puede generar de forma masiva en un solo clic todos los certificados del año en formato PDF (o descargarlos en un archivo comprimido .ZIP).

### 2. Reportes de Anexos (`Reportes > Anexos`)
- **Reporte de Anexos:** Presenta una relación analítica detallada de todos los movimientos del año discriminando Tercero, Tipo y Número de Documento, Fecha, Base Gravable, Tarifa y Valor Retenido. Es la base fundamental para elaborar y conciliar las declaraciones mensuales tributarias (Formulario 350 de Retención en la Fuente, Formulario 300 de IVA).
- **Configuración de Anexos:** Reporte de auditoría que imprime el listado maestro de cuentas y porcentajes activos en el periodo para efectos de control contable.

---

## Solución de problemas y errores frecuentes

### La calculadora no se activa al seleccionar la cuenta en el comprobante
- **Causa 1:** La cuenta no está vinculada a ningún anexo en el año fiscal en curso. Si fue configurada en el año anterior, debe copiarse o crearse en el año activo.
- **Causa 2:** Se seleccionó una cuenta de nivel superior (cuenta de grupo o mayor) que no es auxiliar imputable.
- **Solución:** Ve a `Contabilidad > Configuración > Anexos`, verifica el año activo en el sidebar y comprueba que la cuenta auxiliar figure en la tabla.

### Los anexos desaparecieron o la tabla está vacía
- **Causa:** Se cambió el año de trabajo desde el sidebar a un año nuevo que aún no ha sido parametrizado.
- **Solución:** Utiliza el botón **Copiar** para importar los anexos del año fiscal anterior.

### El certificado de retenciones sale con base gravable en cero
- **Causa:** Al momento de elaborar los comprobantes, los usuarios digitaron los valores de retención directamente en la celda débito/crédito sin ingresar la base en la ventana modal de la calculadora rápida.
- **Solución:** Para que el certificado refleje la base, los comprobantes deben registrarse utilizando la calculadora rápida del anexo.

### ¿Se pueden vincular varias cuentas a un mismo anexo?
- **Respuesta:** Sí. Por ejemplo, un anexo denominado «IVA Generado 19%» puede agrupar diferentes subcuentas contables si comparten la misma tarifa y naturaleza. Sin embargo, no es aconsejable asignar una misma cuenta contable a múltiples anexos distintos, ya que provocaría ambigüedad en el cálculo automático.

---

## Resumen de reglas de negocio

| # | Regla de negocio |
| :--- | :--- |
| 1 | Los Anexos pertenecen al **año fiscal activo**, no son globales a la empresa. |
| 2 | El uso de Anexos **NO es obligatorio** para registrar transacciones ni cerrar periodos en Zoe. |
| 3 | La calculadora automática se activa al seleccionar en un comprobante una cuenta asociada a un anexo del año activo. |
| 4 | La calculadora calcula: `(Valor Base × Porcentaje) ÷ Factor`. El factor estándar es 100. |
| 5 | La base gravable solo se registra en la base de datos si se utiliza el botón **Aplicar** de la calculadora en el comprobante. |
| 6 | Los anexos se replican en años fiscales nuevos mediante el botón **Copiar**. |
| 7 | Los Certificados de Retención consolidan la información anual agrupada por tercero a partir de las cuentas y bases vinculadas en los Anexos. |

---

## Preguntas frecuentes

**¿Qué diferencia hay entre un Anexo y una cuenta del PUC?**  
La cuenta del PUC es el código donde se registra el saldo financiero (ej. 23654002). El Anexo es la regla de negocio asociada a esa cuenta que le indica al sistema cuál es la tarifa impositiva (2.5%), cuál es su naturaleza habitual (Crédito) y cómo debe calcularse la base.

**¿Puedo modificar la tarifa de un anexo a mitad de año?**  
Sí, pero afectará los comprobantes que se registren a partir de ese momento. Los comprobantes contabilizados previamente conservan los valores con los que fueron aprobados.

**¿Qué pasa con los Anexos si elimino una cuenta del PUC?**  
Si una cuenta del PUC es eliminada o inactivada, las asociaciones huérfanas en Anexos deben ser eliminadas o actualizadas hacia una cuenta válida para evitar errores de cálculo en los comprobantes.
