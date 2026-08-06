# Mapa de la aplicación

## Página 1 - Inicio

Descripción:
Pantalla principal del sistema donde el usuario selecciona la empresa con la que trabajará y accede a las opciones de administración.


### Arbol Jerárquico

- Administacíon
  - Inicio
  - Mis Empresas
  - Control de acceso
      - Usuarios
      - Roles y permisos


## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Inicio | Selección de Empresa | Muestra las empresas disponibles para que el usuario seleccione con cuál desea trabajar. |
| Inicio | Tarjeta de Empresa | Presenta la información básica de una empresa (nombre, NIT y país) y permite ingresar a ella. |
| Inicio | Crear Empresa | Permite registrar una nueva empresa dentro del sistema. |
| Administración | Inicio | Redirige a la pantalla principal del sistema. |
| Administración | Mis Empresas | Permite administrar las empresas registradas por el usuario. |
| Control de acceso | Usuarios | Permite crear, editar, consultar o desactivar usuarios del sistema. |
| Control de acceso | Roles y permisos | Permite administrar los roles y definir los permisos asignados a cada uno. |


# Página 2 - Inicio Contabilidad


**Descripción:** Pantalla principal del módulo de Contabilidad. Permite acceder a los diferentes módulos contables de la empresa y visualizar novedades, accesos rápidos e información general.

## Árbol Jerárquico

- Contabilidad
  - Inicio
  - Configuración
    - PUC
    - Tipos de documentos
    - Centros de costos
    - Terceros
    - Anexos
    - Especiales
  - Comprobantes
  - Reportes
  - Exógena
    - Formatos
    - Previsualizar

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Inicio | Tarjeta de soporte | Permite contactar al equipo de soporte mediante un acceso rápido. |
| Inicio | Alternativas del Sistema | Presenta accesos directos a los principales módulos del sistema contable. |
| Inicio | PUC - Plan Único de Cuentas | Permite acceder a la gestión del plan único de cuentas. |
| Inicio | Tipos de documentos | Permite acceder a la configuración de los tipos de documentos contables. |
| Inicio | Centros de costos | Permite administrar los centros de costos de la empresa. |
| Inicio | Terceros | Permite administrar clientes, proveedores y demás terceros registrados. |
| Inicio | Anexos | Permite administrar la información complementaria utilizada en los procesos contables. |
| Inicio | Opciones Especiales | Permite acceder a funcionalidades especiales del sistema contable. |
| Inicio | Comprobantes | Permite acceder a la gestión de comprobantes contables. |
| Inicio | Reportes | Permite acceder a los reportes contables disponibles. |
| Inicio | Formatos Exógena | Permite acceder a la generación de formatos para información exógena. |
| Inicio | Información Exógena | Permite acceder a la administración de la información exógena. |
| Inicio | Novedades y Actualizaciones | Muestra las novedades, mejoras y cambios recientes del sistema. |


# Página 3 - Plan Único de Cuentas (PUC)

**Descripción:** Permite consultar y administrar el Plan Único de Cuentas (PUC) de la empresa mediante una estructura jerárquica de cuentas contables.

## Árbol Jerárquico

- Contabilidad
  - Configuración
    - PUC

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Configuración | Campo de búsqueda | Permite buscar cuentas contables por nombre o código. |
| Configuración | Botón de exportación | Permite exportar la información del Plan Único de Cuentas. |
| Configuración | Árbol del PUC | Presenta la estructura jerárquica de las cuentas contables registradas. |
| Configuración | Control de expansión | Permite desplegar o contraer los niveles del árbol de cuentas. |


# Página 4 - Tipos de Documento

**Descripción:** Permite administrar los tipos de documentos contables utilizados por la empresa para registrar las diferentes operaciones contables.

## Árbol Jerárquico

