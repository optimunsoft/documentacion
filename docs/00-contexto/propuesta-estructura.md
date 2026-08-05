# Propuesta de Estructura de Documentación

## Objetivo

Definir una estructura de documentación clara, escalable y fácil de mantener que permita utilizar los mismos archivos Markdown tanto para el Centro de Ayuda dirigido a los usuarios como para la ingesta de información del sistema RAG de la IA de soporte.

La propuesta busca facilitar la navegación, mejorar la reutilización del contenido y optimizar la recuperación de información por parte de la inteligencia artificial.

---

# Árbol de Carpetas Propuesto

```text
docs/
│
├── README.md
│
├── 00-contexto/
│   ├── benchmark-documentacion.md
│   ├── mapa-app-y-glosario.md
│   └── propuesta-estructura.md
│
├── 01-primeros-pasos/
│   ├── introduccion.md
│   ├── iniciar-sesion.md
│   ├── recuperar-contrasena.md
│   └── configuracion-inicial.md
│
├── 02-administracion/
│   ├── inicio-administracion.md
│   ├── empresas.md
│   ├── usuarios.md
│   ├── roles-y-permisos.md
│   └── activos/
│       ├── usuarios-img-01.png
│       ├── usuarios-img-02.png
│       └── roles-demo.gif
│
├── 03-contabilidad/
│   ├── inicio-contabilidad.md
│   │
│   ├── configuracion/
│   │   ├── plan-unico-de-cuentas.md
│   │   ├── centros-de-costos.md
│   │   ├── terceros.md
│   │   ├── anexos.md
│   │   ├── tipos-de-documento.md
│   │   └── acciones-especiales.md
│   │
│   ├── comprobantes/
│   │   ├── crear-comprobante.md
│   │   ├── editar-comprobante.md
│   │   ├── eliminar-comprobante.md
│   │   └── consultar-comprobante.md
│   │
│   ├── reportes/
│   │   ├── balance-general.md
│   │   ├── estado-de-resultados.md
│   │   ├── libro-mayor.md
│   │   └── auxiliares.md
│   │
│   ├── exogena/
│   │   ├── formatos-exogenos.md
│   │   └── informacion-exogena.md
│   │
│   └── assets/
│       ├── crear-comprobante-img-01.png
│       ├── crear-comprobante-img-02.png
│       ├── comprobante-demo.gif
│       └── reportes-img-01.png
│
├── 04-faq/
│   ├── preguntas-frecuentes.md
│   ├── errores-comunes.md
│   └── solucion-problemas.md
│
├── 05-glosario/
│   └── glosario.md
│
└── templates/
    ├── articulo-base.md
    ├── procedimiento.md
    └── faq.md
```

---

# Organización de los Artículos

Se propone que cada archivo Markdown documente un único tema o procedimiento específico.

Cada artículo debe contener únicamente la información relacionada con una funcionalidad del sistema, evitando combinar varios procesos dentro de un mismo documento.

Esta organización facilita:

- La navegación para el usuario.
- El mantenimiento de la documentación.
- La reutilización del contenido.
- La recuperación precisa de información por parte del sistema RAG.

---

# Estructura Recomendada para cada Artículo

Todos los artículos deberían mantener una estructura uniforme.

```markdown
# Título

## Descripción

Breve explicación del proceso.

## Requisitos previos

## Paso a paso

1.
2.
3.

## Resultado esperado

## Errores frecuentes

## Recursos relacionados
```

Mantener una estructura consistente mejora la experiencia de navegación y facilita el procesamiento automático de la documentación.

---

# Convención de Nombres

## Archivos Markdown

Se utilizará la convención **kebab-case**, escribiendo todos los nombres en minúsculas y separando las palabras mediante guiones.

### Reglas

- Utilizar únicamente letras minúsculas.
- Separar palabras con guion (-).
- No utilizar espacios.
- No utilizar caracteres especiales.
- No utilizar tildes.
- Cada archivo debe representar un único tema.

### Ejemplos

```
crear-comprobante.md

plan-unico-de-cuentas.md

centros-de-costos.md

configurar-terceros.md
```

---

# Convención para Assets

Las imágenes, GIF y demás recursos deberán ubicarse dentro de la carpeta **activos** correspondiente al módulo al que pertenecen.

Formato recomendado:

```
<articulo>-img-01.png

<articulo>-img-02.png

<articulo>-demo.gif

<articulo>-tabla.png
```

Ejemplos

```
crear-comprobante-img-01.png

crear-comprobante-img-02.png

crear-comprobante-demo.gif

roles-y-permisos-img-01.png
```

