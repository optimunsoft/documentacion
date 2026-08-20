---
title: Configurar y gestionar el Plan Único de Cuentas (PUC)
description: Carga inicial del PUC, reglas del árbol jerárquico por longitud de código, inactivación de cuentas, obligatoriedad de tercero y centro de costo, traslado de saldos y exportación a Excel.
module: contabilidad
category: primeros-pasos
slug: configurar-puc
order: 3
tags:
  - puc
  - plan-unico-de-cuentas
  - plan-de-cuentas
  - configuracion
  - contabilidad
  - ano-fiscal
  - contexto-contable
  - arbol-de-cuentas
  - cuenta-auxiliar
  - naturaleza-contable
  - debito
  - credito
  - inactivar-cuenta
  - tercero
  - centro-de-costo
  - eliminar-cuenta
  - mover-saldos
  - especiales
  - exportar-excel
  - optimun
  - primeros-pasos
draft: false
rag_exclude: false
last_updated: 2026-08-20
---

# Configurar y gestionar el Plan Único de Cuentas (PUC)

El Plan Único de Cuentas (PUC) es el catálogo de cuentas contables que utiliza una empresa en Zoe para registrar sus movimientos. Cada línea de un comprobante contable se registra contra una cuenta del PUC. Este documento explica dónde está la pantalla, cómo se carga el PUC por primera vez, qué reglas de negocio gobiernan el árbol de cuentas, cómo se inactiva una cuenta, cómo se exige tercero o centro de costo, qué hacer cuando una cuenta no se puede eliminar y cómo exportar el plan a Excel.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Concepto: qué es el PUC en Zoe](#concepto-qué-es-el-puc-en-zoe)
4. [Contexto por año fiscal](#contexto-por-año-fiscal)
5. [Estado inicial de una empresa nueva](#estado-inicial-de-una-empresa-nueva)
6. [Carga inicial del PUC](#carga-inicial-del-puc)
7. [Estructura del árbol jerárquico](#estructura-del-árbol-jerárquico)
8. [Reglas de negocio según la longitud del código](#reglas-de-negocio-según-la-longitud-del-código)
9. [Crear una cuenta](#crear-una-cuenta)
10. [Editar una cuenta](#editar-una-cuenta)
11. [Inactivar una cuenta](#inactivar-una-cuenta)
12. [Exigir tercero o centro de costo](#exigir-tercero-o-centro-de-costo)
13. [Exportar el PUC a Excel](#exportar-el-puc-a-excel)
14. [Solución de problemas](#solución-de-problemas)
15. [Procedimiento: mover saldos de una cuenta a otra cuenta](#procedimiento-mover-saldos-de-una-cuenta-a-otra-cuenta)
16. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
17. [Preguntas frecuentes](#preguntas-frecuentes)

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > PUC`.
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / PUC`.
- **Título de la pantalla:** «Plan Único de Cuentas».
- **Subtítulo de la pantalla:** «Configura y gestiona el plan de cuentas de tu empresa».

Elementos visibles en la parte superior de la pantalla:

| Elemento | Posición | Función |
| --- | --- | --- |
| Campo **Consultar** | Superior izquierda | Caja de búsqueda de texto libre. Permite localizar una cuenta escribiendo su código o su nombre, sin desplegar el árbol manualmente. |
| Botón **Descargar** | Superior derecha | Genera un archivo de Excel con el plan de cuentas completo del año fiscal activo. Su texto de ayuda emergente es «Descargar plan de cuentas en Excel». |
| Árbol de cuentas | Cuerpo de la pantalla | Lista jerárquica y desplegable de todas las cuentas del PUC del año fiscal activo. |

## Requisitos previos

- Tener una empresa creada y seleccionada en Zoe.
- Tener acceso al módulo de Contabilidad.
- Saber en qué año fiscal se está trabajando, porque el PUC que se muestra y se edita pertenece a ese año.
- Si la empresa proviene del software de escritorio Optimun y se desea conservar su plan de cuentas, contactar a Soporte Técnico **antes** de cargar cualquier plan en esta pantalla.

## Concepto: qué es el PUC en Zoe

El PUC es la lista de cuentas contables con la que la empresa clasifica todos sus movimientos: ventas, compras, gastos, bancos, impuestos, nómina y demás. Es un catálogo jerárquico: las cuentas se organizan en niveles, desde las clases generales (un dígito) hasta las cuentas auxiliares (seis dígitos o más), que son las que reciben los movimientos en los comprobantes.

Configurar bien el PUC desde el inicio evita reprocesos, porque una vez que las cuentas tienen movimientos registrados ya no se pueden eliminar libremente (ver [Solución de problemas](#solución-de-problemas)).

## Contexto por año fiscal

La contabilidad en Zoe funciona por **contextos anuales**. Una parte de la información pertenece al año fiscal en el que el usuario está ubicado y otra parte es global para toda la empresa. El PUC pertenece al año fiscal: si el usuario cambia de año fiscal, cambia el plan de cuentas que ve y edita.

| Información | Alcance | Comportamiento |
| --- | --- | --- |
| PUC (Plan Único de Cuentas) | Por año fiscal | Cada año fiscal tiene su propio PUC. |
| Tipos de documento | Por año fiscal | Cada año fiscal tiene su propia tabla de tipos de documento. |
| Anexos | Por año fiscal | Dependen del año fiscal seleccionado. |
| Comprobantes | Por año fiscal | Los comprobantes pertenecen al año en el que se registran. |
| Exógena | Por año fiscal | La información exógena corresponde a un año fiscal específico. |
| Centros de costo | Global | No dependen del año fiscal. Se crean una vez y quedan disponibles para todos los años. |
| Terceros | Global | No dependen del año fiscal. Se crean una vez y quedan disponibles para todos los años. |

**Consecuencia práctica:** cuando se abre un año fiscal nuevo, ese año inicia **sin PUC**. El plan de cuentas del año anterior no se hereda de forma automática; hay que copiarlo con la opción **Cargar Puc Año Anterior** descrita más abajo. En cambio, los terceros y los centros de costo ya creados siguen disponibles y no deben volverse a cargar.

**Creación de años fiscales:** al crear una empresa, Zoe crea automáticamente el año fiscal actual. Para trabajar en un año fiscal distinto, este debe crearse primero desde `Contabilidad > Configuración > Especiales > Agregar año fiscal`; después se carga el PUC de ese año desde `Contabilidad > Configuración > PUC`.

## Estado inicial de una empresa nueva

Al crear una empresa nueva en Zoe:

- La única tabla que se precarga automáticamente es la de **Tipos de documento**.
- El **PUC nace completamente vacío**. No trae ninguna cuenta.
- El usuario debe cargar el plan de cuentas de forma explícita, eligiendo una de las dos opciones de la siguiente sección.

## Carga inicial del PUC

Cuando el usuario entra a `Contabilidad > Configuración > PUC` y el año fiscal activo todavía no tiene plan de cuentas, la pantalla muestra el mensaje:

> «Actualmente no tienes un plan único de cuentas configurado, puedes elegir una de las siguientes opciones para cargarlo»

Debajo del mensaje aparecen dos tarjetas, que corresponden a las dos únicas formas de cargar el PUC inicial.

### Opción 1: cargar un plan de cuentas genérico (plan predeterminado)

Carga una plantilla base que el sistema tiene preparada. Es la opción indicada cuando la empresa empieza desde cero y no necesita conservar un plan de cuentas anterior.

**Elementos de la tarjeta:**

| Elemento | Tipo | Descripción |
| --- | --- | --- |
| **Cargar un PUC predeterminado** | Título de la tarjeta | Identifica la opción. |
| **Tipo** | Lista desplegable | Selecciona la plantilla base que se va a cargar (por ejemplo, **Comercial**). |
| **Cargar PUC** | Botón de confirmación | Ejecuta la carga del plan seleccionado en el año fiscal activo. |

**Pasos:**

1. Ubicar la tarjeta **Cargar un PUC predeterminado**.
2. En el campo **Tipo**, seleccionar la plantilla que corresponda a la empresa (por ejemplo, **Comercial**).
3. Seleccionar el botón **Cargar PUC**.

Resultado: el árbol de cuentas queda cargado con la estructura de la plantilla y la pantalla deja de mostrar el mensaje de PUC no configurado.

### Opción 2: cargar desde una empresa y un año existentes

Copia el plan de cuentas de otra empresa o de otro año fiscal ya registrado en la misma cuenta de Zoe. Cubre dos casos de uso frecuentes:

- **Contador con varias empresas:** configura el PUC una sola vez y lo replica en las demás empresas que administra.
- **Apertura de un año fiscal nuevo:** copia el PUC del año anterior de la misma empresa hacia el año nuevo, conservando la misma estructura de cuentas.

**Elementos de la tarjeta:**

| Elemento | Tipo | Descripción |
| --- | --- | --- |
| **Cargar Puc Año Anterior** | Título de la tarjeta | Identifica la opción. |
| **Empresa** | Lista desplegable | Empresa de origen desde la cual se copiará el plan de cuentas. |
| **Año** | Lista desplegable | Año fiscal de origen desde el cual se copiará el plan de cuentas. |
| **Copiar PUC** | Botón de confirmación | Ejecuta la copia hacia la empresa y el año fiscal activos. |

**Pasos:**

1. Ubicar la tarjeta **Cargar Puc Año Anterior**.
2. En el campo **Empresa**, seleccionar la empresa de origen.
3. En el campo **Año**, seleccionar el año fiscal de origen.
4. Seleccionar el botón **Copiar PUC**.

**Restricción:** si en la cuenta no existe ninguna empresa con un año fiscal previo que tenga PUC, los campos de esta tarjeta aparecen deshabilitados, porque no hay origen del cual copiar. En ese caso debe usarse la Opción 1.

### Caso especial: empresas que vienen de Optimun de escritorio

La pantalla `Contabilidad > Configuración > PUC` **no importa** planes de cuentas del software de escritorio Optimun. El traslado de esa información hace parte del proceso de **migración asistida** que ejecuta el equipo de Soporte Técnico.

Procedimiento correcto: contactar a Soporte Técnico **antes** de cargar un plan predeterminado. Si se carga un plan genérico primero, ese trabajo deberá deshacerse antes de la migración.

## Estructura del árbol jerárquico

Con el plan cargado, la pantalla muestra el PUC como un árbol desplegable. El comportamiento de la interfaz es el siguiente:

- Cada fila del árbol corresponde a una cuenta y se muestra con el formato `código - nombre` (por ejemplo, `1105 - Caja`).
- La **flecha** ubicada al extremo derecho de la fila expande o contrae esa rama para mostrar u ocultar sus cuentas hijas.
- **Un clic directo sobre la cuenta** (sobre el texto de la fila) abre la ventana de creación o edición de cuentas. Esa es la forma de gestionar las cuentas del PUC: no existe un menú aparte.
- Las cuentas marcadas como auxiliares muestran la etiqueta **Aux** a la izquierda de su código.
- El campo **Consultar** de la parte superior permite localizar una cuenta escribiendo su código o su nombre, sin recorrer el árbol.

### Ejemplo numérico de la jerarquía

Estructura de la rama del activo disponible, desde el nivel más alto hasta las cuentas auxiliares:

| Código | Nombre | Dígitos | Nivel | Etiqueta Aux |
| --- | --- | --- | --- | --- |
| `1` | Activo | 1 | Clase | No |
| `11` | Disponible | 2 | Grupo | No |
| `1105` | Caja | 4 | Cuenta | No |
| `110505` | Caja general | 6 | Auxiliar | Sí |
| `110510` | Cajas menor | 6 | Auxiliar | Sí |
| `110515` | Caja moneda extranjera | 6 | Auxiliar | Sí |
| `1110` | Bancos | 4 | Cuenta | No |
| `111005` | Moneda nacional | 6 | Subcuenta | No |

Otros grupos que cuelgan de la clase `1 - Activo`: `12 - Inversiones`, `13 - Deudores`, `14 - Inventarios`, `15 - Propiedades planta y equipo`, `16 - Intangibles`, `17 - Diferidos`, `18 - Otros activos`, `19 - Valorizaciones`. Al mismo nivel de `1 - Activo` están las demás clases del plan: `2 - Pasivo`, `3 - Patrimonio`, `4 - Ingresos`, y las siguientes según la plantilla cargada.

## Reglas de negocio según la longitud del código

Lo que el usuario puede hacer sobre una cuenta depende de **cuántos dígitos tiene su código**.

| Longitud del código | Ejemplo | Crear cuentas hijas | Eliminar la cuenta | Editar |
| --- | --- | --- | --- | --- |
| 1 dígito (clase) | `1 - Activo` | No | No | **No editable.** Corresponde a la estructura del plan cargado. |
| 2 dígitos (grupo) | `11 - Disponible` | No | No | **No editable.** Corresponde a la estructura del plan cargado. |
| 4 dígitos (cuenta) | `1105 - Caja` | No | No | **Solo nombre y naturaleza (Débito o Crédito).** |
| 6 dígitos o más | `110515 - Caja moneda extranjera` | **Sí** | **Sí**, si no tiene saldos asociados | Todos los campos de la cuenta. |

Reglas complementarias:

- **Regla de los 4 dígitos:** en una cuenta de 4 dígitos solo se permite modificar su **nombre** y su **naturaleza**. No se pueden crear ni eliminar cuentas en ese nivel, porque corresponde a la estructura oficial del plan.
- **Regla de los 6 dígitos:** la creación y la eliminación de cuentas solo está permitida de 6 dígitos en adelante.
- **Regla de jerarquía:** solo las cuentas que **no son auxiliares** pueden tener cuentas hijas. Una cuenta marcada como auxiliar (etiqueta **Aux**) es el último nivel de su rama: recibe movimientos contables, pero no admite cuentas por debajo.

## Crear una cuenta

Para crear una cuenta se hace **clic directo sobre la cuenta que será la cuenta padre** dentro del árbol. Se abre la ventana **Nueva cuenta**, cuyo subtítulo es «Agrega una nueva cuenta al plan único de cuentas».

### Campos de la ventana Nueva cuenta

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Código** | Texto con prefijo fijo | Sí | Se compone de dos partes: el prefijo de la cuenta padre, que el sistema muestra fijo y no editable, y los dígitos finales, que escribe el usuario. |
| **Nombre** | Texto | Sí | Nombre con el que la cuenta aparecerá en el árbol, en los comprobantes y en los reportes. |
| **Naturaleza** | Lista desplegable | Sí | Valores posibles: **Débito** o **Crédito**. Define de qué lado suma la cuenta. |
| **Solicitar** | Lista desplegable de selección única | No | **Solo se muestra cuando la casilla ¿Es auxiliar? está marcada.** Define qué dato adicional exigirá el comprobante al usar esta cuenta. Valores posibles: **Tercero** o **Centro de costo**. No permite seleccionar los dos valores al mismo tiempo. |
| **¿Es auxiliar?** | Casilla de verificación | No | Etiquetada «Marca si es auxiliar (Cuenta auxiliar)». Si se marca, la cuenta queda como último nivel: recibe movimientos y no admite cuentas hijas. |
| **¿Cuenta activa?** | Casilla de verificación | No | Etiquetada «Marca si es activa (Cuenta en uso)». Si se marca, la cuenta está disponible para usarse. Si se desmarca, la cuenta queda inactiva. |

Botones de la ventana: **Cancelar**, que cierra sin guardar, y **Crear**, que guarda la cuenta.

### Ejemplo numérico completo

Creación de una cuenta auxiliar de caja en moneda extranjera bajo la cuenta `1105 - Caja`:

1. En el árbol, hacer clic sobre la cuenta `1105 - Caja`. Se abre la ventana **Nueva cuenta**.
2. En **Código**, el sistema muestra fijo el prefijo `1105`. El usuario escribe `15` en la parte editable. El código resultante es `110515`.
3. En **Nombre**, escribir `Caja Moneda Extranjera`.
4. En **Naturaleza**, seleccionar `Débito`.
5. En **Solicitar**, seleccionar `Tercero`.
6. Marcar la casilla **¿Es auxiliar?**.
7. Marcar la casilla **¿Cuenta activa?**.
8. Seleccionar el botón **Crear**.

Resultado: la cuenta `110515 - Caja moneda extranjera` aparece en el árbol con la etiqueta **Aux**, ubicada debajo de `1105 - Caja` y al mismo nivel de `110505 - Caja general` y `110510 - Cajas menor`. Queda disponible para usarse en los comprobantes del año fiscal activo y exigirá tercero al registrarse.

## Editar una cuenta

Para editar una cuenta existente se hace **clic directo sobre esa cuenta** en el árbol. Se abre la misma ventana descrita arriba, con la información actual de la cuenta cargada en los campos.

Restricción por nivel: en una cuenta de **4 dígitos** únicamente se pueden modificar el **Nombre** y la **Naturaleza**. En cuentas de **6 dígitos o más** se pueden modificar todos los campos.

## Inactivar una cuenta

Inactivar es la alternativa a eliminar cuando la cuenta ya no debe usarse pero no puede borrarse, por ejemplo porque tiene movimientos históricos.

**Procedimiento:** abrir la cuenta con un clic sobre ella en el árbol y **desmarcar la casilla ¿Cuenta activa?**.

**Efectos de inactivar una cuenta:**

- Impide registrar **nuevos asientos contables** con esa cuenta.
- **Oculta la cuenta en las búsquedas**, de modo que no aparece como opción al construir un comprobante.
- **No borra la información existente:** los movimientos ya registrados con esa cuenta se conservan y siguen apareciendo en los reportes del período.

**Reversibilidad:** la operación se deshace volviendo a marcar la casilla **¿Cuenta activa?**, con lo cual la cuenta vuelve a estar disponible.

## Exigir tercero o centro de costo

El campo **Solicitar** de la ventana de la cuenta determina qué información adicional se exigirá al usar esa cuenta en un comprobante.

**Condición de visibilidad:** el campo **Solicitar** únicamente se muestra en la ventana cuando la casilla **¿Es auxiliar?** está marcada. Si la cuenta no es auxiliar, el campo se oculta, porque las cuentas auxiliares son las que reciben los movimientos contables.

**Tipo de selección:** es una lista desplegable de **selección única**. En la interfaz actual se elige **Tercero** o **Centro de costo**, no ambos valores simultáneamente.

**Regla de negocio:** si la cuenta tiene activada la marca de **Tercero** o de **Centro de costo**, el comprobante **exigirá obligatoriamente** ese dato. La línea del comprobante no se puede guardar sin diligenciarlo.

| Valor de Solicitar | Efecto en el comprobante | Cuándo se usa |
| --- | --- | --- |
| **Tercero** | El comprobante obliga a indicar el tercero asociado al movimiento. | Cuentas donde se necesita identificar con quién se hizo la operación: clientes, proveedores, empleados, impuestos. Permite obtener después el detalle por tercero. |
| **Centro de costo** | El comprobante obliga a indicar el centro de costo asociado al movimiento. | Cuentas de gasto o de ingreso cuyo valor debe distribuirse por sede, proyecto, área o línea de negocio. |

**Relación con el año fiscal:** los terceros y los centros de costo son datos **globales** y no dependen del año fiscal. La marca configurada en el campo **Solicitar**, en cambio, vive dentro de la cuenta del PUC, y el PUC sí pertenece a un año fiscal específico. Es decir, esa marca debe revisarse en cada año fiscal cuyo PUC se cargue o se copie.

## Exportar el PUC a Excel

El botón **Descargar**, ubicado en la parte superior derecha de la pantalla del PUC, genera un archivo de Excel con el plan de cuentas completo del año fiscal activo. Su texto de ayuda emergente es «Descargar plan de cuentas en Excel».

Es una herramienta complementaria de revisión: permite ver el PUC completo de forma masiva, en una sola lista, sin necesidad de desplegar el árbol rama por rama.

Usos habituales de la exportación:

- Revisar el plan de cuentas completo de una sola vez.
- Detectar cuentas duplicadas, nombres incorrectos o códigos que no corresponden.
- Compartir el plan de cuentas con el contador o con el equipo antes de iniciar los registros.
- Comparar el PUC de un año fiscal contra el de otro año fiscal.

## Solución de problemas

### No se puede eliminar una cuenta

Existen dos causas posibles:

1. **La cuenta tiene saldos o movimientos asociados.** El sistema **no permite eliminar cuentas con saldos asociados**, porque hacerlo dejaría comprobantes y reportes referenciando una cuenta inexistente. Solución: trasladar el saldo a otra cuenta con el procedimiento de la sección [Mover saldos de una cuenta a otra cuenta](#procedimiento-mover-saldos-de-una-cuenta-a-otra-cuenta), o inactivar la cuenta.
2. **La cuenta es de 4 dígitos o menos.** En ese nivel la eliminación no está permitida por regla de negocio. Solo se pueden modificar el nombre y la naturaleza.

Si el objetivo es únicamente dejar de usar la cuenta y no reorganizar el plan, la solución correcta es [inactivarla](#inactivar-una-cuenta), no eliminarla.

### El PUC aparece vacío al entrar a un año fiscal nuevo

Es el comportamiento esperado: el PUC pertenece al año fiscal y no se hereda automáticamente. Solución: usar la tarjeta **Cargar Puc Año Anterior**, seleccionar la misma empresa y el año fiscal anterior, y ejecutar **Copiar PUC**.

### Los campos de Cargar Puc Año Anterior están deshabilitados

No existe ninguna empresa con un año fiscal previo del cual copiar el plan. Ocurre típicamente en la primera empresa creada en la cuenta. Solución: usar la tarjeta **Cargar un PUC predeterminado**.

### No se puede crear una cuenta debajo de la cuenta seleccionada

Dos causas posibles:

1. La cuenta seleccionada está marcada como **auxiliar** (etiqueta **Aux**). Solo las cuentas que no son auxiliares admiten cuentas hijas. Solución: crear la cuenta nueva a partir de la cuenta padre correspondiente.
2. La cuenta seleccionada es de 4 dígitos o menos. La creación solo está permitida de 6 dígitos en adelante.

### Un comprobante exige tercero o centro de costo

La cuenta utilizada tiene activada la marca correspondiente en el campo **Solicitar**. Solución: diligenciar el dato solicitado o, si esa exigencia no corresponde para la cuenta, abrirla en el PUC y modificar el campo **Solicitar**.

### No se encuentra una cuenta que sí fue creada

Verificar dos condiciones:

1. Que se esté trabajando en el **año fiscal correcto**, porque el PUC pertenece a un año fiscal específico.
2. Que la cuenta **no esté inactiva**, porque las cuentas inactivas se ocultan en las búsquedas.

### No aparece la opción PUC en el menú

Verificar que haya una empresa seleccionada y que el usuario tenga acceso al módulo de Contabilidad.

### No se encuentra cómo cargar el PUC de Optimun

La pantalla del PUC no importa planes de cuentas de Optimun de escritorio. Ese traslado hace parte de la migración asistida. Solución: contactar a Soporte Técnico antes de cargar un plan predeterminado.

## Procedimiento: mover saldos de una cuenta a otra cuenta

Este es el procedimiento oficial para ajustar un PUC que ya tiene saldos activos, es decir, cuando la cuenta que se quiere eliminar o reorganizar tiene movimientos registrados.

**Ruta de la herramienta:** `Contabilidad > Especiales > Mover saldos de una cuenta a otra cuenta`.

**Pasos:**

1. **Crear la cuenta destino.** En `Contabilidad > Configuración > PUC`, crear la cuenta auxiliar que recibirá el saldo. Debe ser una cuenta de **6 dígitos o más**, porque es el único nivel donde se permite crear cuentas. Si el movimiento es transitorio, esta cuenta se crea como cuenta auxiliar temporal.
2. **Abrir la herramienta de traslado.** Ir a `Contabilidad > Especiales > Mover saldos de una cuenta a otra cuenta`.
3. **Seleccionar la cuenta de origen y la cuenta de destino.** La cuenta de origen es la que tiene el saldo actual; la cuenta de destino es la creada en el paso 1.
4. **Confirmar el traslado** y esperar a que el proceso finalice.
5. **Verificar el resultado.** Volver al PUC o generar un reporte de saldos y comprobar que la cuenta de origen quedó en cero y que el valor quedó registrado en la cuenta de destino.
6. **Cerrar el ciclo.** Con la cuenta de origen ya sin saldo, eliminarla, si es de 6 dígitos o más, o inactivarla desmarcando la casilla **¿Cuenta activa?**.

**Advertencia:** este procedimiento modifica saldos contables reales. Debe ejecutarse en un momento en el que no se estén registrando comprobantes y verificarse antes de continuar. Ante cualquier duda, consultar con Soporte Técnico antes de ejecutarlo.

## Resumen de reglas de negocio

| # | Regla |
| --- | --- |
| 1 | El PUC pertenece al año fiscal. También dependen del año fiscal los tipos de documento, los anexos, los comprobantes y la exógena. |
| 2 | Los centros de costo y los terceros son globales y no dependen del año fiscal. |
| 3 | Al crear una empresa nueva solo se precarga la tabla de tipos de documento. El PUC nace vacío. |
| 4 | El PUC vacío se carga de dos formas: con un plan de cuentas genérico del sistema, o copiándolo desde una empresa y un año existentes. |
| 5 | En cuentas de 4 dígitos solo se permite modificar el nombre y la naturaleza (Débito o Crédito). |
| 6 | La creación y la eliminación de cuentas solo se permite de 6 dígitos en adelante. |
| 7 | Solo las cuentas que no son auxiliares pueden tener cuentas hijas. |
| 8 | Inactivar una cuenta impide registrar nuevos asientos con ella y la oculta en las búsquedas, sin borrar los movimientos históricos. |
| 9 | Si la cuenta tiene la marca de tercero o de centro de costo, el comprobante exigirá obligatoriamente ese dato. |
| 10 | No se pueden eliminar cuentas con saldos asociados. |
| 11 | Para ajustar un PUC con saldos activos se crea una cuenta auxiliar temporal y se traslada el saldo mediante `Contabilidad > Especiales > Mover saldos de una cuenta a otra cuenta`. |
| 12 | La exportación a Excel permite revisar el PUC completo de forma masiva sin desplegar el árbol. |
| 13 | La gestión de cuentas en el árbol se hace con un clic directo sobre la cuenta, que abre la ventana de creación o edición. |
| 14 | El campo **Solicitar** solo se muestra cuando la cuenta está marcada como auxiliar, y es de selección única: Tercero o Centro de costo. |

## Preguntas frecuentes

**¿El PUC se copia solo al año siguiente?**
No. Cada año fiscal tiene su propio PUC y el año nuevo inicia vacío. Debe copiarse con la opción **Cargar Puc Año Anterior**, seleccionando la misma empresa y el año anterior.

**¿Hay que volver a crear los terceros y los centros de costo cada año?**
No. Los terceros y los centros de costo son globales de la empresa y no dependen del año fiscal.

**¿Por qué el PUC está vacío en una empresa recién creada?**
Porque al crear una empresa solo se precarga la tabla de tipos de documento. El PUC se carga manualmente con una de las dos opciones disponibles.

**¿Se puede crear una cuenta de 4 dígitos?**
No. Las cuentas se crean de 6 dígitos en adelante. En las de 4 dígitos solo se editan el nombre y la naturaleza.

**¿Se puede agregar una cuenta debajo de una cuenta auxiliar?**
No. Una cuenta marcada como auxiliar es el último nivel de su rama y no admite cuentas hijas.

**¿Cuál es la diferencia entre eliminar e inactivar una cuenta?**
Eliminar borra la cuenta del plan y solo es posible en cuentas de 6 dígitos o más que no tengan saldos asociados. Inactivar conserva la cuenta y su historial, pero impide registrar nuevos asientos con ella y la oculta en las búsquedas.

**¿Cómo se elimina una cuenta que tiene saldo?**
No se puede eliminar directamente. Primero hay que trasladar el saldo a otra cuenta mediante `Contabilidad > Especiales > Mover saldos de una cuenta a otra cuenta` y después eliminar o inactivar la cuenta de origen.

**¿Por qué no aparece el campo Solicitar en la ventana de la cuenta?**
Porque la casilla **¿Es auxiliar?** no está marcada. El campo **Solicitar** solo se muestra en cuentas auxiliares.

**¿Se puede exigir tercero y centro de costo en la misma cuenta?**
No con la interfaz actual: el campo **Solicitar** es de selección única y admite **Tercero** o **Centro de costo**.

**¿Cómo se revisa el PUC completo sin desplegar el árbol?**
Con el botón **Descargar** de la parte superior derecha de la pantalla, que exporta el plan de cuentas completo a Excel.

**¿Se puede cargar en Zoe el plan de cuentas de Optimun de escritorio?**
No desde esta pantalla. Ese traslado hace parte de la migración asistida que gestiona Soporte Técnico y debe coordinarse antes de cargar cualquier plan predeterminado.

## Artículos relacionados

- [Primeros pasos con Contabilidad](./primeros-pasos.md)
- [Cómo crear tu primera empresa (demo)](./crear-primera-empresa.md)
- [Cómo hacer tu primer asiento contable](./primer-asiento-contable.md)
- [Cómo generar reportes básicos](./reportes-basicos.md)