- Contabilidad
  - Configuración
    - Tipos de Documento

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Configuración | Campo de búsqueda | Permite buscar tipos de documento registrados. |
| Configuración | Botón Filtrar | Ejecuta la búsqueda según el criterio ingresado. |
| Configuración | Opción "Ver Tipos API" | Permite visualizar los tipos de documento disponibles desde la integración API. |
| Configuración | Tabla de tipos de documento | Presenta el listado de tipos de documento registrados en el sistema. |
| Configuración | Botón Nuevo | Permite registrar un nuevo tipo de documento. |
| Configuración | Selector de columnas | Permite mostrar u ocultar columnas de la tabla. |
| Configuración | Acciones de registro | Permite editar o eliminar un tipo de documento existente. |
| Configuración | Paginación | Permite navegar entre las diferentes páginas del listado. |
| Configuración | Selector de registros por página | Permite definir la cantidad de registros que se visualizarán por página. |


# Página 5 - Centros de Costos

**Descripción:** Permite administrar los centros de costos de la empresa, los cuales se utilizan para clasificar y controlar los costos asociados a las diferentes áreas o procesos.

## Árbol Jerárquico

- Contabilidad
  - Configuración
    - Centros de Costos

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Configuración | Campo de búsqueda | Permite buscar centros de costos registrados. |
| Configuración | Botón Filtrar | Ejecuta la búsqueda según el criterio ingresado. |
| Configuración | Tabla de centros de costos | Presenta el listado de centros de costos registrados en el sistema. |
| Configuración | Botón Nuevo | Permite registrar un nuevo centro de costos. |
| Configuración | Selector de columnas | Permite mostrar u ocultar columnas de la tabla. |
| Configuración | Acciones de registro | Permite editar o eliminar un centro de costos existente. |
| Configuración | Paginación | Permite navegar entre las diferentes páginas del listado. |
| Configuración | Selector de registros por página | Permite definir la cantidad de registros que se visualizarán por página. |


# Página 6 - Terceros

**Descripción:** Permite administrar los terceros registrados en la empresa, como clientes, proveedores, empleados y demás personas o entidades relacionadas con las operaciones contables.

## Árbol Jerárquico

- Contabilidad
  - Configuración
    - Terceros

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Configuración | Campo de búsqueda | Permite buscar terceros registrados mediante un criterio de búsqueda. |
| Configuración | Botón Filtrar | Ejecuta la búsqueda según el criterio ingresado. |
| Configuración | Tabla de terceros | Presenta el listado de terceros registrados en el sistema con su información principal. |
| Configuración | Botón Nuevo | Permite registrar un nuevo tercero. |
| Configuración | Selector de columnas | Permite mostrar u ocultar columnas de la tabla. |
| Configuración | Acciones de registro | Permite editar, restaurar o eliminar un tercero registrado. |
| Configuración | Paginación | Permite navegar entre las diferentes páginas del listado. |
| Configuración | Selector de registros por página | Permite definir la cantidad de registros que se visualizarán por página. |


# Página 7 - Anexos

**Descripción:** Permite administrar los anexos contables utilizados por la empresa para complementar la configuración y asociación de información dentro del sistema.

## Árbol Jerárquico

- Contabilidad
  - Configuración
    - Anexos

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Configuración | Campo de búsqueda | Permite buscar anexos registrados mediante un criterio de búsqueda. |
| Configuración | Botón Filtrar | Ejecuta la búsqueda según el criterio ingresado. |
| Configuración | Tabla de anexos | Presenta el listado de anexos registrados en el sistema. |
| Configuración | Botón Nuevo | Permite registrar un nuevo anexo. |
| Configuración | Botón Copiar | Permite duplicar o copiar la configuración de un anexo existente. |
| Configuración | Selector de columnas | Permite mostrar u ocultar columnas de la tabla. |
| Configuración | Acciones de registro | Permite editar o eliminar un anexo registrado. |
| Configuración | Paginación | Permite navegar entre las diferentes páginas del listado. |
| Configuración | Selector de registros por página | Permite definir la cantidad de registros que se visualizarán por página. |


