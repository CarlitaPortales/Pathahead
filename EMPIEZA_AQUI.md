# PathAhead · Empieza aquí — lanzar el MVP en 4 pasos

Tiempo total: **~20-25 minutos.** Todo se hace desde el navegador, sin programar.

Al final tendrás:
- Una calculadora pública en una URL (ej. `https://tuusuario.github.io/pathahead/`)
- Cada correo y perfil que dejen, llegando solo a tu Google Sheet

---

## Los archivos de este paquete

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La calculadora. Es lo que se publica. |
| `apps_script.gs` | El código que guarda los correos en tu Google Sheet. |
| `GUIA_INSTALACION.md` | Cómo crear el Google Sheet + Apps Script (Paso 1). |
| `PUBLICAR_EN_GITHUB.md` | Cómo subir la calculadora a GitHub (Paso 3). |
| `README.md` | Descripción del proyecto (opcional, para que el repo se vea ordenado). |

---

## Paso 1 — Backend: dónde caen los correos (~7 min)

Sigue **`GUIA_INSTALACION.md`**. En resumen:
1. Crea un Google Sheet nuevo.
2. Extensiones → Apps Script → pega todo el contenido de `apps_script.gs`.
3. Despliega como **Aplicación web**, con acceso **"Cualquier persona"**.
4. **Copia la URL** que te da (la necesitas en el Paso 2).

---

## Paso 2 — Conecta los 2 enlaces (~2 min)

Abre `index.html` con el Bloc de notas / TextEdit y reemplaza estas dos líneas (cerca del inicio del `<script>`):

```js
const SHEET_ENDPOINT = "PEGA_AQUI_TU_URL_DE_APPS_SCRIPT";   // ← la URL del Paso 1
const SUBSTACK_URL   = "PEGA_AQUI_TU_SUBSTACK";             // ← tu Substack
```

Deja las comillas, reemplaza solo el texto de adentro. Guarda.

> Si prefieres, puedes hacerlo **después** de subir el archivo, editándolo directo en GitHub (ver Paso 3).

---

## Paso 3 — Publica la calculadora (~10 min)

Sigue **`PUBLICAR_EN_GITHUB.md`**. En resumen:
1. Crea cuenta en github.com.
2. Crea un repositorio público (ej. `pathahead`).
3. Sube `index.html` (y `README.md` si quieres).
4. Settings → Pages → branch `main` / `root` → Save.
5. Espera 1-2 min y copia tu URL pública.

---

## Paso 4 — Compártela y empieza a aprender (~2 min)

1. Pega tu URL en un post de **Substack** y en **LinkedIn**.
2. Cada persona que deje su correo entra a tu Google Sheet, con su perfil:
   `tipo · salida · nivel · prioridad · programa más barato/rápido` — y, si ya estudió en US, su universidad, comp real y visa.

Esa data que entre es justo lo que te falta para **calibrar los números** con casos reales.

---

## Después del lanzamiento (cuando quieras)

- **Corregir un dato de un programa** → edita el bloque `PROGRAMS` en `index.html` (sube la versión nueva a GitHub, se actualiza solo).
- **Ver quién entró** → revisa tu Google Sheet.
- **Escribir el post de lanzamiento** → cuando estés lista, te ayudo a armarlo (Substack + LinkedIn) con los datos que ya tienes.

---

## Checklist rápido

- [ ] Google Sheet + Apps Script desplegado (Paso 1)
- [ ] `SHEET_ENDPOINT` y `SUBSTACK_URL` pegados en `index.html` (Paso 2)
- [ ] `index.html` subido a GitHub + Pages activado (Paso 3)
- [ ] URL pública funcionando
- [ ] Probé dejar un correo de prueba y apareció en el Sheet
- [ ] Link compartido en Substack / LinkedIn

¡Eso es el MVP en vivo!
