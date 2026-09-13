# Portfolio — puesta en marcha

Sitio estático hecho con Quarto. Todo el stack es gratuito.

## 1. Instalar Quarto

Descargar desde quarto.org e instalar. Comprobar con:

    quarto --version

## 2. Ver el sitio en local

Desde esta carpeta:

    quarto preview

Se abre en el navegador y se recarga al guardar cambios.

## 3. Publicar gratis en GitHub Pages

1. Crear un repositorio en GitHub (público o privado; con privado hacen falta
   GitHub Pages de pago, así que para la opción gratuita: público).
2. Subir esta carpeta.
3. Desde la carpeta del proyecto:

       quarto publish gh-pages

   Quarto crea la rama `gh-pages`, publica y devuelve la URL.
4. En `_quarto.yml`, sustituir `USUARIO` en `site-url` por el usuario real.

## 4. Privacidad

El sitio sale publicado con dos capas de "no me indexes":

- `robots.txt` con `Disallow: /`
- `<meta name="robots" content="noindex, nofollow">` en todas las páginas

Esto impide que aparezca al buscar el nombre en Google, pero **no** lo protege:
cualquiera con el enlace entra. Si hiciera falta control de acceso real, la
opción habitual es poner Cloudflare Access por delante.

## 5. Añadir un artículo nuevo

Crear una carpeta dentro de `posts/` con un `index.qmd` que empiece así:

    ---
    title: "Título del artículo"
    description: "Una frase que explique de qué va."
    date: 2026-10-01
    ---

Las imágenes van en la misma carpeta y se referencian por nombre.
El índice de `articulos.qmd` se actualiza solo.

## 6. Pendiente

- Añadir `cv.pdf` en la raíz (el enlace de la portada ya apunta ahí).
- Sustituir `USUARIO` en `_quarto.yml`.
