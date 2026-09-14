---
title: Años fiscales y periodos contables
description: Gestión del año fiscal y de los periodos contables mensuales en el módulo de Contabilidad. Cubre el concepto de año fiscal como contenedor del trabajo contable, la inicialización automática del año al crear una empresa, el cambio del año fiscal activo desde el sidebar y con el atajo Alt+A, la habilitación y el retiro de años fiscales desde Configuración > Especiales, la ventana Periodos Contables con la apertura y el cierre de meses y del año completo, el aviso de año fiscal cerrado, la trazabilidad del cierre en la fila de cada mes, el historial de aperturas y cierres, las validaciones de fecha y de periodo al registrar comprobantes y el bloqueo de la edición de comprobantes existentes en periodos cerrados, el alcance anual del PUC, los centros de costo, los anexos, los tipos de documento y los reportes, el ciclo completo de inicio de un año nuevo con el traslado de saldos, y las herramientas complementarias del panel Comprobantes de Acciones Especiales.
module: contabilidad
category: configuracion
slug: anio-fiscal-periodos
order: 9
tags:
  - configuracion
  - acciones-especiales
  - ano-fiscal
  - anio-fiscal
  - periodo-contable
  - periodos-contables
  - agregar-ano-fiscal
  - quitar-ano-fiscal
  - gestionar-periodos-contables
  - abrir-periodo
  - cerrar-periodo
  - cierre-mensual
  - cierre-anual
  - apertura-de-periodo
  - historial-de-periodos
  - ano-fiscal-activo
  - alt-a
  - saldos-iniciales
  - mover-saldos-finales-a-iniciales
  - activar-desactivar-edicion-de-comprobante
  - mover-saldos-entre-cuentas
  - auditoria-de-operacion
  - fijar-mes
  - cierre-de-ano
  - tipo-de-documento-ca
  - ano-fiscal-origen
  - ano-fiscal-destino
  - periodo-abierto
  - periodo-cerrado
  - comprobantes
  - puc
  - centros-de-costo
  - tipos-de-documento
  - anexos
  - reportes-contables
  - trazabilidad
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-14
---

# Años fiscales y periodos contables

