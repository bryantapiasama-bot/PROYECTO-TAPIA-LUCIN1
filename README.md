# Geovisualizador Urbano de Machala

Mapa catastral interactivo del sector Urdesa Norte (Machala, Ecuador) — uso de suelo, accesibilidad y riesgo de inundación.

Construido con [Leaflet.js](https://leafletjs.com/), HTML/CSS/JS puro. No requiere backend ni build: es un único archivo (`index.html`) que se puede abrir directamente en el navegador o publicar como sitio estático.

## 🌐 Ver en vivo

Una vez publicado con GitHub Pages (ver abajo), el sitio quedará disponible en:

```
https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/
```

## 🚀 Cómo publicarlo en GitHub Pages

### Opción A — Desde la web de GitHub (sin usar la terminal)

1. Entra a [github.com](https://github.com) e inicia sesión (crea una cuenta gratis si no tienes).
2. Click en **New repository** (botón verde, esquina superior derecha).
3. Ponle un nombre, por ejemplo `geovisualizador-machala`. Déjalo en **Public**. No marques ninguna casilla de inicialización. Click en **Create repository**.
4. En la página del repositorio recién creado, click en **uploading an existing file** (o el botón **Add file → Upload files**).
5. Arrastra los archivos de esta carpeta: `index.html`, `README.md`, `.nojekyll` y `LICENSE`.
6. Escribe un mensaje de commit (ej. "Primera versión del geovisualizador") y click en **Commit changes**.
7. Ve a la pestaña **Settings** del repositorio → menú lateral **Pages**.
8. En **Build and deployment → Source**, selecciona **Deploy from a branch**.
9. En **Branch**, elige `main` y la carpeta `/ (root)`. Click en **Save**.
10. Espera 1–2 minutos y recarga la página. GitHub te mostrará el enlace público arriba: `https://TU-USUARIO.github.io/geovisualizador-machala/`.

### Opción B — Desde la terminal (git)

```bash
# Dentro de la carpeta con los archivos:
git init
git add .
git commit -m "Primera versión del geovisualizador"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/geovisualizador-machala.git
git push -u origin main
```

Luego repite los pasos 7–10 de la Opción A para activar GitHub Pages.

## 📂 Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `index.html` | El mapa completo (interfaz + datos catastrales embebidos). GitHub Pages sirve automáticamente este archivo como página principal. |
| `.nojekyll` | Le dice a GitHub que no procese el sitio con Jekyll (evita conflictos con archivos que empiecen con `_`). |
| `README.md` | Este archivo. |
| `LICENSE` | Licencia MIT (opcional, puedes borrarla o cambiarla si no la necesitas). |

## 🛠️ Datos y fuentes

- Sistema de referencia: UTM Zone 17S · EPSG:32717 · Datum WGS84.
- `valor_m2` y `cota_msnm` son estimaciones modeladas, no valores catastrales oficiales.
- Cartografía base: OpenStreetMap / CARTO / Esri World Imagery.
- Proyecto académico — Universidad Técnica de Machala, Geomática.

## ✏️ Actualizar el mapa

Para modificar los datos o el diseño, edita directamente `index.html`: los datos GeoJSON están en la constante `DATA` al inicio del `<script>`, y los estilos en el bloque `<style>`. Después de editar, vuelve a subir el archivo al repositorio (o haz `git add . && git commit -m "..." && git push`) y GitHub Pages actualizará el sitio automáticamente en 1–2 minutos.
