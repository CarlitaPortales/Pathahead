# Publicar tu calculadora en GitHub Pages (gratis)

Todo se hace **desde el navegador**. No necesitas instalar nada ni saber programar.
Al final tendrás una URL pública (algo como `https://tuusuario.github.io/pathahead/`) que pegas en tu Substack y LinkedIn.

Tiempo estimado: **10-15 minutos.**

---

## Antes de empezar (2 minutos): pega tus 2 enlaces

El archivo `index.html` tiene dos líneas que debes completar para que funcione la captura de correos y el botón a tu Substack. Búscalas cerca del inicio del `<script>`:

```js
const SHEET_ENDPOINT = "PEGA_AQUI_TU_URL_DE_APPS_SCRIPT";
const SUBSTACK_URL   = "PEGA_AQUI_TU_SUBSTACK";
```

- **SHEET_ENDPOINT** → la URL de tu Google Apps Script (la que sale al desplegar el script; ver `GUIA_INSTALACION.md`). Sin esto, el formulario no guardará correos.
- **SUBSTACK_URL** → el enlace de tu Substack (ej. `https://pathahead.substack.com`).

Puedes hacerlo de dos formas:
- **Ahora**, abriendo `index.html` en tu compu con un editor de texto (Bloc de notas / TextEdit), reemplazando los textos entre comillas y guardando.
- **O después de subirlo**, editándolo directo en GitHub (te explico cómo en el paso 7). Si prefieres, sube primero y configúralo allá.

> Importante: deja las comillas. Solo reemplaza el texto de adentro. Ejemplo correcto:
> `const SUBSTACK_URL = "https://pathahead.substack.com";`

---

## Paso 1 — Crea una cuenta en GitHub (gratis)

1. Entra a **https://github.com** y haz clic en **Sign up**.
2. Usa tu correo, elige un usuario (ej. `pathahead`) y una contraseña.
3. Confirma tu correo. Listo.

> El usuario que elijas será parte de tu URL final. Si eliges `pathahead`, tu sitio será `https://pathahead.github.io/...`.

---

## Paso 2 — Crea un repositorio

Un "repositorio" (repo) es solo una carpeta para tu proyecto.

1. Arriba a la derecha, haz clic en el **+** → **New repository**.
2. En **Repository name** escribe algo simple, por ejemplo: `pathahead`.
3. Déjalo en **Public** (necesario para que GitHub Pages sea gratis).
4. **No** marques "Add a README" (lo subiremos nosotros).
5. Haz clic en **Create repository**.

---

## Paso 3 — Sube el archivo `index.html`

1. En la página del repo recién creado, busca el enlace **"uploading an existing file"** (o ve a **Add file → Upload files**).
2. **Arrastra** tu archivo `index.html` a la zona de carga (o haz clic en *choose your files* y selecciónalo).
   - Si quieres, sube también `README.md` para que el repo se vea ordenado.
3. Abajo, haz clic en el botón verde **Commit changes**.

> El archivo **debe llamarse exactamente `index.html`** (en minúsculas). Así GitHub lo muestra automáticamente al entrar a tu URL.

---

## Paso 4 — Activa GitHub Pages

1. En tu repo, haz clic en **Settings** (arriba a la derecha).
2. En el menú izquierdo, haz clic en **Pages**.
3. En **Source**, elige **Deploy from a branch**.
4. En **Branch**, selecciona **main** y la carpeta **/ (root)**.
5. Haz clic en **Save**.

---

## Paso 5 — Obtén tu URL

1. Espera **1-2 minutos** (GitHub está publicando tu sitio).
2. Recarga la página de **Settings → Pages**. Aparecerá un recuadro:
   *"Your site is live at"* con tu enlace, por ejemplo:
   **`https://pathahead.github.io/pathahead/`**
3. Haz clic y verás tu calculadora en vivo. 🎉

> Si ves un error 404, espera un minuto más y recarga. La primera publicación a veces tarda.

---

## Paso 6 — Compártela

Pega esa URL en:
- El botón/enlace de tu **Substack** (en un post o en la página de inicio).
- Tu **LinkedIn** (en un post o en "Featured").

Cada correo que dejen entra a tu Google Sheet automáticamente.

---

## Paso 7 — Editar o actualizar después (opcional)

**Para configurar los enlaces directamente en GitHub** (si no lo hiciste antes):
1. En tu repo, haz clic en `index.html`.
2. Haz clic en el ícono del **lápiz** (✏️ Edit this file), arriba a la derecha.
3. Usa `Ctrl/Cmd + F` para buscar `PEGA_AQUI`, reemplaza los dos enlaces.
4. Abajo, **Commit changes**. Tu sitio se actualiza solo en ~1 minuto.

**Para subir una versión nueva de la calculadora más adelante:**
1. **Add file → Upload files**, arrastra el `index.html` nuevo (mismo nombre).
2. **Commit changes**. Reemplaza al anterior y se actualiza en vivo.

---

## Si algo no funciona

- **El sitio da 404** → espera 1-2 min, recarga; revisa que el archivo se llame `index.html` y que en Pages esté en `main` / `root`.
- **El formulario no guarda correos** → falta pegar `SHEET_ENDPOINT` (paso "Antes de empezar"). Revisa que tu Apps Script esté desplegado como *Aplicación web* con acceso *"Cualquier persona"* (ver `GUIA_INSTALACION.md`).
- **El botón del Substack no aparece** → falta pegar `SUBSTACK_URL` (es normal que esté oculto si no lo pusiste).
- **Quiero un dominio propio** (ej. `calculadora.pathahead.com`) → se puede en **Settings → Pages → Custom domain**, pero eso es un paso avanzado para más adelante.

---

¡Eso es todo! Con esto tu calculadora está pública, gratis y lista para recoger correos y datos reales.