La contabilidad en Zoe está organizada por años y, dentro de cada año, por meses. El **año fiscal** es el contenedor de todo el trabajo contable de un año determinado, y el **periodo contable** es cada uno de sus doce meses, que se abre o se cierra de forma independiente. De esa organización dependen cosas que el usuario percibe a diario: qué información ve en pantalla, en qué fechas puede grabar un comprobante y qué queda protegido de modificaciones. Este documento explica cómo se inicializa el año fiscal al crear una empresa, cómo se cambia el año de trabajo, cómo se habilitan y se retiran años, cómo se abren y se cierran los meses y el año completo, cómo se consulta el historial de esos cambios, qué validaciones aplican al registrar comprobantes y cuál es el ciclo completo cuando se inicia un año nuevo.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Conceptos: año fiscal y periodo contable](#conceptos-año-fiscal-y-periodo-contable)
4. [Distinciones que evitan errores](#distinciones-que-evitan-errores)
5. [Inicialización al crear una empresa](#inicialización-al-crear-una-empresa)
6. [El año fiscal activo](#el-año-fiscal-activo)
7. [Elementos de la pantalla Acciones Especiales](#elementos-de-la-pantalla-acciones-especiales)
8. [Agregar un año fiscal](#agregar-un-año-fiscal)
9. [Quitar un año fiscal](#quitar-un-año-fiscal)
10. [Gestionar periodos contables](#gestionar-periodos-contables)
11. [Historial de aperturas y cierres](#historial-de-aperturas-y-cierres)
12. [Validaciones al registrar un comprobante](#validaciones-al-registrar-un-comprobante)
13. [Alcance anual de la información](#alcance-anual-de-la-información)
14. [Ciclo de inicio de un año nuevo](#ciclo-de-inicio-de-un-año-nuevo)
15. [Herramientas complementarias del panel Comprobantes](#herramientas-complementarias-del-panel-comprobantes)
16. [Solución de problemas](#solución-de-problemas)
17. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
18. [Preguntas frecuentes](#preguntas-frecuentes)

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Especiales`.
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / ESPECIALES`.
- **Título de la pantalla:** «Acciones Especiales».
- **Subtítulo de la pantalla:** «Gestiona periodos fiscales, saldos iniciales y procesos de cierre contable, además de otras opciones que sólo encontrarás aquí».
- **Contenido de la pantalla:** tres paneles, **Periodos**, **Comprobantes** y **Terceros**. Cada opción dispone de un ícono de información que despliega un aviso con el efecto de la acción.

**Rutas complementarias:**

| Proceso | Ruta |
| --- | --- |
| Agregar un año fiscal | `Contabilidad > Configuración > Especiales > Periodos > Años fiscales > Agregar año fiscal` |
| Quitar un año fiscal | `Contabilidad > Configuración > Especiales > Periodos > Años fiscales > Quitar año fiscal` |
| Abrir o cerrar meses y el año | `Contabilidad > Configuración > Especiales > Periodos > Periodos contables > Gestionar periodos contables` |
| Consultar el historial de aperturas y cierres | `Contabilidad > Configuración > Especiales > Periodos > Historial` |
| Cambiar el año fiscal activo | Contenedor azul del año en el sidebar del menú Contabilidad, o atajo `Alt + A` |
| Trasladar saldos entre años | `Contabilidad > Configuración > Especiales > Comprobantes > Mover Saldos Finales a Iniciales` |
| Ejecutar el cierre contable del ejercicio | `Contabilidad > Configuración > Especiales > Comprobantes > Cierre anual` |

## Requisitos previos

- Tener una empresa creada y seleccionada en Zoe.
- Contar con acceso al módulo de Contabilidad.
- Conocer el año fiscal en el que se está trabajando, visible en el contenedor azul del sidebar junto a la palabra «Contabilidad».

## Conceptos: año fiscal y periodo contable

**Año fiscal:** es el contenedor del trabajo contable de un año determinado. Dentro de él viven el PUC, los asientos y comprobantes, los anexos, los tipos de documento y los reportes de ese año. Cada año fiscal tiene su propio contenido, y la información de uno no es visible desde otro.

**Periodo contable:** es cada mes del año fiscal, de enero a diciembre. Cada mes se abre o se cierra de forma independiente del resto, de modo que una empresa puede tener enero y febrero cerrados y marzo abierto recibiendo movimientos. Cerrar un periodo es la manera de dejar en firme lo ya conciliado.

**Año fiscal activo:** es el año con el que se está trabajando en la sesión. Se identifica en el contenedor azul del sidebar del menú Contabilidad. Cambiarlo cambia el contexto completo de la contabilidad: el PUC, los asientos y los reportes pasan a ser los del año seleccionado.

**Relación entre ambos:** el año fiscal es el contenedor y los periodos contables son sus doce divisiones. El estado del año condiciona el de los meses, pero no al revés: un año abierto puede tener meses abiertos y cerrados a la vez, mientras que un año cerrado inmoviliza todos sus meses.

## Distinciones que evitan errores

Tres confusiones habituales conviene resolverlas antes de operar:

| Se confunde | Realidad |
| --- | --- |
| Quitar un año fiscal **borra** la información del año | **No la borra.** El año deja de estar disponible en la lista de trabajo, pero la información grabada se conserva. El propio aviso de la opción lo advierte. |
| Bloquear la edición de comprobantes **es** cerrar un periodo | **Son controles distintos.** Cerrar un periodo impide registrar movimientos con fecha de ese mes. Bloquear la edición impide modificar comprobantes concretos, con el periodo abierto o cerrado. |
| Cerrar el año fiscal **es** el cierre anual contable | **Son procesos distintos.** Cerrar el año fiscal en *Gestionar periodos contables* bloquea el registro de movimientos. El **Cierre anual** del panel Comprobantes es el proceso contable de cierre del ejercicio. |

## Inicialización al crear una empresa

**El año fiscal viene precargado.** Al crear una empresa nueva, la plataforma deja habilitado el **año actual** de forma predeterminada. No existe un paso de configuración inicial que el usuario deba ejecutar para empezar a trabajar.

**Comportamiento al entrar a Contabilidad:** ese año queda seleccionado en el contenedor azul del sidebar, y el PUC, los asientos y los reportes arrancan sobre él.

**Qué sí requiere acción manual:** habilitar años distintos del actual. Si la empresa necesita trabajar un año anterior —por ejemplo durante una migración de información— o el año siguiente, ese año debe agregarse desde Acciones Especiales y después seleccionarse como año activo.

## El año fiscal activo

### Dónde se ve

En el **contenedor azul del sidebar**, junto a la palabra «Contabilidad». Muestra siempre el año con el que se está trabajando.

### Cómo se cambia

| Vía | Detalle |
| --- | --- |
| Contenedor del sidebar | Al pulsarlo abre la ventana **Configuración de año fiscal**. |
| Atajo de teclado | `Alt + A` abre la misma ventana. |

**Campos de la ventana Configuración de año fiscal:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Año** | Lista desplegable | Sí | Lista únicamente los años fiscales habilitados en la empresa. El año activo aparece con una marca de verificación. |
| **Cancelar** | Botón | — | Cierra la ventana sin cambiar el año. |
| **Guardar** | Botón | — | Aplica el cambio de año activo. |

**Efecto del cambio:** al guardar, el contenedor del sidebar pasa a mostrar el año seleccionado y toda la contabilidad cambia de contexto. Las pantallas de PUC, comprobantes, anexos y reportes muestran a partir de ese momento la información del año nuevo.

**Si el año buscado no aparece en el desplegable:** no está habilitado en la empresa. Debe agregarse primero desde Acciones Especiales.

### Fijación del mes de trabajo

El año se selecciona desde el sidebar, pero **el mes se fija dentro del propio formulario del comprobante**, no en la ventana Configuración de año fiscal.

**Ubicación:** campo **Fijar mes**, primer campo del formulario del asiento, a la izquierda de **Fecha**. Es una lista desplegable con los meses del año y lleva debajo un ícono de información.

**Efecto:** cuando hay un mes fijado, solo se pueden registrar asientos dentro de ese periodo, lo que reduce los errores de digitación al capturar muchos movimientos consecutivos del mismo mes.

## Elementos de la pantalla Acciones Especiales

La pantalla agrupa sus opciones en tres paneles.

**Panel Periodos:**

| Grupo | Opción | Función |
| --- | --- | --- |
| Años fiscales | **Agregar año fiscal** | Habilita otro año para trabajar en él. |
| Años fiscales | **Quitar año fiscal** | Retira un año de la lista de trabajo. No elimina la información grabada. |
| Periodos contables | **Gestionar periodos contables** | Abre y cierra los meses del año y el año completo. |
| — | **Historial** | Consulta de las aperturas y los cierres realizados. |

**Panel Comprobantes:**

| Opción | Función |
| --- | --- |
| **Saldos iniciales** | Gestión de los saldos de apertura del año fiscal. |
| **Cierre anual** | Proceso contable de cierre del ejercicio. |
| **Comprobantes en proceso** | Comprobantes que aún no están contabilizados en firme. |
| **Mover Saldos Finales a Iniciales** | Traslada los saldos de cierre de un año a los saldos iniciales del siguiente. |
| **Activar/Desactivar Edición de Comprobante** | Habilita o bloquea la edición de comprobantes. No es un cierre de periodo. |
| **Mover saldos entre cuentas** | Traslada el movimiento de una cuenta del PUC a otra. |
| **Auditoría de Operación** | Consulta de las operaciones realizadas en la empresa. |

**Panel Terceros:**

| Opción | Función |
| --- | --- |
| **Actualizar documento** | Modifica el documento o NIT de un tercero. Se documenta en la guía de Terceros. |

Cada opción tiene un **ícono de información** que despliega un aviso con el efecto de la acción.

## Agregar un año fiscal

**Ruta:** `Contabilidad > Configuración > Especiales > Periodos > Años fiscales > Agregar año fiscal`.

Se abre la ventana **Agregar año fiscal**, con el subtítulo «Añade un nuevo año fiscal a tu espacio de trabajo».

**Campos de la ventana:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Año** | Lista desplegable | Sí | Año que se desea habilitar. Admite años anteriores y posteriores al actual. |
| **Cancelar** | Botón | — | Cierra la ventana sin crear el año. |
| **Agregar** | Botón | — | Habilita el año seleccionado. |

**Confirmación:** la plataforma muestra el aviso **«Operación exitosa — Año fiscal agregado correctamente»**.

**Resultado:** el año queda disponible de inmediato en el desplegable de **Configuración de año fiscal**, listo para seleccionarse como año activo.

**Regla importante: agregar el año no lo deja configurado.** La acción solo habilita el año. El año nuevo arranca **sin PUC y sin centros de costo**:

| Información | Comportamiento al habilitar un año nuevo |
| --- | --- |
| PUC | No se hereda. Se copia del año anterior desde `Configuración > PUC`, opción **Cargar Puc Año Anterior**. |
| Centros de costo | No se heredan. Deben crearse de nuevo en el año. |
| Terceros | Siguen disponibles: pertenecen a la empresa, no al año. |

## Quitar un año fiscal

**Ruta:** `Contabilidad > Configuración > Especiales > Periodos > Años fiscales > Quitar año fiscal`.

Se abre la ventana **Quitar año fiscal**, con el subtítulo «Quita un año fiscal de tu espacio de trabajo».

**Campos de la ventana:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Año** | Lista desplegable | Sí | Año que se desea retirar de la lista. |
| **Cancelar** | Botón | — | Cierra la ventana sin retirar el año. |
| **Quitar** | Botón | — | Retira el año seleccionado. |

**Confirmación:** la plataforma muestra el aviso **«Operación exitosa — Año fiscal eliminado correctamente»**. El aviso conserva la palabra «eliminado» aunque la opción del menú y la ventana usen el verbo «quitar».

**Verificación posterior:** al volver a abrir el desplegable de **Configuración de año fiscal** o el de **Quitar año fiscal**, el año retirado ya no aparece en la lista.

**Alcance real de la acción.** El aviso informativo de la opción lo declara de forma explícita: **«Ya no tendrás disponible este año fiscal. NO se eliminará la información que hayas grabado.»** Retirar un año lo saca de la lista de trabajo y del selector del sidebar; los comprobantes, el PUC y los demás datos de ese año se conservan. Si el año vuelve a agregarse más adelante, su información sigue disponible.

**Regla de negocio: no se puede quitar el año en uso.** Al intentar eliminar el año fiscal activo, la plataforma muestra el mensaje de error **«No se puede quitar el año fiscal en uso. Por favor cambiate a otro año fiscal»** y la operación no se ejecuta.

**Procedimiento correcto:**

1. Cambiar el año activo a otro año desde el contenedor del sidebar o con `Alt + A`.
2. Volver a `Especiales > Periodos > Años fiscales > Quitar año fiscal`.
3. Seleccionar el año que se desea retirar y confirmar.

**Para qué se usa:** para mantener limpio el selector de años. Sirve cuando se habilitó un año por error, o cuando se trabajaron años antiguos durante una migración y mantenerlos visibles aumenta el riesgo de que alguien registre movimientos en el año equivocado.

## Gestionar periodos contables

**Ruta:** `Contabilidad > Configuración > Especiales > Periodos > Periodos contables > Gestionar periodos contables`.

Abre la ventana **Periodos Contables**, con el subtítulo «Consulta y gestiona el estado de apertura y cierre de los periodos». Es el control del estado de los periodos.

**Selección del año.** La ventana se abre sin año seleccionado: la ficha superior muestra «Sin estado · 0 meses abiertos» y el cuerpo el texto «Selecciona un año». El desplegable **Buscar Año** lista los años fiscales habilitados, cada uno con su estado al lado.

**Regla de negocio: la ventana no está limitada al año fiscal activo.** Se puede gestionar el estado de los periodos de cualquier año habilitado sin cambiar el año de trabajo. Es la excepción a la dependencia general del año fiscal activo que rige en el resto del módulo.

**Elementos de la ventana, una vez seleccionado el año:**

| Elemento | Contenido |
| --- | --- |
| Ficha del año | El año, la etiqueta **AÑO FISCAL**, el estado (**Abierto** o **Cerrado**), el contador «N meses abiertos» y la barra **Progreso del año** con el indicador `N/12` de meses cerrados. |
| Desplegable **Buscar Año** | Cambia el año cuyos periodos se están gestionando. |
| Botón del año | **Cerrar año** cuando está abierto; **Abrir año** cuando está cerrado. |
| **Detalle de Periodos** | Encabezado con el contador «12 periodos» y la lista de los doce meses. |
| Fila de cada mes | Número de periodo (01–12), nombre del mes, etiqueta de estado **Abierto** o **Cerrado** y botón **Cerrar** o **Abrir** según corresponda. |

**Trazabilidad en la propia fila.** Cuando un mes está cerrado, su fila muestra además **«Cerrado por: [usuario]»** y **«Fecha: [aaaa-mm-dd]»**. La autoría del cierre de un mes concreto se consulta ahí mismo, sin necesidad de abrir el Historial.

**Acciones disponibles:**

| Acción | Alcance |
| --- | --- |
| **Cerrar** (mes) | Impide registrar y modificar movimientos con fecha de ese mes. |
| **Abrir** (mes) | Vuelve a habilitar el mes. |
| **Cerrar año** | Deja el año fiscal en firme y retira la gestión de sus periodos mensuales. |
| **Abrir año** | Devuelve la lista de meses, cada uno en el estado en que quedó. |

**Confirmación:** el cierre de un mes es inmediato, sin diálogo de confirmación previo. La plataforma responde con el aviso **«Operación exitosa — Mes cerrado correctamente»**. La acción es reversible con el botón **Abrir** de la misma fila.

**Independencia de los meses:** cada mes se abre y se cierra por separado. Un año fiscal puede tener simultáneamente meses cerrados y meses abiertos.

**Regla de negocio: el año condiciona los meses.** Al cerrar el año fiscal, la sección **Detalle de Periodos** deja de mostrar la lista de meses y en su lugar aparece un ícono de candado con los textos **«Año fiscal cerrado»** y **«No se pueden abrir o cerrar meses»**. No se trata de controles deshabilitados: los controles mensuales desaparecen. Para modificar el estado de un mes de un año cerrado hay que abrir primero el año.

**Cerrar y abrir el año no altera el estado individual de los meses:** al volver a abrir el año, la lista reaparece con cada mes tal como estaba.

**Finalidad del cierre mensual:** proteger la información ya conciliada y reportada. Un mes cerrado no admite el registro de movimientos nuevos ni la modificación de los existentes, lo que impide alterar cifras que ya se entregaron o declararon.

## Historial de aperturas y cierres

**Ruta:** `Contabilidad > Configuración > Especiales > Periodos > Historial`.

Abre la ventana **Historial de movimientos**, con el subtítulo «Consulta el historial de periodos». Registra la trazabilidad de los cambios de estado de los periodos de la empresa.

**Diferencia con la información de la fila del mes:** la ventana **Periodos Contables** indica quién cerró cada mes y cuándo, pero solo del estado vigente. El **Historial de movimientos** recoge la secuencia completa de aperturas y cierres, incluidos los de los meses que después volvieron a abrirse.

**Presentación:** no es una tabla de columnas sino una **línea de tiempo vertical**, ordenada de lo más reciente hacia atrás. Cada evento se presenta como una tarjeta precedida de un ícono de estado.

**Contenido de cada entrada:**

| Elemento | Contenido |
| --- | --- |
| Ícono de estado | Un check azul cuando el evento fue una **apertura**; una equis gris cuando fue un **cierre**. |
| Año | El año fiscal al que corresponde el evento. |
| Etiqueta de estado | **ABIERTO** (verde) o **CERRADO** (gris). |
| Fecha | Fecha del evento en formato largo, por ejemplo «14 de septiembre de 2026». |
| Usuario | Usuario que ejecutó la operación. |

**Controles de la ventana:** paginación numerada con selector de registros por página, con valor predeterminado de 7 por página.

**Para qué sirve:** permite explicar por qué un periodo que se creía cerrado aparece abierto, identificar quién reabrió un mes para hacer un ajuste y determinar en qué momento se cerró el año. Cumple para los periodos la misma función que el historial de cambios cumple para los terceros y las cuentas del PUC.

TODO(dato): confirmar cómo distingue la ventana los eventos mensuales de los anuales. En las entradas verificadas la tarjeta muestra únicamente el año, sin indicar el mes afectado ni el tipo de periodo.

## Validaciones al registrar un comprobante

Al registrar un comprobante en `Contabilidad > Comprobantes`, la fecha debe cumplir dos condiciones:

| # | Condición | Consecuencia si no se cumple |
| --- | --- | --- |
| 1 | La fecha debe pertenecer al **año fiscal activo**. | El comprobante no se puede grabar con una fecha de otro año. |
| 2 | El mes de la fecha debe estar **abierto**. | El comprobante no se puede grabar en un mes cerrado. |

**Indicador en la interfaz:** la pantalla del comprobante muestra el estado del periodo correspondiente a la fecha capturada, con los textos **Periodo abierto** o **Periodo cerrado**. Cuando el periodo está cerrado, la etiqueta aparece en ámbar junto al título de la ventana, antes de cualquier intento de guardado.

**Mensaje de error al guardar:** si se intenta grabar de todos modos, la plataforma responde con **«Ocurrió un error — No se pueden realizar operaciones contables en [mes] de [año]. El periodo está cerrado.»** y no persiste ningún cambio.

**Regla de negocio: el cierre también bloquea la edición.** La restricción no se limita a los movimientos nuevos. Un comprobante ya existente cuya fecha cae en un mes cerrado tampoco se puede modificar: al abrirlo aparece la etiqueta **Periodo cerrado** y cualquier cambio guardado con **Actualizar** devuelve el mismo error. Es lo que da sentido al cierre como mecanismo de protección.

**Qué hacer cuando aparece «Periodo cerrado»:** existen dos salidas, y la elección depende de si la fecha es correcta.

1. Si la fecha es la correcta y el movimiento debe quedar en ese mes, abrir el periodo desde `Especiales > Periodos > Gestionar periodos contables`.
2. Si la fecha se digitó por error, corregirla a un mes abierto.

**Orden de diagnóstico recomendado** cuando un comprobante no se graba: primero el año fiscal activo, después el indicador de periodo y solo entonces el contenido del asiento. Las dos primeras causas explican la mayoría de los casos.

## Alcance anual de la información

La mayor parte de la información contable pertenece al año fiscal y cambia al cambiar de año.

| Información | Alcance |
| --- | --- |
| PUC (Plan Único de Cuentas) | Del año fiscal |
| Tipos de documento | Del año fiscal |
| Centros de costo | Del año fiscal |
| Anexos | Del año fiscal |
| Comprobantes y asientos | Del año fiscal |
| Reportes | Del año fiscal |
| Terceros | De la empresa |

**Consecuencia operativa:** cuando el usuario reporta que «no ve» cuentas, asientos, anexos o reportes, la causa más frecuente no es una pérdida de información sino que el año fiscal activo no es el esperado. La primera verificación debe ser el contenedor azul del sidebar.

**Caso típico:** al cambiar a un año fiscal recién habilitado, la pantalla del PUC muestra el mensaje «Actualmente no tienes un plan único de cuentas configurado, puedes elegir una de las siguientes opciones para cargarlo». No es un error: ese año todavía no tiene PUC.

## Ciclo de inicio de un año nuevo

Secuencia recomendada cuando ya existe un año fiscal con movimientos y comienza el siguiente:

| # | Paso | Ruta |
| --- | --- | --- |
| 1 | Habilitar el año nuevo | `Especiales > Periodos > Años fiscales > Agregar año fiscal` |
| 2 | Seleccionarlo como año activo | Contenedor del sidebar o `Alt + A` |
| 3 | Cargar el PUC del año anterior | `Configuración > PUC`, opción **Cargar Puc Año Anterior** |
| 4 | Crear los centros de costo del año | `Configuración > Centros de Costo` |
| 5 | Registrar el asiento de cierre del año anterior | `Especiales > Comprobantes > Cierre anual` |
| 6 | Trasladar los saldos | `Especiales > Comprobantes > Mover Saldos Finales a Iniciales` |
| 7 | Registrar los comprobantes del año | `Contabilidad > Comprobantes`, en meses abiertos |
| 8 | Cerrar cada mes conciliado | `Especiales > Periodos > Gestionar periodos contables` |
| 9 | Cerrar el año al terminar el ejercicio | `Especiales > Periodos > Gestionar periodos contables` |
| 10 | Verificar la trazabilidad de los cierres | `Especiales > Periodos > Historial` |

**Restricción de orden entre los pasos 5 y 8.** El cierre anual es un comprobante con fecha del 31 de diciembre, de modo que exige diciembre abierto. Debe registrarse **antes** de cerrar los periodos del año que se está cerrando; de lo contrario habrá que reabrirlos para poder ejecutarlo.

**No es necesario cerrar el año anterior para empezar el nuevo.** Ambos años pueden permanecer abiertos mientras se termina de cuadrar el anterior. Alternar entre los dos es una operación normal durante los primeros meses del año, y se resuelve cambiando el año activo.

**Los terceros no se rehacen.** A diferencia del PUC y de los centros de costo, los terceros pertenecen a la empresa y siguen disponibles en el año nuevo sin ninguna acción adicional.

## Herramientas complementarias del panel Comprobantes

### Mover Saldos Finales a Iniciales

**Ruta:** `Contabilidad > Configuración > Especiales > Comprobantes > Mover Saldos Finales a Iniciales`.

Traslada los saldos de cierre de un año fiscal a los saldos iniciales del año siguiente. Es el proceso que conecta un ejercicio con el siguiente y **no tiene relación con la apertura o el cierre de periodos**: no cambia el estado de ningún mes.

Abre una ventana con el subtítulo «Transfiere saldos finales a iniciales».

**Campos de la ventana:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Año fiscal origen** | Lista desplegable | Sí | Año del que se toman los saldos finales. |
| **Año fiscal destino** | Lista desplegable | Sí | Año al que se transfieren como saldos iniciales. |
| **Cancelar** | Botón | — | Cierra la ventana sin ejecutar el proceso. |
| **Guardar** | Botón | — | Ejecuta la transferencia. |

**Independencia del año activo:** origen y destino se eligen en la propia ventana, de modo que el proceso puede ejecutarse desde cualquier año fiscal activo. Conviene verificar el orden de los dos campos antes de guardar, porque son visualmente idénticos.

### Cierre anual

**Ruta:** `Contabilidad > Configuración > Especiales > Comprobantes > Cierre anual`.

Proceso contable de cierre del ejercicio. Es distinto de **cerrar el año fiscal** desde *Gestionar periodos contables*: esta última acción bloquea el registro de movimientos, mientras que el Cierre anual registra el asiento contable del cierre.

**No abre un formulario de configuración sino un comprobante.** La opción abre la pantalla **Nuevo CA - Cierre De Año**, con el subtítulo «Complete los datos del asiento contable». Es el formulario estándar de comprobante, precargado para el cierre.

**Valores precargados del encabezado:**

| Campo | Valor |
| --- | --- |
| **Fijar mes** | Diciembre. |
| **Fecha** | 31 de diciembre del año fiscal activo. |
| **Tipo de documento** | **CA - Cierre de año**, uno de los tipos reservados de la plataforma. |
| **Descripción** | «Cierre de ejercicio fiscal [año]». |

**Indicador de periodo:** la pantalla muestra junto al título la etiqueta **Periodo abierto** o **Periodo cerrado**, igual que cualquier comprobante.

**Resto del formulario:** tabla **Cuentas del asiento** con las columnas habituales (cuenta, concepto, factura, tercero, centro de costo, débito y crédito), el botón **Agregar línea**, el resumen de **Total débito**, **Total crédito** y **Diferencia**, y los botones **Cancelar** y **Crear**. Como en cualquier asiento, la diferencia debe quedar en cero para poder grabarlo.

**Regla de negocio derivada: el cierre anual exige diciembre abierto.** Al tratarse de un comprobante con fecha del 31 de diciembre, está sujeto a las mismas validaciones de periodo que cualquier otro asiento. Si diciembre o el año fiscal están cerrados, el cierre anual no se puede crear. El orden correcto es registrar primero el asiento de cierre y cerrar los periodos después.

### Activar/Desactivar Edición de Comprobante

Opción propia del panel **Comprobantes** de Acciones Especiales. Habilita o bloquea la edición de comprobantes.

**Aclaración necesaria: bloquear la edición de comprobantes no es cerrar un periodo.** Son mecanismos con alcances distintos:

| Mecanismo | Qué impide | Dónde se controla |
| --- | --- | --- |
| Cerrar un periodo | Registrar y modificar movimientos con fecha de ese mes. | `Especiales > Periodos > Gestionar periodos contables` |
| Activar/Desactivar Edición de Comprobante | Modificar comprobantes, con independencia del estado del periodo. | `Especiales > Comprobantes > Activar/Desactivar Edición de Comprobante` |

### Mover saldos entre cuentas

Traslada el movimiento registrado en una cuenta del PUC a otra cuenta. No guarda relación con el estado de los periodos.

### Auditoría de Operación

Consulta de las operaciones realizadas en la empresa. Es distinta del **Historial** del panel Periodos, que se limita a las aperturas y los cierres de periodos.

## Solución de problemas

### No aparecen cuentas, asientos, anexos ni reportes

El año fiscal activo no es el esperado. Cada año fiscal tiene su propia información y no comparte contenido con los demás. Debe verificarse el contenedor azul del sidebar y cambiarse al año correcto con `Alt + A` o desde el propio contenedor.

### El año que se necesita no está en el desplegable

Ese año no está habilitado en la empresa. Debe agregarse en `Especiales > Periodos > Años fiscales > Agregar año fiscal` y después seleccionarse como año activo.

### La plataforma no permite quitar un año fiscal

Aparece el mensaje «No se puede quitar el año fiscal en uso. Por favor cambiate a otro año fiscal». El año seleccionado es el año activo. Debe cambiarse el año de trabajo a otro y repetir la operación.

### El PUC aparece vacío en un año recién habilitado

Es el comportamiento esperado. Agregar un año fiscal solo lo habilita: no crea PUC ni centros de costo. El PUC se copia del año anterior con la opción **Cargar Puc Año Anterior** de `Configuración > PUC`, y los centros de costo deben crearse de nuevo.

### El comprobante no se deja grabar en una fecha determinada

Dos causas posibles: el mes está cerrado, o la fecha no pertenece al año fiscal activo. La etiqueta **Periodo cerrado** junto al título de la ventana señala la primera; el contenedor azul del sidebar, la segunda. El mensaje que devuelve la plataforma es «No se pueden realizar operaciones contables en [mes] de [año]. El periodo está cerrado.»

### No se puede editar un comprobante ya existente

Su fecha corresponde a un mes cerrado. El cierre de periodo bloquea tanto el registro de movimientos nuevos como la modificación de los anteriores. Debe abrirse el mes en `Especiales > Periodos > Gestionar periodos contables` o, si el bloqueo no proviene del periodo, revisarse la opción **Activar/Desactivar Edición de Comprobante** del panel Comprobantes.

### El Cierre anual no se puede crear

El Cierre anual es un comprobante con fecha del 31 de diciembre y está sujeto a las mismas validaciones de periodo que cualquier asiento. Si diciembre o el año fiscal completo están cerrados, no se puede grabar. Debe abrirse diciembre en `Especiales > Periodos > Gestionar periodos contables`, registrar el cierre y volver a cerrar el periodo.

### Los saldos iniciales del año nuevo no aparecen

No se ha ejecutado **Mover Saldos Finales a Iniciales**, o se ejecutó con los años invertidos. En la ventana, **Año fiscal origen** debe ser el año que se cierra y **Año fiscal destino** el que comienza.

### La ventana Periodos Contables no muestra los meses

Dos causas posibles: no se ha seleccionado un año en el desplegable **Buscar Año**, en cuyo caso el cuerpo muestra el texto «Selecciona un año»; o el año seleccionado está cerrado, y entonces aparece el aviso **«Año fiscal cerrado — No se pueden abrir o cerrar meses»**. En el segundo caso debe pulsarse **Abrir año**.

### Un mes que se creía cerrado aparece abierto

El periodo fue reabierto. La opción **Historial** del panel Periodos indica qué usuario ejecutó la apertura y en qué momento.

### Se teme que quitar un año elimine la información

No la elimina. El aviso de la propia opción lo declara: «Ya no tendrás disponible este año fiscal. NO se eliminará la información que hayas grabado.» El año únicamente deja de estar disponible para trabajarlo.

## Resumen de reglas de negocio

| # | Regla |
| --- | --- |
| 1 | Al crear una empresa nueva, el año fiscal actual queda habilitado de forma predeterminada. No hay que crear el primer año a mano. |
| 2 | Toda la contabilidad opera sobre el año fiscal activo, identificado en el contenedor azul del sidebar. |
| 3 | El año activo se cambia desde ese contenedor o con el atajo `Alt + A`, mediante la ventana **Configuración de año fiscal**. |
| 4 | El desplegable de años lista únicamente los años habilitados en la empresa. |
| 5 | Agregar un año fiscal solo lo habilita: el año arranca sin PUC y sin centros de costo. |
| 6 | Quitar un año fiscal no elimina la información grabada; solo retira el año de la lista de trabajo. |
| 7 | No se puede quitar el año fiscal en uso. Es necesario cambiarse a otro año primero. |
| 8 | Cada mes del año se abre y se cierra de forma independiente de los demás. |
| 9 | Con el año fiscal cerrado no se pueden abrir ni cerrar meses: la lista de periodos se reemplaza por el aviso «Año fiscal cerrado». |
| 10 | Abrir y cerrar el año no altera el estado individual de los meses. |
| 11 | La ventana Periodos Contables no depende del año fiscal activo: permite gestionar los periodos de cualquier año habilitado. |
| 12 | El cierre de un mes es inmediato, sin diálogo de confirmación previo, y reversible con el botón **Abrir**. |
| 13 | Cada mes cerrado conserva en su fila el usuario que lo cerró y la fecha del cierre. |
| 14 | Un comprobante solo se graba si su fecha pertenece al año fiscal activo y cae en un mes abierto. |
| 15 | El cierre de un periodo bloquea tanto el registro de movimientos nuevos como la edición de los comprobantes ya existentes con fecha de ese mes. |
| 16 | La pantalla del comprobante indica el estado del periodo con los textos **Periodo abierto** y **Periodo cerrado**. |
| 17 | El PUC, los tipos de documento, los centros de costo, los anexos, los comprobantes y los reportes pertenecen al año fiscal. Los terceros pertenecen a la empresa. |
| 18 | Todas las aperturas y los cierres quedan registrados en el **Historial de movimientos**, con su usuario, su fecha y si el evento fue una apertura o un cierre. |
| 19 | Cerrar el año fiscal no es lo mismo que ejecutar el Cierre anual contable. |
| 20 | El Cierre anual es un comprobante con fecha del 31 de diciembre y tipo de documento CA, sujeto a las validaciones de periodo: exige diciembre abierto. |
| 21 | Mover Saldos Finales a Iniciales toma el año origen y el año destino de su propia ventana, con independencia del año fiscal activo. |
| 22 | El mes de trabajo se fija en el campo **Fijar mes** del formulario del comprobante, no en la ventana Configuración de año fiscal. |
| 23 | Bloquear la edición de comprobantes no es cerrar un periodo. |

## Preguntas frecuentes

**¿Qué es un año fiscal en Zoe?**
El contenedor del trabajo contable de un año determinado: dentro de él viven el PUC, los asientos, los anexos, los tipos de documento y los reportes de ese año.

**¿Qué es un periodo contable?**
Cada mes del año fiscal, de enero a diciembre. Cada uno se abre o se cierra de forma independiente.

**¿Hay que configurar el año fiscal al crear la empresa?**
No. Siempre queda habilitado el año actual de forma predeterminada, y aparece seleccionado al entrar a Contabilidad.

**¿Dónde se ve el año con el que se está trabajando?**
En el contenedor azul del sidebar del menú Contabilidad, junto a la palabra «Contabilidad».

**¿Cómo se cambia el año de trabajo?**
Desde ese contenedor o con el atajo `Alt + A`. Ambas vías abren la ventana **Configuración de año fiscal**.

**¿Por qué no se ven cuentas, asientos o anexos?**
Porque el año fiscal activo no es el esperado. Cada año tiene su propia información. Debe revisarse el contenedor del sidebar.

**¿Cómo se trabaja en un año distinto al actual?**
Agregando ese año en `Especiales > Periodos > Años fiscales > Agregar año fiscal` y seleccionándolo después en el sidebar.

**¿Se pueden habilitar años anteriores al actual?**
Sí. El desplegable de **Agregar año fiscal** admite años anteriores y posteriores.

**¿Al quitar un año se borra la información?**
No. El año solo deja de estar disponible para trabajarlo. La información grabada se conserva, como lo advierte el aviso de la opción.

**¿Por qué no se puede quitar un año fiscal?**
Porque es el año en uso. Hay que cambiarse a otro año fiscal y luego quitarlo.

**¿Qué pasa si se vuelve a agregar un año que se había quitado?**
Vuelve a estar disponible con la información que tenía, porque nunca se eliminó.

**¿Un año fiscal nuevo trae el PUC del año anterior?**
No. Se copia con la opción **Cargar Puc Año Anterior** de `Configuración > PUC`.

**¿Los centros de costo pasan al año nuevo?**
No. Deben crearse de nuevo en cada año fiscal.

**¿Los terceros hay que volver a cargarlos cada año?**
No. Los terceros pertenecen a la empresa y están disponibles en todos los años.

**¿Dónde se abren y se cierran los meses?**
En `Contabilidad > Configuración > Especiales > Periodos > Periodos contables > Gestionar periodos contables`, que abre la ventana **Periodos Contables**.

**¿Hay que cambiar el año activo para cerrar un mes de otro año?**
No. La ventana **Periodos Contables** tiene su propio desplegable **Buscar Año** y permite gestionar los periodos de cualquier año habilitado sin salir del año en el que se está trabajando.

**¿Por qué la ventana de periodos aparece vacía al abrirla?**
Porque todavía no se ha seleccionado un año. El cuerpo muestra el texto «Selecciona un año» hasta que se elige uno en **Buscar Año**.

**¿Qué significa la barra «Progreso del año»?**
Indica cuántos de los doce meses del año fiscal están cerrados, con el contador `N/12` a su derecha.

**¿Se pueden tener meses abiertos y cerrados a la vez?**
Sí. Cada mes se gestiona por separado dentro del año fiscal.

**¿Cerrar un mes pide confirmación?**
No. El cierre es inmediato y la plataforma responde con «Mes cerrado correctamente». La acción es reversible con el botón **Abrir** de la misma fila.

**¿Por qué no se pueden abrir ni cerrar meses?**
Porque el año fiscal está cerrado. En ese estado la lista de meses desaparece y en su lugar aparece el aviso «Año fiscal cerrado — No se pueden abrir o cerrar meses»; primero hay que pulsar **Abrir año**.

**¿Cerrar y volver a abrir el año cambia el estado de los meses?**
No. Al abrir el año, cada mes reaparece en el estado en que quedó.

**¿Por qué no se puede grabar un comprobante en cierta fecha?**
Porque el mes está cerrado o porque la fecha no pertenece al año fiscal activo.

**¿Cómo se sabe si un periodo está abierto antes de grabar?**
La pantalla del comprobante muestra **Periodo abierto** o **Periodo cerrado** según la fecha capturada. La etiqueta de periodo cerrado aparece en ámbar junto al título de la ventana.

**¿Qué mensaje muestra la plataforma al intentar guardar en un mes cerrado?**
«No se pueden realizar operaciones contables en [mes] de [año]. El periodo está cerrado.»

**¿Se puede editar un comprobante ya existente de un mes cerrado?**
No. El cierre bloquea tanto el registro de movimientos nuevos como la modificación de los anteriores.

**¿Qué hacer si aparece «Periodo cerrado» y la fecha es la correcta?**
Abrir ese mes desde **Gestionar periodos contables** y volver a grabar.

**¿Se puede saber quién cerró o abrió un periodo?**
Sí, por dos vías. La fila del mes en **Periodos Contables** muestra «Cerrado por» y «Fecha» del estado vigente, y la opción **Historial** del panel Periodos abre el **Historial de movimientos**, una línea de tiempo con la secuencia completa de aperturas y cierres, cada una con su usuario y su fecha.

**¿Hay que cerrar el año anterior para empezar a trabajar el año nuevo?**
No. Ambos años pueden estar abiertos al mismo tiempo mientras se termina de cuadrar el anterior.

**¿Cómo pasan los saldos de un año al siguiente?**
Con la opción **Mover Saldos Finales a Iniciales** del panel Comprobantes de Acciones Especiales, indicando el **Año fiscal origen** y el **Año fiscal destino**.

**¿Hay que estar parado en algún año para mover los saldos?**
No. La ventana pide el año origen y el año destino, así que el proceso se ejecuta desde cualquier año fiscal activo.

**¿Cerrar el año fiscal es lo mismo que el Cierre anual?**
No. Cerrar el año fiscal bloquea el registro de movimientos. El **Cierre anual** registra el asiento contable de cierre del ejercicio.

**¿Qué abre la opción Cierre anual?**
Un comprobante: la pantalla **Nuevo CA - Cierre De Año**, con el tipo de documento **CA - Cierre de año**, la fecha en el 31 de diciembre y el mes fijado en Diciembre. Se diligencia como cualquier asiento y se graba con **Crear**.

**¿Por qué el Cierre anual no se deja crear?**
Porque diciembre o el año fiscal están cerrados. Al ser un comprobante con fecha del 31 de diciembre, necesita ese periodo abierto.

**¿Qué va primero, el cierre anual o cerrar los periodos?**
El cierre anual. Si se cierran los periodos antes, hay que reabrir diciembre para poder registrarlo.

**¿Dónde se fija el mes de trabajo?**
En el campo **Fijar mes** del formulario del comprobante, a la izquierda de la fecha. No está en la ventana Configuración de año fiscal, que solo tiene el campo Año.

**¿Bloquear la edición de un comprobante cierra el periodo?**
No. Son controles distintos: cerrar un periodo impide registrar movimientos con fecha de ese mes, y bloquear la edición impide modificar comprobantes concretos.

**¿Para qué sirve entonces quitar un año fiscal?**
Para mantener limpio el selector de años y reducir el riesgo de que alguien se cambie por error a un año que ya no se trabaja y registre movimientos ahí.
