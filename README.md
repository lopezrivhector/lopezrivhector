# Portafolio Digital — Héctor A. López Rivera

Portafolio personal académico/preprofesional, minimalista y classy. Una sola página HTML, sin dependencias de servidor, completamente editable.

---

## 📁 Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | El portafolio completo (HTML + CSS + JS embebidos en un solo archivo). |
| `cv.pdf` | Tu CV en PDF — se descarga desde el botón "Download CV". |
| `README.md` | Esta guía. |

> **Pendiente:** sube tu foto profesional como `profile.jpg` cuando la tengas (ver paso 4 más abajo).

---

## 🚀 Publicar en internet (GitHub Pages, gratis) — 10 minutos

### Paso 1 · Crea una cuenta de GitHub

1. Entra a [github.com](https://github.com) y crea una cuenta con tu correo `lopezriv.hector@gmail.com`.
2. **Username sugerido:** `hectorlopezrivera` o `halopezrivera` — esto se convierte en parte de tu URL si no compras dominio.

### Paso 2 · Crea el repositorio del portafolio

1. Click en **"+" → "New repository"**.
2. Repository name: **`hectorlopezrivera.github.io`** (sustituye `hectorlopezrivera` por tu username de GitHub — el nombre del repo **debe ser exactamente** `tuusuario.github.io` para que funcione automáticamente).
3. Selecciona **Public**.
4. Marca ✅ "Add a README file".
5. Click **"Create repository"**.

### Paso 3 · Sube los archivos

**Opción A — desde el navegador (más fácil):**

1. En tu repo nuevo, click **"Add file" → "Upload files"**.
2. Arrastra `index.html`, `cv.pdf` y (cuando la tengas) `profile.jpg`.
3. Scroll abajo, click **"Commit changes"**.
4. Espera 1–2 minutos.
5. Visita `https://tuusuario.github.io` — ¡tu portafolio está en línea!

**Opción B — desde la terminal (más profesional, mejor para edits frecuentes):**

```bash
git clone https://github.com/tuusuario/tuusuario.github.io.git
cd tuusuario.github.io
# Copia index.html y cv.pdf a esta carpeta
git add .
git commit -m "Initial portfolio"
git push origin main
```

### Paso 4 · Activa GitHub Pages (si no se activó automáticamente)

1. En el repo, ve a **Settings → Pages** (menú lateral izquierdo).
2. Source: **"Deploy from a branch"**.
3. Branch: **`main`** / Folder: **`/ (root)`** → **Save**.
4. Espera unos minutos. Tu sitio aparece en `https://tuusuario.github.io`.

---

## 🌐 Conseguir un dominio personalizado (opcional, ~$12/año)

Para que la URL sea **`hectorlopezrivera.com`** en vez de `hectorlopezrivera.github.io`:

### A · Compra el dominio

Recomendados (en orden de mejor precio/calidad):

1. **[Namecheap](https://www.namecheap.com)** — `.com` ~$10–15/año, panel limpio.
2. **[Porkbun](https://porkbun.com)** — incluso más barato, transparente.
3. **[Cloudflare Registrar](https://www.cloudflare.com/products/registrar/)** — al precio de costo (sin markup).

**Sugerencias de dominios:**

- `hectorlopezrivera.com` ← más limpio
- `halopezrivera.com`
- `hectorlopez.md` ← `.md` es elegante para futuros médicos (un poco más caro)
- `hectorlopezrivera.science`

### B · Conecta el dominio a GitHub Pages

**En tu proveedor de dominio (Namecheap, etc.) — DNS settings:**

Agrega estos registros:

| Type | Host / Name | Value |
|---|---|---|
| A | @ | `185.199.108.153` |
| A | @ | `185.199.109.153` |
| A | @ | `185.199.110.153` |
| A | @ | `185.199.111.153` |
| CNAME | www | `tuusuario.github.io` |

**En GitHub:**

1. Ve a **Settings → Pages → Custom domain**.
2. Escribe `hectorlopezrivera.com` (o el dominio que compraste) → **Save**.
3. Espera 10–60 minutos a que se propague el DNS.
4. Cuando GitHub valide, marca ✅ **"Enforce HTTPS"** (importante: certificado SSL gratis).

¡Listo! Tu portafolio vive en tu dominio personalizado.

---

## ✏️ Cómo editar tu portafolio

El portafolio es UN solo archivo HTML, así que editarlo es directo. Tienes dos formas:

### Forma rápida — directo en GitHub (desde cualquier dispositivo)

1. Entra a tu repo en github.com.
2. Click en `index.html`.
3. Click el ícono del **lápiz** (Edit) arriba a la derecha.
4. Edita el texto que quieras (la búsqueda con `Ctrl+F` / `Cmd+F` ayuda mucho).
5. Scroll abajo, click **"Commit changes"**.
6. En 1–2 minutos los cambios aparecen en tu sitio.

### Forma profesional — VS Code en tu computadora

1. Instala [VS Code](https://code.visualstudio.com).
2. Clona el repo: `git clone https://github.com/tuusuario/tuusuario.github.io.git`
3. Abre la carpeta en VS Code.
4. Abre `index.html` y usa `Live Server` (extensión) para previsualizar mientras editas.
5. Cuando termines: `git add . && git commit -m "Update content" && git push`

---

## 🎯 Lugares clave para editar (con ejemplos)

Abre `index.html` y busca (`Ctrl+F`/`Cmd+F`) estas frases:

| Buscar | Qué edita |
|---|---|
| `<!-- HERO -->` | Tu nombre, título profesional, ubicación, teléfono. |
| `<!-- ABOUT -->` | Bio personal, intereses de investigación, estadísticas (pillars). |
| `<!-- EDUCATION -->` | Universidades, GPA, fechas, coursework. |
| `<!-- RESEARCH -->` | Experiencias de investigación (Miami, UPR, MIT, etc.). |
| `<!-- SKILLS -->` | Habilidades con barras de progreso. Cambia `--skill-level: 90%;` para ajustar. |
| `<!-- PUBLICATIONS -->` | Manuscritos, posters y oral presentations. |
| `<!-- CLINICAL -->` | Horas de shadowing por especialidad. |
| `<!-- LEADERSHIP -->` | SfN Neuronline, Red Cross, NSA, AMSA, HOSA. |
| `<!-- HONORS -->` | Honors, awards, certificaciones CITI, ORCID. |
| `<!-- CONTACT -->` | Email, LinkedIn, ORCID. |

### Agregar tu foto profesional

1. Súbela al repo con el nombre **`profile.jpg`** (o `.png`).
2. En `index.html`, busca `<!-- Reemplazar con:` y reemplaza el `<div class="hero-photo-frame"></div>` por:

```html
<img src="profile.jpg" alt="Héctor López Rivera" />
<div class="hero-photo-frame"></div>
```

Mientras no la tengas, el sitio muestra tu monograma "HALR" elegante.

### Cambiar la paleta de colores

Al inicio del CSS hay variables. Cambia estos valores y todo el sitio se actualiza:

```css
:root {
  --bg: #fbfaf6;       /* fondo principal */
  --navy: #1a2a44;     /* azul oscuro (acento principal) */
  --gold: #b8935f;     /* dorado (acento secundario) */
  --ink: #1a1a1a;      /* texto principal */
}
```

### Actualizar el CV

Cuando actualices tu CV en Word, reemplaza `cv.pdf` en el repo con la versión nueva (mismo nombre). El botón "Download CV" automáticamente sirve la versión actualizada.

---

## 🔧 Próximos pasos sugeridos

- [ ] Subir foto profesional (`profile.jpg`)
- [ ] Crear cuenta de GitHub y subir los 3 archivos
- [ ] Decidir dominio personalizado y comprarlo
- [ ] Compartir la URL en LinkedIn, en signatures de email, en aplicaciones a programas
- [ ] Agregar Google Analytics (opcional, te dice cuánta gente visita el sitio)
- [ ] Considerar un blog en el futuro (escribir sobre research, MD/PhD path, etc.)

---

## 💡 Notas técnicas

- **Sin dependencias de build:** es HTML+CSS+JS puro. Funciona abriendo `index.html` directo en un navegador.
- **Responsive:** se adapta a teléfono, tablet y desktop.
- **Performance:** carga súper rápido (todo en un archivo, fonts desde Google).
- **SEO:** incluye meta tags básicos (description, Open Graph) para compartir en redes.
- **Accesibilidad:** semántico, focus visible, contraste adecuado.
- **Imprimible:** se ve decente al imprimir (`Ctrl+P`).

---

¿Preguntas o necesitas ayudar a configurar algo? Estoy aquí cuando quieras.