Esta nomenclatura facilita localizar rápidamente los recursos asociados a cada artículo y evita conflictos entre archivos con nombres similares.

---

# Beneficios para el Centro de Ayuda

La estructura propuesta permite:

- Organizar la documentación por módulos funcionales del sistema.
- Facilitar la navegación mediante categorías claras.
- Mantener una estructura uniforme entre todos los artículos.
- Mejorar el mantenimiento y actualización de la documentación.
- Favorecer la reutilización de contenido entre diferentes módulos.

---

# Beneficios para el Sistema RAG

La organización propuesta también optimiza el proceso de ingesta de información para la IA de soporte.

Los principales beneficios son:

- Cada archivo representa un único tema, reduciendo la ambigüedad durante la búsqueda.
- Los nombres de los archivos describen claramente el contenido.
- La documentación se encuentra organizada por módulos funcionales.
- Los recursos multimedia permanecen asociados a cada procedimiento.
- Se facilita la indexación y recuperación de información relevante.
- Se reduce la posibilidad de recuperar información de procesos no relacionados.

Esta organización mejora la precisión de las respuestas generadas por el sistema RAG y simplifica el mantenimiento futuro del repositorio documental.

---


# Propuesta de Estructura del Centro de Ayuda

Además de la organización del repositorio, se propone una estructura para la interfaz del Centro de Ayuda que facilite la navegación de los usuarios y permita acceder rápidamente a la documentación.

La propuesta toma como referencia las buenas prácticas identificadas en los centros de ayuda de Siigo, Alegra, Holded y Contoda.

## Página Principal

La página principal será el punto de entrada para todos los usuarios.

Contendrá los siguientes elementos:

- Buscador principal.
- Accesos rápidos a los módulos del sistema.
- Artículos más consultados.
- Novedades o actualizaciones recientes.
- Acceso a Preguntas Frecuentes.

### Estructura propuesta

```text
Centro de Ayuda
│
├── Buscador
│
├── Módulos
│   ├── Primeros pasos
│   ├── Administración
│   ├── Contabilidad
│   ├── Comprobantes
│   ├── Reportes
│   ├── Exógena
│   └── Preguntas Frecuentes
│
├── Artículos más consultados
│
└── Novedades
```

---

## Página de Categoría

Cada módulo mostrará únicamente los artículos correspondientes a esa categoría.

Ejemplo:

```text
Contabilidad

Configuración
Comprobantes
Reportes
Exógena

-----------------------------------

• Plan Único de Cuentas

• Centros de Costos

• Terceros

• Tipos de Documento

• Anexos

• Acciones Especiales
```

Esta organización permite localizar rápidamente la documentación relacionada con un proceso específico.

---

## Página de Artículo

Todos los artículos seguirán una estructura uniforme para ofrecer una experiencia consistente.

### Componentes

- Breadcrumb (Ruta de navegación)
- Título del artículo
- Descripción breve
- Tabla de contenido
- Procedimiento paso a paso
- Capturas de pantalla
- GIF o video (cuando aplique)
- Errores frecuentes
- Artículos relacionados
- Valoración del artículo

### Estructura propuesta

```text
Inicio

>

Contabilidad

>

Configuración

>

Plan Único de Cuentas

--------------------------------

Título

Descripción

--------------------------------

Tabla de contenido

1.

2.

3.

--------------------------------

Paso a paso

Imagen

GIF

--------------------------------

Errores frecuentes

--------------------------------

Artículos relacionados

--------------------------------

¿Te resultó útil este artículo?

👍 Sí      👎 No
```

---

## Justificación

La estructura propuesta busca combinar las mejores prácticas identificadas durante el benchmark:

- Buscador principal visible desde cualquier página.
- Navegación mediante módulos funcionales.
- Breadcrumb para indicar la ubicación del usuario.
- Tabla de contenido en artículos extensos.
- Recursos visuales (capturas, GIF y videos).
- Sección de errores frecuentes.
- Artículos relacionados.
- Sistema de valoración para obtener retroalimentación de los usuarios.

Con esta organización se mejora la experiencia del usuario final y se facilita la recuperación de información por parte del sistema RAG utilizado por la IA de soporte.

# Conclusión

La estructura propuesta está basada en las buenas prácticas identificadas durante el análisis de los centros de ayuda de diferentes plataformas SaaS, priorizando una organización modular, consistente y escalable.

El diseño permite utilizar una única fuente de documentación tanto para el Centro de Ayuda destinado a los usuarios como para la base de conocimiento utilizada por la IA de soporte, reduciendo la duplicidad de información y facilitando su mantenimiento a largo plazo.


