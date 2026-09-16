---
title: Terceros
description: Administración de los terceros de la empresa (clientes, proveedores, empleados y demás participantes de las operaciones contables). Cubre la pantalla de Terceros, la creación y edición de registros, las validaciones de identidad para persona natural y persona jurídica, la diferencia entre terceros nacionales y extranjeros, el procedimiento especial para modificar el documento o NIT desde Configuración > Especiales, las restricciones para eliminar terceros con movimientos contables asociados, la importación masiva desde Excel con su resumen de resultados, y la consulta del historial de auditoría de cambios.
module: contabilidad
category: configuracion
slug: terceros
order: 8
tags:
  - configuracion
  - terceros
  - tercero
  - persona-natural
  - persona-juridica
  - razon-social
  - nit
  - documento-de-identificacion
  - actualizar-documento
  - eliminar-tercero
  - importacion-excel
  - carga-masiva
  - auditoria
  - trazabilidad
  - acciones-especiales
  - municipio
  - extranjeros
  - puc
  - solicitar
  - comprobantes
  - reportes-contables
  - contabilidad
  - optimun
draft: false
rag_exclude: false
last_updated: 2026-09-07
---

# Terceros

Un tercero es toda persona o entidad con la que la empresa tiene una relación económica y que queda identificada en sus registros contables: clientes, proveedores, empleados, entidades oficiales y demás participantes de las operaciones. La pantalla de Terceros es el maestro único donde esos registros se crean, se consultan y se mantienen, y del que se alimentan los comprobantes y los reportes. Este documento explica dónde está la pantalla, cómo se crean y editan los terceros, qué exige el sistema según sean personas naturales o jurídicas y nacionales o extranjeras, cómo se modifica el documento o NIT mediante el procedimiento especial, por qué no siempre es posible eliminar un tercero, cómo se cargan varios a la vez desde un archivo de Excel y cómo se consulta el historial de auditoría de los cambios.

## Tabla de contenido