# Página 8 - Acciones Especiales

**Descripción:** Permite acceder a procesos especiales relacionados con la administración contable, como la gestión de períodos fiscales, saldos iniciales, cierre contable y otras operaciones de mantenimiento del sistema.

## Árbol Jerárquico

- Contabilidad
  - Configuración
    - Especiales

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Configuración | Panel de Períodos | Agrupa las opciones relacionadas con la administración de años fiscales y períodos contables. |
| Configuración | Panel de Comprobantes | Agrupa las opciones especiales para la administración de comprobantes y procesos contables. |
| Configuración | Panel de Terceros | Contiene opciones especiales relacionadas con la gestión de terceros. |
| Configuración | Opción Agregar año fiscal | Permite crear un nuevo año fiscal en el sistema. |
| Configuración | Opción Quitar año fiscal | Permite eliminar un año fiscal existente. |
| Configuración | Opción Gestionar períodos contables | Permite administrar los períodos contables de un año fiscal. |
| Configuración | Opción Historial | Permite consultar el historial de procesos realizados. |
| Configuración | Opción Saldos iniciales | Permite gestionar los saldos iniciales de las cuentas contables. |
| Configuración | Opción Cierre anual | Permite ejecutar el proceso de cierre contable del año fiscal. |
| Configuración | Opción Comprobantes en proceso | Permite consultar los comprobantes que aún no han sido finalizados. |
| Configuración | Opción Mover saldos finales a iniciales | Permite trasladar los saldos finales de un período como saldos iniciales del siguiente. |
| Configuración | Opción Activar/Desactivar edición de comprobantes | Permite habilitar o restringir la edición de comprobantes contables. |
| Configuración | Opción Mover saldos entre cuentas | Permite trasladar saldos de una cuenta contable a otra. |
| Configuración | Opción Auditoría de operación | Permite consultar el registro de operaciones realizadas en el sistema. |
| Configuración | Opción Actualizar documento | Permite actualizar la información documental de los terceros. |
| Configuración | Botón de información | Muestra información o ayuda sobre cada proceso especial. |


# Página 9 - Comprobantes

**Descripción:** Permite consultar, administrar y gestionar los comprobantes contables registrados en la empresa.

## Árbol Jerárquico

- Contabilidad
  - Comprobantes

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Comprobantes | Campo de búsqueda | Permite buscar comprobantes registrados mediante un criterio de búsqueda. |
| Comprobantes | Botón Filtrar | Ejecuta la búsqueda según el criterio ingresado. |
| Comprobantes | Búsqueda avanzada | Permite aplicar filtros adicionales para localizar comprobantes específicos. |
| Comprobantes | Botón Actualizar | Recarga la información del listado de comprobantes. |
| Comprobantes | Tabla de comprobantes | Presenta el listado de comprobantes registrados con su información principal. |
| Comprobantes | Botón Nuevo | Permite crear un nuevo comprobante contable. |
| Comprobantes | Selector de columnas | Permite mostrar u ocultar columnas de la tabla. |
| Comprobantes | Acciones de registro | Permite visualizar, descargar o ejecutar acciones sobre un comprobante según su estado. |
| Comprobantes | Paginación | Permite navegar entre las diferentes páginas del listado. |
| Comprobantes | Selector de registros por página | Permite definir la cantidad de registros que se visualizarán por página. |


# Página 10 - Reportes Financieros

**Descripción:** Permite generar y exportar los diferentes reportes financieros, auxiliares, anexos y certificados disponibles en el sistema.

## Árbol Jerárquico

