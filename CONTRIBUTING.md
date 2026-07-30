---

### 📄 `CONTRIBUTING.md`
```markdown
# 🛠️ Guía de Contribución y Flujo de Trabajo

Para mantener la calidad técnica e ir organizando el contenido de forma estándar para la IA, todos los commits y Pull Requests deben seguir las reglas descritas a continuación.

---

## 🔄 Flujo de Git (Gitflow Básico)

1. **`master` está protegida.** No se permiten commits directos a `master`. Todo cambio entra vía Pull Request (PR).
2. **Nomenclatura de ramas:**
   - Nuevas funcionalidades/documentos: `feature/DOC-ID-breve-descripcion` (ej. `feature/DOC-1-mapa-y-glosario`).
   - Correcciones: `fix/DOC-ID-breve-descripcion`.

3. **Mensajes de Commit (Conventional Commits):**
   - `docs: añade mapa general de la app`
   - `docs: actualiza glosario con terminos de facturacion`
   - `fix: corrige ortografia en propuesta de estructura`

---

## 🗂️ Convención de Nombres y Archivos

* **Nombres de archivos `.md`:** Utilizar siempre `kebab-case` en minúsculas.
  * ❌ `Mapa_App.md`, `GlosarioUI.md`
  * ✅ `mapa-app-y-glosario.md`, `crear-factura-venta.md`
* **Imágenes y Capturas (`docs/assets/img/`):**
  * Formato preferido: PNG o WebP.
  * Nombre: `modulo-pantalla-accion.png` (ej. `ventas-factura-crear-paso1.png`).
  * Todas las imágenes deben ser legibles y **no contener información confidencial real** de clientes de producción.

---

## 📋 Proceso de Revisión (Pull Request)

1. Una vez terminada la tarea en tu rama local, sube los cambios a GitHub.
2. Abre un **Pull Request hacia `master`**.
3. El PR cargará automáticamente la plantilla de revisión. Llénala con los datos correspondientes.
4. Vincula la tarea de Jira correspondiente en el PR.
5. Asigna el PR a revisión y mueve la tarjeta en Jira a la columna **En Review (PR)**.