1. [Ubicación en la aplicación](#ubicación-en-la-aplicación)
2. [Requisitos previos](#requisitos-previos)
3. [Concepto: qué es un tercero](#concepto-qué-es-un-tercero)
4. [Alcance: los terceros son globales](#alcance-los-terceros-son-globales)
5. [Elementos de la pantalla](#elementos-de-la-pantalla)
6. [Crear un tercero](#crear-un-tercero)
7. [Tipos de tercero y validaciones de identidad](#tipos-de-tercero-y-validaciones-de-identidad)
8. [Editar un tercero](#editar-un-tercero)
9. [Actualizar el documento o NIT de un tercero](#actualizar-el-documento-o-nit-de-un-tercero)
10. [Eliminar un tercero y sus restricciones](#eliminar-un-tercero-y-sus-restricciones)
11. [Importación masiva desde Excel](#importación-masiva-desde-excel)
12. [Historial de auditoría de terceros](#historial-de-auditoría-de-terceros)
13. [Exigencia del tercero desde el PUC](#exigencia-del-tercero-desde-el-puc)
14. [Uso del tercero en los reportes](#uso-del-tercero-en-los-reportes)
15. [Solución de problemas](#solución-de-problemas)
16. [Resumen de reglas de negocio](#resumen-de-reglas-de-negocio)
17. [Preguntas frecuentes](#preguntas-frecuentes)

## Ubicación en la aplicación

- **Ruta de menú:** `Contabilidad > Configuración > Terceros`.
- **Ruta de navegación mostrada en la pantalla (breadcrumb):** `PANEL / CONFIGURACIÓN / TERCEROS`.
- **Título de la pantalla:** «Terceros».
- **Subtítulo de la pantalla:** «Gestiona y administra los terceros de tu empresa».
- **Contenido de la pantalla:** una tarjeta titulada «Listado de terceros», con la tabla de los terceros registrados en la empresa y el contador de registros junto al título.

**Rutas complementarias:**

| Proceso | Ruta |
| --- | --- |
| Modificar el documento o NIT de un tercero | `Contabilidad > Configuración > Especiales > Terceros > Actualizar documento` |
| Consultar el historial de cambios de un tercero | `Contabilidad > Configuración > Terceros`, ícono de historial en las acciones de la fila |
| Exigir el tercero en una cuenta contable | `Contabilidad > Configuración > PUC`, campo **Solicitar** |
| Registrar el tercero en un movimiento | `Contabilidad > Comprobantes`, columna **Tercero** |

## Requisitos previos

- Tener una empresa creada y seleccionada en Zoe.
- Tener acceso al módulo de Contabilidad.
- Contar con la información de identificación del tercero: tipo y número de documento, razón social o nombres y apellidos, y su ubicación.
- Para la importación masiva, disponer de la plantilla oficial de Excel.

## Concepto: qué es un tercero

Un **tercero** es una persona natural o jurídica con la que la empresa mantiene una relación económica y que se identifica en los registros contables. Comprende a los clientes, los proveedores, los empleados, las entidades oficiales y cualquier otro participante de las operaciones de la empresa.

Mientras la cuenta del PUC indica la naturaleza del movimiento (qué ocurrió) y el centro de costo indica su origen organizacional (dónde ocurrió dentro de la empresa), el tercero indica **con quién** se realizó la operación.

**Función del tercero en la plataforma:**

| Ámbito | Función |
| --- | --- |
| Comprobantes contables | Identifica a la contraparte de cada movimiento. Se registra en la columna **Tercero** de la tabla **Cuentas del asiento**. |
| Cuentas del PUC | Las cuentas marcadas con **Solicitar > Tercero** obligan a indicar el tercero cada vez que se utilizan en un asiento. |
| Reportes contables | Permite filtrar y agrupar la información por tercero, para obtener el detalle de lo registrado con un cliente, un proveedor o un empleado en particular. |
| Trazabilidad | Sostiene el historial financiero: cada movimiento queda enlazado al tercero con el que se realizó. |

Un mismo tercero puede cumplir varios papeles a la vez: una empresa puede ser cliente y proveedor al mismo tiempo. El registro es uno solo, identificado por su documento, y son los movimientos contables los que determinan en qué condición participa en cada operación.

## Alcance: los terceros son globales

Los terceros pertenecen a la **empresa**, no al año fiscal. Se crean una vez y quedan disponibles para todos los años fiscales.

| Información | Alcance |
| --- | --- |
| Terceros | Global (por empresa) |
| PUC (Plan Único de Cuentas) | Por año fiscal |
| Centros de costo | Por año fiscal |
| Tipos de documento | Por año fiscal |
| Comprobantes | Por año fiscal |

**Consecuencia práctica:** al habilitar un año fiscal nuevo no hay que volver a crear los terceros, a diferencia de lo que ocurre con los centros de costo y con el PUC. Si un tercero no aparece en el listado, no es por el año fiscal seleccionado: es que no está creado en la empresa.

**Nota sobre la marca del PUC:** lo que sí pertenece al año fiscal es la marca **Solicitar > Tercero** de cada cuenta contable, porque vive dentro del PUC. Esa configuración debe revisarse en cada año fiscal cuyo plan se cargue o se copie.

## Elementos de la pantalla

La pantalla presenta una tabla en la que cada fila corresponde a un tercero registrado en la empresa.

La tarjeta que contiene la tabla se titula **Listado de terceros** y muestra junto al título el número de registros de la empresa.

**Columnas de la tabla:**

| Columna | Contenido |
| --- | --- |
| **NIT / Documento** | Número de documento o NIT del tercero. |
| **Razón social / Nombre** | Razón social de las personas jurídicas, o el nombre compuesto de las personas naturales. |
| **Tipo de tercero** | Etiqueta que indica la relación del tercero con la empresa: **Cliente**, **Proveedor** u **Otro**. |
| **Contacto** | Teléfono y correo electrónico registrados. |
| **Dirección** | Dirección registrada del tercero. |
| **Acciones** | Los tres botones de la fila: editar, historial de cambios y eliminar. |

**Controles de la pantalla:**

| Control | Ubicación | Descripción |
| --- | --- | --- |
| **Consultar** | Parte superior | Campo de texto para buscar un tercero por documento, razón social u otro criterio. |
| **Filtrar** | Junto a **Consultar** | Ejecuta la búsqueda según el criterio ingresado. |
| **Importar** | Sobre la tabla, a la derecha | Desplegable con dos opciones: **Subir desde plantilla** y **Descargar plantilla**. Ver [Importación masiva desde Excel](#importación-masiva-desde-excel). |
| **Descargar** | Sobre la tabla, a la derecha | Exporta a Excel el listado de terceros de la empresa. |
| **Nuevo** | Sobre la tabla, a la derecha | Abre la ventana **Nuevo tercero**. |
| **Columnas** | Sobre la tabla, a la derecha | Permite mostrar u ocultar columnas de la tabla. |
| **Editar** (ícono de lápiz) | En cada fila | Abre la ventana **Editar tercero**. |
| **Historial** (ícono de reloj) | En cada fila | Abre la ventana **Historial de cambios** del tercero. Ver [Historial de auditoría de terceros](#historial-de-auditoría-de-terceros). |
| **Eliminar** (ícono de papelera) | En cada fila | Elimina el tercero, siempre que no tenga movimientos contables asociados. |
| **Paginación** | Debajo de la tabla | Navegación entre páginas del listado. |
| **Selector de registros por página** | Debajo de la tabla | Define cuántos registros se muestran por página. |

**No existe una acción para restaurar terceros.** La eliminación es permanente, de modo que las tres acciones de la fila son editar, consultar el historial y eliminar.

**Búsqueda antes de crear:** conviene buscar el documento antes de registrar un tercero nuevo. El documento es el dato que identifica de forma única a cada tercero dentro de la empresa, de modo que buscarlo primero evita intentos de creación duplicada y, sobre todo, evita crear con un documento equivocado un registro cuyo número después solo podrá corregirse por el procedimiento especial.

## Crear un tercero

Al seleccionar el botón **Nuevo** se abre la ventana **Nuevo tercero**, con el subtítulo «Registra un nuevo proveedor o tercero».

**Campos comunes a todos los terceros:**

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Tipo de identificación** | Lista desplegable | Sí | Clase de documento del tercero: **Nit**, **Cédula de ciudadanía**, **Pasaporte**, entre otros. |
| **NIT/Documento** | Texto | Sí | Número de documento del tercero. Es el dato que lo identifica de forma única dentro de la empresa. |
| **DV** | Texto | No | Dígito de verificación. La plataforma lo completa a partir del número digitado. |
| **Régimen de IVA** | Lista desplegable | Sí | Condición del tercero frente al IVA: **Responsable del iva** o **No responsable del iva**. |
| **Responsabilidad tributaria** | Lista desplegable | Sí | Responsabilidad tributaria del tercero, por ejemplo **Agente retención iva** o **Regimen simple de tributación**. |
| **Tipo de tercero** | Lista desplegable | Sí | Relación del tercero con la empresa: **Cliente**, **Proveedor** u **Otro**. |
| **Tipo de persona** | Lista desplegable | Sí | **Persona natural** o **Persona jurídica**. Define qué campos de nombre exige el formulario. |
| **Correo electrónico** | Texto | Sí | Correo de contacto del tercero. |
| **¿Es un tercero extranjero?** | Casilla | No | «Marcar si es extranjero (No reside en el país)». Cambia los campos de ubicación que pide el formulario. |
| **Dirección** | Texto | Sí | Dirección del tercero. |
| **Teléfonos** | Bloque repetible | No | Uno o varios teléfonos, cada uno con su indicativo de país. Cada línea tiene su propio interruptor y su botón para eliminarla; la fila con **+** agrega otra. |
| **Cancelar** | Botón | — | Cierra la ventana sin guardar. |
| **Crear** | Botón | — | Guarda el tercero. |

Los campos de **nombre** y de **ubicación** cambian según el tipo de persona y según si el tercero es nacional o extranjero. Se describen en [Tipos de tercero y validaciones de identidad](#tipos-de-tercero-y-validaciones-de-identidad).

**No confundir Tipo de tercero con Tipo de persona.** Son dos campos distintos y contiguos en el formulario. **Tipo de tercero** describe la relación comercial (Cliente, Proveedor u Otro) y es el valor que se muestra como etiqueta en el listado. **Tipo de persona** describe la naturaleza jurídica del tercero (natural o jurídica) y es el que determina qué campos de nombre exige el sistema.

**Pasos:**

1. Ir a `Contabilidad > Configuración > Terceros`.
2. Buscar el documento en el campo de búsqueda para verificar que el tercero no exista ya.
3. Seleccionar el botón **Nuevo**.
4. Diligenciar **Tipo de identificación** y **NIT/Documento**.
5. Seleccionar **Régimen de IVA**, **Responsabilidad tributaria** y **Tipo de tercero**.
6. Seleccionar **Tipo de persona** y diligenciar los campos de nombre que el formulario exija según esa selección.
7. Marcar la casilla **¿Es un tercero extranjero?** si corresponde, y diligenciar la ubicación: **Municipio** si el tercero es nacional, o **País** y **Ciudad** si es extranjero.
8. Completar **Correo electrónico**, **Dirección** y los **Teléfonos**.
9. Seleccionar el botón **Crear**.

Resultado: el tercero queda disponible de inmediato para asociarlo a los movimientos de cualquier comprobante de la empresa, en cualquier año fiscal.

**Verificar el documento antes de confirmar:** el número de documento queda bloqueado en la pantalla de edición una vez creado el tercero, y solo puede corregirse mediante el procedimiento especial descrito más adelante. Conviene revisarlo antes de guardar.

## Tipos de tercero y validaciones de identidad

El sistema aplica validaciones distintas según dos criterios independientes: la naturaleza del tercero (persona natural o jurídica) y su ubicación (nacional o extranjero).

### Persona natural y persona jurídica

| Tipo de persona | Campos de nombre del formulario | Cómo se forma el nombre del tercero |
| --- | --- | --- |
| **Persona jurídica** | **Razón social** (obligatorio). | La razón social digitada es el nombre con el que el tercero aparece en el listado, en los comprobantes y en los reportes. |
| **Persona natural** | **Primer nombre** y **Primer apellido** (obligatorios); **Segundo nombre**, **Segundo apellido** y **Nombre comercial** (opcionales). | El sistema **construye internamente la razón social** a partir de los nombres y apellidos diligenciados. No hay campo de razón social. |

**Regla de negocio:** todo tercero tiene una razón social. En las personas jurídicas la digita el usuario; en las personas naturales la compone el sistema con los nombres y apellidos. Por eso el formulario no pide razón social cuando el tercero es una persona natural: pedirla sería duplicar un dato que la plataforma ya deriva.

**Implicación práctica:** la razón social compuesta es el texto que se verá después en el listado de terceros, en el desplegable del comprobante y en los reportes. De ahí que convenga diligenciar los nombres y apellidos completos y bien escritos: son el nombre con el que ese tercero va a existir en toda la contabilidad.

### Terceros nacionales y extranjeros

El formulario decide qué campos de ubicación pedir según la casilla **¿Es un tercero extranjero?** («Marcar si es extranjero (No reside en el país)»).

| Ubicación | Campos de ubicación del formulario |
| --- | --- |
| **Nacional** (casilla sin marcar) | **Municipio** (obligatorio), que se selecciona de una lista. |
| **Extranjero** (casilla marcada) | **País** (obligatorio), **Ciudad** (obligatorio) y **Estado** (opcional). El campo **Municipio** desaparece del formulario, porque la lista de municipios corresponde a la división territorial nacional y no aplica a un tercero del exterior. |

Los dos criterios se combinan: un tercero puede ser una persona jurídica nacional (razón social y municipio), una persona natural nacional (nombres, apellidos y municipio), una persona jurídica extranjera (razón social, país y ciudad) o una persona natural extranjera (nombres, apellidos, país y ciudad).

**Por qué el sistema lo exige:** la identificación y la ubicación del tercero no son datos decorativos. Sostienen los reportes contables y los requerimientos de información que la empresa debe presentar, en los que cada tercero debe quedar plenamente identificado. Un registro incompleto se convierte después en una corrección sobre movimientos ya contabilizados.

## Editar un tercero

El ícono de lápiz de la fila abre la ventana **Editar tercero**, con el subtítulo «Actualiza los datos del cliente, proveedor u otro tercero». El formulario es el mismo de la creación y permite modificar el nombre o la razón social, el tipo de tercero, la información tributaria, la ubicación y los datos de contacto. El botón de confirmación se llama **Actualizar** en lugar de **Crear**.

**Los campos de identificación están bloqueados en esta pantalla.** **Tipo de identificación**, **NIT/Documento** y **DV** aparecen en gris y no admiten cambios; son los únicos datos del tercero que no se modifican desde la edición normal. Ver [Actualizar el documento o NIT de un tercero](#actualizar-el-documento-o-nit-de-un-tercero).

**Efecto de los cambios:** los movimientos contables quedan asociados al tercero por su identificador interno, no por el texto de su nombre. Al corregir la razón social, el cambio se refleja también en los movimientos ya registrados y en los reportes que se generen a partir de ese momento. La edición sirve para corregir o actualizar los datos de un tercero existente, no para reutilizar el registro con un tercero distinto: eso mezclaría bajo una misma identidad los movimientos de dos contrapartes diferentes.

## Actualizar el documento o NIT de un tercero

El campo de documento o NIT permanece **bloqueado en la pantalla de edición** por seguridad e integridad de los datos.

**Razón del bloqueo:** el documento es la llave con la que se identifica al tercero dentro de la empresa. De él dependen el enlace de los movimientos contables ya registrados, la identificación del tercero en los reportes y la lógica de la importación masiva, que decide crear o actualizar un registro según ese número. Permitir su modificación desde la edición corriente, junto al resto de campos, expondría ese enlace a un cambio accidental. Por eso la plataforma lo separa en un proceso propio, deliberado y trazable.

**Ruta del procedimiento:** `Contabilidad > Configuración > Especiales > Terceros > Actualizar documento`.

**Pasos:**

1. Ir a `Contabilidad > Configuración > Especiales`.
2. Ubicar el panel **Terceros**, que contiene una única opción.
3. Seleccionar la opción **Actualizar documento**.
4. En el campo **Tercero**, buscar y seleccionar el tercero cuyo documento se va a modificar.
5. Ajustar **Tipo de identificación** y **NIT/Documento**.
6. Seleccionar el botón **Guardar**.

**Campos de la ventana Actualizar documento de tercero** («Modifica el documento de identificación»):

| Campo | Tipo | Obligatorio | Descripción |
| --- | --- | --- | --- |
| **Tercero** | Buscador | Sí | Identifica al tercero que se va a modificar. Una vez seleccionado, muestra su nombre junto al documento actual. |
| **Tipo de identificación** | Lista desplegable | Sí | Permite cambiar también la clase de documento, no solo el número. |
| **NIT/Documento** | Texto | Sí | Número de documento nuevo. |
| **DV** | Texto | No | Dígito de verificación correspondiente al número nuevo. |
| **Cancelar** | Botón | — | Cierra la ventana sin guardar. |
| **Guardar** | Botón | — | Aplica el cambio de documento. |

**El proceso también cambia el tipo de identificación.** No se limita al número: sirve, por ejemplo, para corregir un tercero que quedó registrado con cédula de ciudadanía cuando debía quedar con NIT o con pasaporte.

**Alcance del cambio:** el proceso actualiza el documento del tercero conservando su identidad y su historial. Los movimientos contables ya registrados siguen enlazados al mismo tercero, ahora identificado con el documento corregido; no se duplica el registro ni se pierde el historial.

**Cuándo se usa:** para corregir un documento digitado de forma errónea o para actualizar el número cuando el tercero cambia de identificación. No es el camino para trasladar los movimientos de un tercero a otro: si los movimientos corresponden realmente a otra contraparte, deben corregirse en los comprobantes.

## Eliminar un tercero y sus restricciones

El ícono de papelera de cada fila permite eliminar un tercero, pero la eliminación **no siempre es posible**.

**La eliminación es permanente.** Al seleccionar la papelera, la plataforma abre el diálogo **¿Estás seguro?** con la advertencia «Esta acción no se puede deshacer» y el texto «El tercero **[nombre]** será eliminado de forma permanente. Esta acción no se puede deshacer», con los botones **Cancelar** y **Si, eliminar**. No existe una papelera de reciclaje ni una acción para restaurar terceros eliminados.

**Regla de negocio:** el sistema no permite eliminar un tercero que tenga movimientos o asientos contables asociados. Al confirmar la eliminación de un tercero en esa condición, la plataforma muestra el mensaje **«Ocurrió un error — No se puede eliminar el tercero porque está referenciado por comprobantes contables»** y el registro se conserva.

**Por qué:** eliminar un tercero que ya participó en la contabilidad dejaría movimientos registrados sin contraparte identificable. Los comprobantes perderían el dato de con quién se realizó la operación, los reportes por tercero quedarían incompletos y el historial financiero de la empresa dejaría de ser reconstruible. La restricción protege la trazabilidad: la contabilidad debe poder explicarse hacia atrás, y para eso cada movimiento necesita conservar su tercero.

**Qué se puede eliminar:** los terceros creados que todavía no han participado en ningún movimiento contable. Es el caso de un registro creado por error o de un duplicado detectado antes de usarlo.

**Qué hacer cuando el tercero no se puede eliminar:** si un tercero ya tiene movimientos y no debe seguir usándose, la vía no es la eliminación sino dejar de utilizarlo en los comprobantes nuevos. Su historial permanece disponible para consulta y para los reportes de los períodos en los que sí participó.

**Duplicados:** cuando el mismo tercero quedó registrado dos veces con documentos distintos y ambos tienen movimientos, ninguno de los dos se podrá eliminar. La corrección pasa por revisar los comprobantes involucrados. De ahí la recomendación de buscar el documento antes de crear un tercero nuevo.

## Importación masiva desde Excel

La importación masiva permite crear y actualizar varios terceros a la vez a partir de un archivo de Excel, en lugar de registrarlos uno por uno desde el formulario.

### Dónde está

En la pantalla de Terceros, el botón **Importar** despliega dos opciones:

| Opción | Función |
| --- | --- |
| **Descargar plantilla** | Descarga el archivo de Excel con la estructura que espera el proceso. Es el punto de partida: la carga debe construirse sobre esta plantilla. |
| **Subir desde plantilla** | Abre la ventana **Importar terceros desde Excel** para cargar el archivo diligenciado. |

Junto a **Importar** está el botón **Descargar**, que cumple una función distinta: exporta a Excel el listado de terceros ya registrados en la empresa.

**Confirmación previa:** la ventana **Importar terceros desde Excel** muestra primero un aviso titulado «Creación y actualización de terceros», con el texto «Si el registro no existe en la plataforma se creará. Si ya existe, se modificará con la información del archivo que estás cargando», y debajo la advertencia «Solo continúa si has revisado el archivo y aceptas esta operación». El proceso continúa con el botón **Continuar y elegir archivo**, que abre el selector de archivos del equipo. La otra opción es **Cancelar**.

Ese aviso es la regla de negocio del proceso, y la plataforma la presenta antes de dejar seleccionar el archivo precisamente porque la carga puede modificar terceros que ya existen.

### Lógica de procesamiento

El proceso se resuelve fila por fila y toma el **documento** como criterio de identificación:

| Situación de la fila | Resultado |
| --- | --- |
| El documento **no existe** en la empresa | Se **crea** el tercero con los datos de la fila. |
| El documento **ya existe** en la empresa | Se **actualiza** el tercero existente con los datos de la fila. |

**Consecuencia:** la importación no es solo un proceso de alta, también es un proceso de actualización. Volver a cargar un archivo ya procesado no genera terceros duplicados: los registros existentes se actualizan con los valores del archivo.

**Advertencia:** por esa misma razón, un dato mal diligenciado en el archivo sobrescribe la información del tercero que ya estaba registrado. Conviene revisar el contenido del archivo antes de cargarlo, sobre todo cuando incluye documentos que ya existen en la empresa.

### Requisitos del archivo

| Requisito | Detalle |
| --- | --- |
| **Formato** | El archivo debe ser `.xlsx`. |
| **Plantilla oficial** | Debe usarse la plantilla que se obtiene en **Importar > Descargar plantilla**, sin alterar sus columnas, su orden ni sus encabezados. El proceso lee cada columna según la estructura de la plantilla. |
| **Sin fórmulas** | Las celdas deben contener valores, no fórmulas. Si el contenido se preparó en otra hoja de cálculo, debe pegarse como valor antes de cargarlo. |
| **Límite de filas** | El archivo no debe superar el número máximo de filas admitido. TODO(dato): indicar el límite exacto. |
| **Límite de tamaño** | El archivo no debe superar el tamaño máximo admitido. TODO(dato): indicar el límite exacto. |

TODO(dato): listar las columnas de la plantilla oficial e indicar cuáles son obligatorias.

**Sobre las validaciones:** las reglas del formulario también rigen en la importación. Cada fila debe traer la razón social si el tercero es una persona jurídica, o los nombres y apellidos si es una persona natural, y la ubicación que corresponda según sea nacional o extranjero. Las filas que no cumplan se reportan como fallidas.

### Resumen de resultados

Al finalizar la carga, la plataforma presenta un resumen de lo ocurrido:

| Dato del resumen | Qué indica |
| --- | --- |
| **Registros procesados** | Total de filas que el sistema leyó del archivo. |
| **Registros creados** | Terceros nuevos, cuyo documento no existía en la empresa. |
| **Registros actualizados** | Terceros que ya existían y cuyos datos fueron modificados con los del archivo. |
| **Registros fallidos** | Filas que no se pudieron procesar. |
| **Detalle de errores por fila** | Para cada fila fallida, el número de fila y el motivo del rechazo. |

**Cómo se usa el resumen:** el detalle por fila indica exactamente dónde está el problema dentro del archivo, de modo que la corrección se hace sobre las filas señaladas y no sobre el archivo completo. Como la importación actualiza los documentos que ya existen, el archivo corregido puede volver a cargarse íntegro sin duplicar los terceros que sí se procesaron en el primer intento.

**Verificación posterior:** conviene confirmar en el listado de Terceros que los registros creados aparecen con la información esperada, en especial la razón social de las personas naturales, que el sistema compone a partir de los nombres y apellidos del archivo.

## Historial de auditoría de terceros

La plataforma conserva la trazabilidad de los cambios realizados sobre cada tercero, de modo que pueda consultarse qué se modificó, cuándo y quién lo hizo.

**Ruta de consulta:** el historial es **una acción de la fila** en la pantalla de Terceros. Se abre con el **ícono de reloj** de la columna **Acciones**, entre el lápiz de editar y la papelera de eliminar. No se consulta desde Acciones Especiales.

Se abre la ventana **Historial de cambios**, con el subtítulo «Cambios registrados sobre los datos propios de este tercero».

**Columnas del historial:**

| Columna | Contenido |
| --- | --- |
| **Fecha** | Fecha y hora en que se realizó el cambio. |
| **Usuario** | Usuario que ejecutó el cambio. |
| **Evento** | Tipo de operación registrada, por ejemplo «Tercero modificado». |
| **Campo** | Dato del tercero que se modificó: Dirección, Nombre Comercial, Régimen IVA, Responsabilidad Tributaria, entre otros. |
| **Antes** | Valor que tenía el campo antes del cambio, resaltado en rojo. |
| **Después** | Valor que quedó registrado tras el cambio, resaltado en verde. |

Cada modificación genera una fila por campo alterado: si en una misma edición se cambian la dirección y el nombre comercial, el historial registra dos filas con la misma fecha y el mismo usuario.

**Controles de la ventana:** campo **Consultar** con botón **Filtrar** para buscar dentro del historial, botón de refrescar, selector de **Columnas**, paginación con selector de registros por página y botón **Cerrar**.

**Alcance:** el historial recoge los cambios sobre los datos propios del tercero. TODO(dato): confirmar si las eliminaciones de terceros quedan registradas en alguna vista, dado que el historial se consulta desde la ficha del tercero y la eliminación es permanente.

**Para qué sirve:** permite reconstruir por qué un tercero luce hoy distinto de como se registró, identificar el origen de un dato incorrecto y responder por los cambios ante una revisión o una auditoría. Junto con la restricción de eliminación y el procedimiento especial para el documento, forma el conjunto de controles con los que la plataforma protege la integridad del maestro de terceros.

## Exigencia del tercero desde el PUC

Crear los terceros no basta para que la información quede clasificada: el dato **se exige desde la cuenta contable**, no desde la pantalla de Terceros.

En `Contabilidad > Configuración > PUC`, las ventanas **Nueva cuenta** y **Editar cuenta** contienen el campo **Solicitar**, cuyo desplegable ofrece dos valores: **Tercero** y **Centro de costo**. Cuando en una cuenta se selecciona **Tercero**, la plataforma obliga a indicar el tercero cada vez que esa cuenta se utiliza en un asiento contable.

**Reglas del campo Solicitar:**

| # | Regla |
| --- | --- |
| 1 | El campo **Solicitar** solo aparece cuando la cuenta está marcada con la casilla **¿Es auxiliar?**, porque las cuentas auxiliares son las que reciben los movimientos. |
| 2 | El campo admite **Tercero**, **Centro de costo** o ambos valores en la misma cuenta. Cada marca exige su dato de forma independiente en el comprobante. |
| 3 | La marca vive en la cuenta del PUC del año fiscal correspondiente, aunque los terceros sean globales. |

**Criterio de uso:** se marca **Tercero** en las cuentas donde importa identificar con quién se hizo la operación: clientes, proveedores, empleados, cuentas por cobrar, cuentas por pagar e impuestos. Es lo que permite obtener después el detalle por tercero.

**Captura en el comprobante:** al registrar un comprobante en `Contabilidad > Comprobantes`, la tabla **Cuentas del asiento** incluye la columna **Tercero**. Cuando la cuenta de la línea está marcada con **Solicitar > Tercero**, esa celda se habilita y despliega la lista de terceros de la empresa, con un campo de búsqueda para filtrarla. En las líneas cuya cuenta no exige el dato, la celda muestra el texto **No requerido** y no admite valor. Si la celda exige el dato y se deja vacía, el comprobante no se puede guardar.

## Uso del tercero en los reportes

El tercero capturado en los comprobantes es lo que permite analizar la información por contraparte.

**Filtrado de reportes:** los reportes contables permiten acotar la consulta a un tercero mediante el campo **Filtrado por**, cuyo valor predeterminado es **No aplica**. Al seleccionar un tercero, el reporte se limita a los movimientos registrados con esa contraparte.

**Detalle por tercero:** el Libro Auxiliar incluye la columna **Tercero** en el detalle de los movimientos, de modo que cada línea muestra con quién se realizó la operación.

**Limitación:** los reportes solo pueden mostrar la información que se capturó al registrar cada comprobante. Los movimientos contabilizados antes de marcar la cuenta con **Solicitar > Tercero** no tienen tercero asignado y aparecerán sin identificar. Por esa razón conviene definir la exigencia en las cuentas al inicio del año fiscal.

## Solución de problemas

### El campo de documento o NIT aparece bloqueado al editar un tercero

Es el comportamiento esperado. **Tipo de identificación**, **NIT/Documento** y **DV** aparecen en gris en la ventana **Editar tercero** y no admiten cambios. Para modificarlos debe usarse `Contabilidad > Configuración > Especiales > Terceros > Actualizar documento`.

### El sistema no permite eliminar un tercero

Aparece el mensaje «No se puede eliminar el tercero porque está referenciado por comprobantes contables». El tercero tiene movimientos o asientos contables asociados y la plataforma bloquea su eliminación para proteger la trazabilidad del historial financiero. Si el tercero no debe seguir usándose, basta con no incluirlo en los comprobantes nuevos.

### Se eliminó un tercero por error

No se puede recuperar. La eliminación es permanente y la plataforma no ofrece ninguna acción para restaurar terceros eliminados, como lo advierte el diálogo de confirmación. El tercero debe volver a crearse con el botón **Nuevo**.

### El formulario exige la razón social

El tercero está clasificado como persona jurídica, y en ese caso la razón social es obligatoria. Si se trata de una persona natural, debe seleccionarse ese tipo de persona: el sistema pedirá nombres y apellidos y compondrá la razón social a partir de ellos.

### El formulario exige municipio, o país y ciudad

El sistema valida la ubicación según el origen del tercero: los nacionales requieren la selección del municipio y los extranjeros requieren el país y la ciudad. Debe verificarse que el tercero esté clasificado como corresponde.

### El nombre de una persona natural aparece mal escrito en los reportes

La razón social de las personas naturales la construye el sistema a partir de los nombres y apellidos registrados. La corrección se hace editando esos campos en la ficha del tercero; el cambio se refleja también en los movimientos ya registrados.

### El desplegable de terceros aparece vacío en el comprobante

La empresa no tiene terceros creados, o el criterio escrito en el campo de búsqueda del desplegable no coincide con ninguno. Los terceros se crean en `Contabilidad > Configuración > Terceros`.

### Un comprobante exige seleccionar un tercero

La cuenta utilizada en el movimiento tiene el valor **Tercero** en el campo **Solicitar** de su configuración en el PUC. Debe diligenciarse el dato o, si la exigencia no corresponde a esa cuenta, retirarse la marca desde `Contabilidad > Configuración > PUC`.

### La columna Tercero de una línea del comprobante muestra «No requerido»

La cuenta de esa línea no está marcada con **Solicitar > Tercero** en el PUC. Si el dato debe capturarse en esa cuenta, la marca se agrega desde `Contabilidad > Configuración > PUC`.

### No aparecen los terceros al cambiar de año fiscal

Los terceros son globales de la empresa y no dependen del año fiscal, de modo que no se pierden al abrir un año nuevo. Si un tercero no aparece, no está creado en la empresa.

### La importación de Excel reporta filas fallidas

El resumen de la carga incluye el detalle de errores por fila, con el número de fila y el motivo del rechazo. Deben corregirse esas filas en el archivo y volver a cargarlo. Como la importación actualiza los documentos que ya existen, el archivo puede cargarse completo sin duplicar los terceros creados en el intento anterior.

### La importación no procesa el archivo

Debe verificarse que el archivo esté en formato `.xlsx`, que se haya usado la plantilla oficial sin alterar sus columnas, que las celdas no contengan fórmulas y que el archivo esté dentro de los límites de filas y de tamaño admitidos.

### La importación modificó terceros que ya existían

Es el comportamiento esperado. La importación crea el tercero cuando el documento no existe y lo actualiza cuando ya existe en la empresa. Para evitarlo, el archivo debe limitarse a los documentos que se desea crear o modificar.

### Se necesita saber quién modificó un tercero

Debe abrirse el **ícono de reloj** en las acciones de la fila del tercero, en `Contabilidad > Configuración > Terceros`. La ventana **Historial de cambios** muestra la fecha, el usuario, el evento, el campo modificado y sus valores **Antes** y **Después**.

### No se encuentra el historial de cambios en Acciones Especiales

El historial de un tercero no está en `Configuración > Especiales`: el panel **Terceros** de esa pantalla contiene únicamente la opción **Actualizar documento**. El historial se consulta desde el ícono de reloj de la fila, en la pantalla de Terceros.

## Resumen de reglas de negocio

| # | Regla |
| --- | --- |
| 1 | Un tercero es una persona natural o jurídica con la que la empresa tiene una relación económica: clientes, proveedores, empleados, entidades oficiales y demás participantes de las operaciones contables. |
| 2 | Los terceros son globales de la empresa y no dependen del año fiscal: se crean una vez y quedan disponibles para todos los años. |
| 3 | El documento es el dato que identifica de forma única a cada tercero dentro de la empresa. |
| 4 | Los terceros de tipo persona jurídica exigen el diligenciamiento obligatorio de la razón social. |
| 5 | Los terceros de tipo persona natural exigen como mínimo nombres y apellidos; el sistema construye internamente la razón social a partir de esos datos. |
| 6 | Los terceros nacionales exigen la selección del municipio. |
| 7 | Los terceros extranjeros exigen la especificación del país y la ciudad. |
| 8 | En la ventana **Editar tercero**, los campos **Tipo de identificación**, **NIT/Documento** y **DV** permanecen bloqueados, por seguridad e integridad de los datos. |
| 9 | El documento solo se modifica desde `Contabilidad > Configuración > Especiales > Terceros > Actualizar documento`, proceso que conserva la identidad y el historial del tercero y que permite cambiar también el tipo de identificación. |
| 10 | No se puede eliminar un tercero que tenga movimientos o asientos contables asociados, para proteger la trazabilidad y el historial financiero. La plataforma responde con el mensaje «No se puede eliminar el tercero porque está referenciado por comprobantes contables». |
| 11 | Solo se pueden eliminar los terceros que aún no han participado en ningún movimiento contable. |
| 11.1 | La eliminación es permanente: no existe una acción para restaurar un tercero eliminado. |
| 12 | La importación masiva se realiza desde un archivo `.xlsx` construido sobre la plantilla que entrega **Importar > Descargar plantilla**, sin fórmulas y dentro de los límites de filas y tamaño establecidos. |
| 13 | La importación procesa cada fila por su documento: si no existe en la empresa crea el tercero, y si ya existe lo actualiza. La plataforma advierte de esta lógica antes de permitir seleccionar el archivo. |
| 14 | Al finalizar la importación, la plataforma muestra el resumen de registros procesados, creados, actualizados y fallidos, con el detalle de errores por fila. |
| 15 | El historial de cambios de cada tercero se consulta desde el ícono de reloj de su fila, y registra fecha, usuario, evento, campo modificado y sus valores **Antes** y **Después**. |
| 15.1 | Cada modificación genera una fila por campo alterado. |
| 16 | La exigencia del tercero en los comprobantes se activa desde el campo **Solicitar** de las cuentas del PUC, disponible solo en cuentas auxiliares. |
| 17 | En el comprobante, el tercero se captura en la columna **Tercero** de la tabla **Cuentas del asiento**. En las líneas cuya cuenta no lo exige, la celda muestra **No requerido**. |
| 18 | Los movimientos quedan asociados al tercero por su identificador interno; al corregir su nombre o razón social, el cambio se refleja también en los movimientos ya registrados. |
| 19 | Los reportes contables permiten filtrar por tercero, pero solo reflejan la información capturada al registrar cada comprobante. |
| 20 | La pantalla de Terceros permite exportar el listado completo a Excel con el botón **Descargar**, distinto del botón **Importar**. |
| 21 | **Tipo de tercero** (Cliente, Proveedor u Otro) y **Tipo de persona** (natural o jurídica) son campos distintos: el primero describe la relación comercial y el segundo determina las validaciones de nombre. |

## Preguntas frecuentes

**¿Qué es un tercero en Zoe?**
Es una persona natural o jurídica con la que la empresa tiene una relación económica y que se identifica en sus registros contables: clientes, proveedores, empleados, entidades oficiales y demás participantes de las operaciones.

**¿Dónde se administran los terceros?**
En `Contabilidad > Configuración > Terceros`.

**¿Hay que volver a crear los terceros cada año fiscal?**
No. Los terceros son globales de la empresa y quedan disponibles para todos los años fiscales, a diferencia del PUC y de los centros de costo.

**¿Qué diferencia hay entre una persona natural y una persona jurídica al crear un tercero?**
La persona jurídica exige diligenciar la razón social. La persona natural exige como mínimo nombres y apellidos, y con ellos el sistema construye internamente la razón social.

**¿Por qué el formulario no pide la razón social de una persona natural?**
Porque la compone el sistema a partir de los nombres y apellidos que se diligencian. Es el nombre con el que ese tercero aparecerá en los listados, los comprobantes y los reportes.

**¿Qué datos de ubicación se exigen?**
Los terceros nacionales requieren la selección del municipio. Los terceros extranjeros requieren la especificación del país y la ciudad.

**¿Por qué no se puede editar el NIT o el documento de un tercero?**
Porque **Tipo de identificación**, **NIT/Documento** y **DV** permanecen bloqueados en la ventana **Editar tercero**, por seguridad e integridad de los datos: el documento es la llave con la que se identifica al tercero y con la que se enlazan sus movimientos contables.

**¿Cómo se cambia entonces el documento de un tercero?**
Mediante el procedimiento especial en `Contabilidad > Configuración > Especiales > Terceros > Actualizar documento`.

**¿Se pierde el historial del tercero al actualizar su documento?**
No. El proceso conserva la identidad y el historial del tercero: los movimientos ya registrados siguen enlazados al mismo registro, ahora identificado con el documento corregido.

**¿Por qué no se puede eliminar un tercero?**
Porque tiene movimientos o asientos contables asociados. La plataforma lo impide para proteger la trazabilidad y el historial financiero: eliminarlo dejaría movimientos registrados sin contraparte identificable.

**¿Qué terceros sí se pueden eliminar?**
Los que todavía no han participado en ningún movimiento contable, como un registro creado por error o un duplicado detectado antes de usarlo.

**¿Qué se hace con un tercero que ya no se usa y no se puede eliminar?**
Dejar de incluirlo en los comprobantes nuevos. Su historial permanece disponible para consulta y para los reportes de los períodos en los que participó.

**¿Cómo se cargan varios terceros a la vez?**
Con la importación masiva: botón **Importar > Subir desde plantilla** en la pantalla de Terceros, cargando un archivo de Excel construido sobre la plantilla oficial.

**¿De dónde se descarga la plantilla de importación?**
Del mismo botón **Importar**, en la opción **Descargar plantilla**.

**¿Qué pasa si en el archivo de importación hay documentos que ya existen?**
El proceso los actualiza con los datos del archivo. Solo crea terceros cuando el documento no existe en la empresa.

**¿Se puede volver a cargar el mismo archivo sin duplicar terceros?**
Sí. La importación identifica cada fila por su documento: los que ya existen se actualizan en lugar de duplicarse.

**¿Qué requisitos debe cumplir el archivo de importación?**
Debe estar en formato `.xlsx`, usar la plantilla oficial sin alterar sus columnas, no contener fórmulas y respetar los límites de filas y de tamaño establecidos.

**¿Qué información muestra la plataforma al terminar la importación?**
Un resumen con los registros procesados, creados, actualizados y fallidos, además del detalle de los errores por fila.

**¿Qué se hace si algunas filas quedaron fallidas?**
Revisar el detalle de errores por fila, corregir esas filas en el archivo y volver a cargarlo.

**¿Se puede saber quién modificó un tercero?**
Sí. Cada tercero tiene su propio historial de cambios, que registra la fecha, el usuario, el evento, el campo modificado y sus valores **Antes** y **Después**.

**¿Dónde se consulta el historial de cambios de un tercero?**
En el ícono de reloj de las acciones de la fila, en `Contabilidad > Configuración > Terceros`. Abre la ventana **Historial de cambios**. No se consulta desde Acciones Especiales.

**¿Se puede recuperar un tercero eliminado?**
No. La eliminación es permanente y la plataforma no ofrece ninguna acción para restaurarlo. Hay que crearlo de nuevo.

**¿Cuál es la diferencia entre Tipo de tercero y Tipo de persona?**
**Tipo de tercero** indica la relación comercial (Cliente, Proveedor u Otro) y es la etiqueta que se ve en el listado. **Tipo de persona** indica si es persona natural o jurídica y determina qué campos de nombre exige el formulario.

**¿Cómo se exporta el listado de terceros a Excel?**
Con el botón **Descargar** de la pantalla de Terceros, que es distinto del botón **Importar**.

**¿Cómo se hace que el comprobante exija el tercero?**
Marcando la cuenta contable con el valor **Tercero** en el campo **Solicitar**, desde `Contabilidad > Configuración > PUC`. El campo solo aparece en cuentas auxiliares.

**¿Se puede exigir tercero y centro de costo en la misma cuenta?**
Sí. El campo **Solicitar** admite **Tercero**, **Centro de costo** o ambos valores. Si la cuenta tiene los dos, la línea del comprobante exigirá los dos datos.

**¿Qué significa «No requerido» en la columna Tercero de un comprobante?**
Que la cuenta de esa línea no está marcada con **Solicitar > Tercero**, por lo que la plataforma no pide el dato.

**¿Por qué el reporte por tercero aparece incompleto?**
Porque los reportes solo reflejan la información capturada al registrar cada comprobante. Los movimientos contabilizados antes de marcar la cuenta con **Solicitar > Tercero** no tienen el dato asignado.

**¿Un mismo tercero puede ser cliente y proveedor?**
Sí. El registro del tercero es uno solo, identificado por su documento, y son los movimientos contables los que determinan en qué condición participa en cada operación.
