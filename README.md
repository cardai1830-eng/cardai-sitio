# cardai.mx

Sitio web de Cardai Solutions. Una sola página en HTML, sin dependencias ni proceso de compilación.

## Publicar

El flujo `.github/workflows/pages.yml` publica la raíz del repositorio en GitHub Pages con cada cambio en `main`.

Primera vez: Settings → Pages → Build and deployment → Source: **GitHub Actions**. Después, Settings → Pages → Custom domain → `cardai.mx` y **Enforce HTTPS** cuando el DNS esté listo.

## Configurar

Al inicio de `index.html` está el bloque `window.CARDAI` con cuatro valores:

| Valor | Para qué |
| --- | --- |
| `formEndpoint` | Endpoint de Formspree que recibe el formulario por correo |
| `whatsapp` | Número con código de país y sin signos, por ejemplo `5215512345678` |
| `agendaUrl` | Enlace de agenda; lo usan todos los botones "Agenda una llamada" |
| `pixelId` | Identificador del píxel de Meta |

Mientras un valor esté vacío, el sitio funciona sin esa pieza.

## Archivos

| Archivo | Qué es |
| --- | --- |
| `index.html` | La página principal; cada sección lleva un comentario y un `id` |
| `aviso-de-privacidad.html` | Aviso de privacidad; sustituir los datos entre corchetes |
| `404.html` | Página de error |
| `og-image.png` | Imagen al compartir el enlace en redes |
| `favicon.svg`, `favicon-96.png`, `apple-touch-icon.png`, `icon-512.png` | Iconos |
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Buscadores y manifiesto |