- Contabilidad
  - Reportes

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Reportes | Mensaje informativo | Muestra una indicación sobre el proceso de filtrado y generación de reportes. |
| Reportes | Panel de Balances | Agrupa los reportes financieros relacionados con balances de la empresa. |
| Reportes | Panel de Auxiliares | Agrupa los reportes auxiliares disponibles para consulta. |
| Reportes | Panel de Anexos | Agrupa los reportes relacionados con anexos contables. |
| Reportes | Panel de Certificados | Agrupa los certificados disponibles para generar y exportar. |
| Reportes | Mayor y Balance | Permite generar el reporte de Mayor y Balance en los formatos disponibles. |
| Reportes | Balance de Comprobación | Permite generar el Balance de Comprobación. |
| Reportes | Balance de Comprobación Agrupado | Permite generar el Balance de Comprobación Agrupado. |
| Reportes | Estado de Resultados | Permite generar el Estado de Resultados. |
| Reportes | Caja Diario | Permite generar el reporte de Caja Diario. |
| Reportes | Estado de Situación Financiera | Permite generar el Estado de Situación Financiera. |
| Reportes | Libro Auxiliar | Permite generar el Libro Auxiliar. |
| Reportes | Reporte de Anexos | Permite generar el reporte de anexos registrados. |
| Reportes | Configuración de Anexos | Permite generar el reporte de configuración de anexos. |
| Reportes | Certificado de Retenciones | Permite generar el certificado de retenciones. |
| Reportes | Botón de descarga | Permite descargar el reporte seleccionado en el formato disponible. |


# Página 11 - Formatos Exógenos

**Descripción:** Permite administrar la asignación de cuentas contables a los formatos de información exógena requeridos para la generación de reportes fiscales.

## Árbol Jerárquico

- Contabilidad
  - Exógena
    - Formatos

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Exógena | Listado de formatos exógenos | Presenta los formatos de información exógena disponibles para su configuración. |
| Exógena | Tarjeta de formato | Muestra el código y la descripción de cada formato exógeno. |
| Exógena | Botón Editar | Permite configurar la asignación de cuentas contables para el formato seleccionado. |


# Página 12 - Información Exógena

**Descripción:** Permite generar y consultar la información exógena a partir de los formatos y conceptos previamente configurados para la elaboración de reportes fiscales.

## Árbol Jerárquico

- Contabilidad
  - Exógena
    - Información Exógena

## Componentes

| Menú | Componente | Descripción |
|------|------------|-------------|
| Exógena | Selector de formato | Permite seleccionar el formato de información exógena que se utilizará para la generación del documento. |
| Exógena | Selector de concepto | Permite seleccionar el concepto asociado al formato previamente elegido. |
| Exógena | Botón Generar Documento | Genera el documento de información exógena según el formato y concepto seleccionados. |
| Exógena | Panel de información exógena | Muestra la información correspondiente al formato y concepto seleccionados. |
| Exógena | Panel de formatos y conceptos | Presenta la relación entre formatos, conceptos y cuentas asociadas para su consulta. |


# Glosario

| Término | Definición | Ubicación en la APP |
|---------|------------|---------------------|
| Plan Único de Cuentas (PUC) | Catálogo organizado de todas las cuentas contables que una empresa utiliza para registrar sus operaciones financieras. Cada cuenta tiene un código y una descripción. | Contabilidad / Configuración / PUC |
| Centro de Costos | Unidad o área de la empresa donde se asignan y controlan los costos (por ejemplo: Producción, Ventas o Administración). | Contabilidad / Configuración / Centros de Costo |
| Formatos Exógena | Archivos o reportes exigidos por la autoridad tributaria (como la DIAN en Colombia) para reportar información financiera y tributaria. | Contabilidad / Exógena / Formatos |
| Terceros | Personas naturales o jurídicas con las que la empresa tiene relación comercial, como clientes, proveedores, empleados o entidades gubernamentales. | Contabilidad / Configuración / Terceros |
| Información Exógena | Conjunto de datos financieros y tributarios que una empresa debe reportar periódicamente a la DIAN. | Contabilidad / Exógena / Información Exógena |
| Activo | Bienes, derechos y recursos que posee una empresa y que tienen valor económico. | Contabilidad / Configuración / PUC |
| Disponible | Parte del activo compuesta por dinero en caja, bancos y otros recursos de disponibilidad inmediata. | Contabilidad / Configuración / PUC |
| Intangibles | Activos sin existencia física que generan valor para la empresa, como licencias de software, patentes o marcas. | Contabilidad / Configuración / PUC |
| Diferidos | Gastos pagados por anticipado cuyo beneficio se obtiene en varios períodos contables. | Contabilidad / Configuración / PUC |
| Valorizaciones | Incremento del valor de un activo respecto a su valor registrado inicialmente. | Contabilidad / Configuración / PUC |
| Pasivo | Obligaciones o deudas que la empresa tiene con terceros y que deberá pagar en el futuro. | Contabilidad / Configuración / PUC |
| Impuestos, Gravámenes y Tasas | Obligaciones tributarias que la empresa debe pagar al Estado, como IVA, retención en la fuente o impuesto de renta. | Contabilidad / Configuración / PUC |
| Pasivos Estimados y Provisiones | Obligaciones cuyo valor o fecha de pago aún no se conocen con exactitud, pero que se estiman para reflejar la realidad financiera. | Contabilidad / Configuración / PUC |
| Patrimonio | Valor que pertenece a los propietarios de la empresa, calculado como Activos menos Pasivos. | Contabilidad / Configuración / PUC |
| Capital | Recursos aportados por los socios o propietarios para iniciar o fortalecer la empresa. | Contabilidad / Configuración / PUC |
| Reservas | Parte de las utilidades retenidas para cumplir obligaciones legales o cubrir necesidades futuras. | Contabilidad / Configuración / PUC |
| Reservas Obligatorias | Reservas exigidas por la ley para proteger el patrimonio de la empresa. | Contabilidad / Configuración / PUC |
| Reservas Ocasionales | Reservas creadas voluntariamente por decisión de los socios para un fin específico. | Contabilidad / Configuración / PUC |
| Revalorización del Patrimonio | Ajuste del patrimonio para reflejar cambios en el valor económico de los recursos de la empresa. | Contabilidad / Configuración / PUC |
| Resultados del Ejercicio | Utilidad o pérdida obtenida por la empresa durante un período contable. | Contabilidad / Configuración / PUC |
| Utilidades Acumuladas | Ganancias obtenidas en años anteriores que no han sido distribuidas entre los socios. | Contabilidad / Configuración / PUC |
| Pérdidas Acumuladas | Pérdidas de ejercicios anteriores que aún no han sido compensadas. | Contabilidad / Configuración / PUC |
| Superávit por Valorizaciones | Incremento patrimonial generado por la valorización de activos, sin que represente una ganancia realizada. | Contabilidad / Configuración / PUC |
| Ingreso | Recursos que recibe la empresa por la venta de bienes o prestación de servicios. | Contabilidad / Configuración / PUC |
| Gastos | Consumos o desembolsos necesarios para el funcionamiento de la empresa, como servicios públicos o arriendos. | Contabilidad / Configuración / PUC |
| Costos | Recursos utilizados directamente para producir bienes o prestar servicios. | Contabilidad / Configuración / PUC |
| Costos de Producción o de Operación | Conjunto de costos necesarios para fabricar un producto o prestar un servicio. | Contabilidad / Configuración / PUC |
| Mano de Obra Directa | Salarios y prestaciones del personal que participa directamente en la producción de bienes o servicios. | Contabilidad / Configuración / PUC |
| Costos Indirectos | Costos necesarios para la producción que no pueden asociarse directamente a un producto específico, como energía o supervisión. | Contabilidad / Configuración / PUC |
| Documentos Contables | Soportes físicos o electrónicos que respaldan las transacciones registradas en la contabilidad. | Contabilidad / Configuración / Tipos de Documento |
| Documentos Contables Internos | Documentos generados por la propia empresa para registrar operaciones internas, como comprobantes contables. | Contabilidad / Configuración / Tipos de Documento |
| Documentos Contables Externos | Documentos emitidos por terceros, como facturas de proveedores o recibos bancarios. | Contabilidad / Configuración / Tipos de Documento |
| Nómina | Registro de salarios, prestaciones, deducciones y pagos realizados a los empleados. | Contabilidad / Configuración / PUC |
| Nota Crédito de Factura de Compra | Documento que disminuye el valor de una factura de compra debido a devoluciones, descuentos o correcciones. | Contabilidad / Configuración / Tipos de Documento |
| Nota Débito de Factura de Compra | Documento que incrementa el valor de una factura de compra por ajustes o cargos adicionales. | Contabilidad / Configuración / Tipos de Documento |
| Nota de Contabilidad | Documento utilizado para registrar ajustes contables que no provienen de una factura o comprobante externo. | Contabilidad / Configuración / Tipos de Documento |
| Comprobante de Ingreso | Documento que registra la entrada de dinero a la empresa. | Contabilidad / Configuración / Tipos de Documento |
| Comprobante de Egreso | Documento que registra la salida de dinero por pagos realizados. | Contabilidad / Configuración / Tipos de Documento |
| Conciliación Bancaria | Proceso de comparar los movimientos registrados por la empresa con el extracto del banco para identificar diferencias. | Contabilidad / Configuración / Tipos de Documento |
| Notas Bancarias | Registros de ajustes relacionados con movimientos bancarios no registrados previamente o con diferencias encontradas en la conciliación. | Contabilidad / Configuración / Tipos de Documento |
| Gastos Diversos | Gastos operativos que no pertenecen a una categoría específica. | Contabilidad / Configuración / PUC |
| Gastos de Nómina | Gastos relacionados con salarios, prestaciones sociales, seguridad social y demás obligaciones laborales. | Contabilidad / Configuración / PUC |
| Provisión de Impuestos | Registro contable que estima el valor de los impuestos que la empresa deberá pagar en el futuro. | Contabilidad / Configuración / PUC |
| Tipo de Tercero | Clasificación de un tercero según su relación con la empresa, como cliente, proveedor, empleado o entidad oficial. | Contabilidad / Configuración / Terceros |
| Año Fiscal | Período anual sobre el cual se calculan impuestos y se presentan los estados financieros. | Contabilidad / Configuración / Especiales |
| Períodos Contables | Divisiones del año fiscal (mensuales, trimestrales o anuales) utilizadas para registrar y analizar la información financiera. | Contabilidad / Configuración / Especiales |
| Saldos Iniciales | Valores con los que comienzan las cuentas contables al iniciar un nuevo período o al implementar el sistema. | Contabilidad / Configuración / Especiales |
| Cierre Anual | Proceso contable mediante el cual se finaliza un año fiscal, se calculan resultados y se preparan los estados financieros. | Contabilidad / Configuración / Especiales |
| Comprobante de Pago | Documento que certifica que un pago fue realizado y registrado. | Contabilidad / Comprobantes |
| Mayor Balance | Reporte que muestra el movimiento y saldo de cada cuenta del libro mayor durante un período. | Contabilidad / Reportes |
| Balance de Comprobación | Informe que presenta los saldos débito y crédito de todas las cuentas para verificar que la contabilidad esté cuadrada. | Contabilidad / Reportes |
| Balance de Comprobación Agrupado | Versión resumida del balance de comprobación donde las cuentas se presentan agrupadas por categorías. | Contabilidad / Reportes |
| Caja Diario | Reporte que registra cronológicamente todos los ingresos y egresos de efectivo de la empresa. | Contabilidad / Reportes |
| Estado de Situación Financiera | Estado financiero que muestra los activos, pasivos y patrimonio de la empresa en una fecha determinada. También se conoce como Balance General. | Contabilidad / Reportes |
| Libro Auxiliar | Reporte detallado de los movimientos registrados en una cuenta contable específica. | Contabilidad / Reportes |